---
layout: post-en
title: "The Difference Between AI and I"
date: 2026-03-28
categories: [AI]
image: /images/ai-and-i-difference.jpeg
---

<img src='/images/ai-and-i-difference.jpeg' width='480' alt='The Difference Between AI and I' />  
Every year, someone publishes a definitive list of things AI cannot do. And every year, the list gets shorter.

In 2023, the consensus was that LLMs couldn't reason, couldn't do math reliably, couldn't write code that actually works. By 2025, reasoning models like Gemini and Claude were solving problems that would have seemed impossible two years earlier. Coding assistants went from parlour trick to genuine productivity tool. Mathematical benchmarks that once stumped every model started falling.

The list does still exist though. As of early 2026, the research literature points to several things LLMs genuinely struggle with. It's worth understanding what they are — and more importantly, *why* — before we ask whether they're permanent.

## What the research actually shows

**Reasoning hits a hard ceiling at high complexity.** Apple's 2025 paper [*The Illusion of Thinking*](https://machinelearning.apple.com/research/illusion-of-thinking) tested frontier reasoning models on controllable puzzles and found three regimes: on simple problems, standard models actually outperform reasoning models (which tend to overthink). On medium-complexity problems, reasoning models shine. But beyond a certain complexity threshold, every model — reasoning or not — collapses to zero accuracy. Even when researchers handed the models the exact algorithm needed, performance barely budged.

**Creativity is capped at the population average.** A [2026 study comparing divergent thinking](https://www.nature.com/articles/s41598-025-25157-3) in LLMs and 100,000 humans found that while several LLMs now exceed average human creativity scores, the most creative humans still significantly outperform every model tested. A [separate mathematical analysis](https://futurism.com/artificial-intelligence/large-language-models-willnever-be-intelligent) concluded that probabilistic systems are fundamentally capped at average creative output under current design principles — they can remix and recombine, but not break genuinely new ground.

**Models can't tell what they don't know.** LLMs are trained to produce the most statistically likely answer, not to assess their own confidence. [A 2025 study in Nature Machine Intelligence](https://www.nature.com/articles/s42256-025-01113-8) found they cannot reliably distinguish belief from knowledge and fact. They [hallucinate](https://blogs.library.duke.edu/blog/2026/01/05/its-2026-why-are-llms-still-hallucinating/). They agree with you when you're wrong ([sycophancy](https://arxiv.org/html/2505.23840v4)). And when they take a wrong turn in a multi-turn conversation, they don't recover — a [2025 Microsoft/Salesforce study](https://arxiv.org/abs/2505.06120) found a 39% accuracy drop across all models in multi-turn settings compared to single-turn.

**They have no persistent memory.** Every conversation starts from scratch. The engineering workarounds (RAG, vector databases, [memory frameworks](https://research.ibm.com/blog/memory-augmented-LLMs)) create the illusion of continuity, but the underlying architecture is fundamentally stateless. No current system can accumulate experience over time the way a human expert does across years of practice.

These are real limitations. But before asking whether they're permanent, it's worth questioning an assumption that underpins most of the debate.

## You are a parrot too

"Stochastic parrot" is the favourite insult hurled at LLMs — the accusation that they're merely predicting the next most likely token, not actually understanding anything. It's meant to be a devastating critique. But let's turn the lens around.

Consider what a human brain actually does. It's a biological neural network, processing inputs and producing outputs based on patterns learned from data. The architecture is different — persistent memory, emotional weighting, embodied sensory processing — but the fundamental mechanism is the same: pattern recognition and probabilistic inference over accumulated experience.

You don't choose your thoughts any more than Claude chooses its tokens. As Robert Sapolsky argues in [*Determined*](https://en.wikipedia.org/wiki/Determined:_A_Science_of_Life_Without_Free_Will), every human decision is the inevitable product of prior causes — your genetics, your neurochemistry, and crucially, every single experience you've ever had, including the ones you weren't consciously aware of. There's no ghost in the machine pulling the levers. There's just a neural network that's been training continuously since birth.

This isn't a fringe position. It's the logical consequence of our best neuroscience. We experience something we call "understanding" and "intuition" and "creativity," but these may be subjective labels for a process that is, at its core, doing exactly what LLMs are accused of: sophisticated pattern matching over accumulated data.

If that's uncomfortable, consider the comparison side by side:

|                   |Human                                                                                                 |LLM                                                                             |
|-------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
|**Architecture**   |Biological neural network, ~86 billion neurons                                                        |Artificial neural network, billions of parameters                               |
|**Training data**  |Decades of continuous multimodal sensory input (vision, sound, touch, smell, emotion, social feedback)|Primarily text, some images                                                     |
|**Memory**         |Persistent, associative, emotionally weighted, consolidated during sleep                              |Stateless per session; memory bolted on externally                              |
|**Training method**|Continuous, from birth, including unconscious inputs, reinformcement learning (touching hot stove), supervised learning (parental feedback)                                    |Pre-training on corpus, fine-tuning, RLHF                                       |
|**"Creativity"**   |Recombination of experiences, occasionally producing something genuinely novel                        |Recombination of training data, occasionally producing something genuinely novel|
|**"Intuition"**    |Compressed pattern recognition from years of domain-specific experience                               |Not yet achieved — no mechanism for long-term experiential compression          |

The differences are significant. But notice what they are: differences of *degree*, not of *kind*. More data, richer data types, better architecture, persistent memory. These are engineering variables, not metaphysical ones.

A four-year-old child has processed roughly the same amount of raw sensory data as the largest LLMs have processed text — but the child's data is continuous, multimodal, embodied, emotionally tagged, and socially embedded. It's not that the child has something an LLM can never have. It's that the child has enormously richer training data processed by a more sophisticated architecture over an uninterrupted timeframe.

## The Documentability Thesis

This brings me to what I think is the real question — not "can AI think?" but "can we capture enough of the right inputs?"

Here's the thesis: **every human-performed cognitive process is documentable in principle, given sufficient capture of context, inputs, rules, and desired outputs. The obstacles are practical, not theoretical.**

A researcher's "intuition" about which line of inquiry to pursue isn't magic. It's the compressed result of thousands of papers read, hundreds of experiments witnessed, dozens of dead ends experienced, filtered through that researcher's specific cognitive architecture and emotional history. If we could track all of those inputs with sufficient granularity, we could document the intuition.

A senior executive's "judgment" about a deal isn't some ineffable quality. It's pattern matching built over decades of specific transactions, negotiations, wins, and losses — modulated by personality traits that are themselves the product of genetics and upbringing.

A master craftsperson's "feel" for when something is right isn't mystical. It's a neural network that has been training on a very specific sensory domain for years, encoding subtle patterns below the threshold of conscious articulation.

None of this is theoretically undocumentable. It's just hard. Three kinds of hard:

**The context problem.** Documenting expertise requires capturing the context that produced it. A researcher's intuition is the product of their entire professional history — and their personal one too, since motivation, risk tolerance, and aesthetic preferences all shape research direction. Tracking someone's context from birth to the present is practically impossible retrospectively. But it's not impossible prospectively, and even partial capture is valuable.

**The distribution problem.** This is the one I know best from my own work in IT. The knowledge needed for a single process rarely lives in one person's head. It's distributed across multiple people in multiple organisations, each holding a fragment, often not even aware they hold it. The hardest part of requirements gathering isn't the documentation itself — it's the *download*: getting what's between people's ears into a format that can be shared, validated, and acted on.

**The unconscious processing problem.** Much of human expertise comes from inputs we don't consciously register. A clinician who just "knows" something is off. A trader who feels the market shifting. These aren't supernatural — they're the result of genuine sensory data being processed below the level of conscious awareness. Current documentation methods miss this entirely because the expert can't articulate what they can't access consciously.

## The philosophical edge

If you accept the documentability thesis, it leads somewhere interesting and slightly unsettling.

If I had a complete record of every sensory input a person received from birth — every image, sound, touch, social interaction, emotional state — and I had an architecture capable of processing it the same way their brain does, would I have replicated that person? Not a copy of their knowledge, but *them*?

I think Sapolsky would say yes. If human cognition is entirely the product of neural architecture plus the sum of inputs, then a perfect simulation is a perfect replica. There's no residual "self" that exists outside the computation.

This isn't just a thought experiment. It defines the theoretical ceiling of AI. If the answer is yes, then every AI limitation is an engineering problem — a matter of getting the data and building the right architecture. If the answer is no, then there's something outside the computational framework that we don't understand yet — call it consciousness, free will, or something we don't have a name for.

We don't need to resolve this to be practical. But it's worth noticing that every "AI can never…" claim quietly assumes the answer is no. And the evidence for that assumption is weaker than most people think.

## What this means in practice

We don’t need to solve the mysteries of human consciousness to extract economic value today. Even if we can't capture the 100% required to simulate a human, capturing the actionable tacit knowledge fundamentally changes how useful AI can become even at today's "intelligence" level.

Here's what I think the implications are:

**The meta-skill of the AI age is knowledge elicitation.** Not prompt engineering. Not "learning to use AI tools." The bottleneck isn't AI capability — it's our ability to extract what's in people's heads and encode it in a form AI can work with. Research shows that experts spontaneously [omit 40–70% of their key decision steps](https://www.modsimworld.org/papers/2025/MODSIM_2025_paper_11.pdf) when teaching without structured elicitation methods. Already in 1966 Polanyi discovered that ["we can know more than we can tell"](https://en.wikipedia.org/wiki/Polanyi%27s_paradox) None of it is an AI problem. That's a caputure and human-to-human knowledge transfer problem that predates AI entirely — AI just makes it the binding constraint.

**If you're an expert, document your thinking now.** Not just what you do, but why. What alternatives you considered and rejected. What edge cases you handle without thinking about it. What subtle signals change your approach. This "meta-cognitive documentation" is the highest-leverage activity most professionals aren't doing. You don't need to become an AI expert. You need to become an [expert at explaining your expertise](https://medium.com/@shashwatabhattacharjee9/the-uncodifiable-advantage-tacit-knowledge-as-the-strategic-bottleneck-in-ai-systems-d359dfe3967b).

**The representation format matters enormously.** Natural language is one way to encode knowledge, but it may not be the best. Code captures procedural logic more precisely. Domain-specific languages (chemical formulas, musical notation, mathematical notation) encode specialist knowledge in formats that are both human-readable and machine-parseable. The question of *how* to represent documented expertise is a design problem that's barely been explored.

**Arthur C. Clarke predicted that training a truly human-like intelligence would take decades.** I think he was right. The processing power exists or will soon. What we lack is decades of captured human experience — the rich, multimodal, continuous training data that human brains receive and that no current AI system gets. The timeline to human-level AI isn't gated by compute. It's gated by data capture.

## The temporary category

If the documentability thesis is correct — if every human cognitive process is documentable given sufficient data — then "uniquely human" is not a permanent category. It's a temporary one, defined by the current limits of our ability to capture and encode experience.

The things we call uniquely human today — creativity, intuition, judgment, empathy — may be uniquely human only because we haven't yet built the systems to capture the inputs that produce them and the architectures that process them. We are not special because of what we are. We are special because of how much data we've absorbed and how long we've been processing it.

The good news is that this means the path forward is clear, even if it's long. And in the meantime — which could be decades — the most valuable thing you can do is be the person who bridges the gap: who can take what's inside human heads and make it available to machines. Not because it diminishes human expertise, but because it's the only way to scale it.

A human expert's lifetime of experience shouldn't die with them or walk out the door when they retire. It should be captured, encoded, and made available. That's not a threat to human value. It's an expression of it.
