# Product Requirements Document: Test Runner MVP

## Overview

A standalone, browser-based test runner designed for children learning in their second language. The app loads a test definition from a JSON file, presents questions one at a time in a wizard-style flow, records detailed interaction data (including translation usage), evaluates answers, and outputs both the attempt record and evaluation results as downloadable JSON files.

This MVP is a single-user, no-backend trial. All logic runs client-side in HTML and JavaScript. AI-evaluated free text questions use the Anthropic API with a user-provided API key stored in localStorage.

## Target Users

Children across a mixed age range (approximately 5–13), taking tests in a second language with English as their primary language. The UI must be accessible and clear for younger children while not feeling patronising to older ones.

## Data Schemas

The app is built around three JSON schemas developed alongside this PRD:

- **Test Definition** (`test-definition-schema.json`) — the test content, structure, media library, multilingual strings, evaluation config, and question weights.
- **Test Attempt** (`test-attempt-schema.json`) — the event-based record of everything the student did during the test.
- **Test Evaluation** (`test-evaluation-schema.json`) — the scored results produced by running evaluation logic against the attempt data.

These schemas are the source of truth for all data structures. This PRD does not duplicate their contents but references them throughout.

## Core User Flow

### 1. Setup Screen

The user is presented with a clean landing screen with two actions:

- **Load Test**: a file picker that accepts a `.json` file conforming to the test definition schema.
- **Settings**: access to configure the Anthropic API key (stored in localStorage). A simple input field with a save button and a visual indicator of whether a key is currently stored.

Once a valid test file is loaded, the app displays the test title, description, and instructions (in the test's `default_locale`), along with a **Start Test** button.

Validation on load should check for: valid JSON, presence of required top-level fields (`id`, `title`, `questions`), and that all `media_refs` in questions point to entries in the `media` array. Display clear error messages if validation fails.

### 2. Question Display (Wizard Flow)

Questions are presented one at a time. The screen shows:

- **Progress indicator**: "Question 3 of 12" and a simple progress bar.
- **Section header** (if the current question belongs to a section): the section title and description, shown when entering a new section.
- **Question text** in the test's `default_locale`.
- **Media** associated with the question (images displayed inline, referenced from the test-level media library).
- **Answer input** appropriate to the `answer_type` (see Answer Types below).
- **Navigation**: Back and Next buttons. Next is disabled until the question is answered (unless `allow_skip` is true in test settings, in which case a Skip button is also shown).
- **Translation controls** (see Translation UX below).
- **Hint button** (if `show_hints` is enabled in settings): reveals the hint text for the current question. Only shown after a first incorrect attempt, or always available — to be determined during implementation based on what feels right for the age range.

#### Answer Types (MVP)

| Type | UI Control | Evaluation |
|---|---|---|
| `single_choice` | Radio buttons with option text and optional media | Deterministic: compare selected option ID to `correct_answer` |
| `multi_choice` | Checkboxes with option text and optional media | Deterministic: compare selected option IDs to `correct_answer` array |
| `number` | Numeric input field | Deterministic: compare to `correct_answer` within `numeric_tolerance` |
| `free_text` (deterministic) | Text input or textarea | Deterministic: compare to `correct_answer` and `alternatives`, respecting `case_sensitive` flag |
| `free_text` (AI evaluated) | Textarea | AI: send student response + `ai_prompt_context` to Anthropic API |

The distinction between deterministic and AI-evaluated free text is driven by the `evaluation.method` field on the question definition.

### 3. Translation UX

Each question has two translation toggle buttons:

- **Translate question**: toggles the display of the translated question text alongside or below the original. A single button that reveals the translation for the question body.
- **Translate options**: toggles the display of translations for all answer options at once (only shown for choice-based question types).

When a hint or feedback is displayed, it also gets its own translate toggle.

Translation toggles reveal text in the student's primary language (English) when the test is presented in another locale, or in the first available non-default locale when the test is in English. The specific `from_locale` and `to_locale` are recorded in the event stream.

Every translation toggle interaction generates a `translation_requested` event in the attempt record with the appropriate `element` type, `element_id` (null for question text, specific option IDs are not needed since all options are translated together), and locale information.

### 4. Event Recording

Throughout the test, the app builds an attempt record conforming to the test attempt schema. Events are appended to each question's event array in real time. The following events are captured:

- `question_displayed` — when the question first renders on screen.
- `answer_submitted` — each time the student selects or enters an answer.
- `answer_changed` — when a previously submitted answer is modified.
- `translation_requested` — each toggle of a translation button, with element and locale detail.
- `hint_requested` — when the hint is revealed.
- `feedback_displayed` — when correct/incorrect feedback is shown.
- `media_interaction` — when the student interacts with media (zoom, etc.).
- `question_exited` — when the student navigates away from the question.

Timing data is captured automatically: `started_at` and `finished_at` at the attempt level, and `time_spent_seconds` per question calculated from display/exit events.

The `navigation_path` array at the attempt level records the sequence of question IDs as the student moves through the test, including revisits.

### 5. Test Completion and Evaluation

When the student reaches the last question and confirms submission (or when a test-level time limit expires), the app:

1. Finalises the attempt record with completion status and timing.
2. Runs evaluation against each question:
   - **Deterministic questions**: evaluated immediately in JavaScript by comparing the final answer against the test definition's `correct_answer`, `alternatives`, `numeric_tolerance`, and `case_sensitive` fields.
   - **AI-evaluated questions**: sends the student's response along with the question's `ai_prompt_context` to the Anthropic API. If no API key is configured, these questions are marked with `status: "skipped"` and `score: null` in the evaluation.
3. Produces an evaluation record conforming to the test evaluation schema, including per-question scores (0.0–1.0 normalised), weights, and the summary aggregation.

### 6. Results Screen

After evaluation, the student sees a results screen showing:

- Overall score (weighted percentage).
- Per-question breakdown: question text, their answer, whether it was correct, and the explanation (if `show_correct_answer_comment` is enabled).
- For AI-evaluated questions: the score and the AI's reasoning (from `raw_response`).
- For failed AI evaluations: a clear message that the question couldn't be auto-graded.
- Two download buttons:
  - **Download Attempt Data** — the full test attempt JSON.
  - **Download Evaluation** — the full test evaluation JSON.

## UI and Design Principles

- **Large, clear typography**: minimum 16px base font, scaling up for younger users. Question text should be prominent.
- **High contrast**: dark text on light backgrounds, clear visual distinction between question, options, and navigation.
- **Touch-friendly targets**: buttons and interactive elements minimum 44px tap target, with generous spacing.
- **Minimal visual clutter**: one question at a time, clear hierarchy, no distracting elements.
- **Translation toggles should be visually subtle but discoverable**: small flag icons or a "Show in English" link, not competing with the main question UI.
- **Progress should feel encouraging**: a progress bar that fills, friendly language ("3 of 12 — keep going!").
- **Responsive**: must work on tablets (primary expected device) and desktops. Mobile phone support is a nice-to-have but not required for MVP.

## Technical Constraints

- **No server backend**: all logic runs in the browser. The app is a single HTML file (or a small set of static files).
- **API key storage**: the Anthropic API key is stored in localStorage. A warning should be displayed that the key is stored locally and unencrypted.
- **File loading**: test definitions are loaded via the browser's file picker API.
- **File download**: attempt and evaluation JSON are generated in-browser and offered as file downloads via Blob URLs.
- **Media**: the test definition is self-contained. Images are stored as base64-encoded strings in the `data` field of each media entry. The app renders them using data URIs (`data:${mime_type};base64,${data}`). An optional `url` field is also supported for future server-backed usage. Resolution order: if `data` is present for the current locale, use it; otherwise fall back to `url`; otherwise fall back to `default_locale`. A soft file size limit of 50MB is recommended for test definitions; the app should display a warning (not a block) if the loaded file exceeds this.
- **Browser support**: modern evergreen browsers (Chrome, Firefox, Safari, Edge). No IE11 support.

## Out of Scope for MVP

- Test authoring or management UI.
- User accounts or authentication.
- Multiple concurrent users or shared results.
- Server-side storage of attempts or evaluations.
- Image choice answer type.
- Ordering and matching answer types.
- Audio or video media playback.
- Accessibility features beyond basic semantic HTML (screen reader optimisation, keyboard navigation are desirable but not blocking for the trial).
- Offline AI evaluation.
- Sections with independent time limits.
- Test-level time limits (the per-question `time_limit_seconds` should be respected if set).

## Open Questions

1. **Hint display timing**: should hints be available immediately, or only after a first incorrect attempt? Younger children may benefit from immediate access; older children may benefit from trying first.
2. **Answer feedback timing**: should the student see whether they got each question right immediately after answering (learning mode), or only at the end (test mode)? This could be a setting in the test definition.
3. **Free text deterministic matching**: how fuzzy should matching be? Exact match with alternatives may be too rigid for younger children with spelling difficulties. Consider simple normalisation (trim whitespace, collapse spaces) as a baseline.
4. **Translation locale selection**: if a test supports more than two locales, should the student be able to choose which translation to see, or does the app always translate to `default_locale`?
5. **Shuffled option recording**: the attempt schema records `option_order_presented` — should the results screen reconstruct the original presentation order or show options in definition order?

## Success Criteria for MVP Trial

- A test author can create a JSON file by hand, load it, and have a child complete the test.
- The attempt JSON accurately captures all interactions including translation usage.
- Deterministic evaluation produces correct results for all supported answer types.
- AI evaluation works when an API key is provided and degrades gracefully when it is not.
- The downloaded JSON files can be opened and inspected to verify data quality.
- A child aged 8–10 can navigate the test without adult help (beyond initial file loading).
