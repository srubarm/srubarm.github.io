---
layout: post
title: "Rozdíl mezi inteligencí umělou a mou"
date: 2026-03-28
categories: [AI]
image: /images/ai-and-i-difference.jpeg
---
<img src='/images/ai-and-i-difference.jpeg' width='480' alt='Rozdíl mezi AI a mnou' />  
Každý rok někdo publikuje definitivní seznam věcí, které AI neumí. A každý rok je ten seznam kratší.

V roce 2023 panovala shoda, že velké jazykové modely (LLM) nedokážou uvažovat, neumí spolehlivě počítat a nedokážou napsat funkční kód. O dva roky později už reasoning modely jako Gemini a Claude řešily úlohy, které by se v roce 2023 zdály nemyslitelné. Kódovací asistenti se z pouhé technologické hračky proměnili v reálný nástroj produktivity. Matematické benchmarky, na kterých dřív selhával každý model, začaly být pokořovány jeden po druhém.

Ten seznam ale pořád existuje. Na začátku roku 2026 výzkumná literatura poukazuje na několik oblastí, ve kterých LLM skutečně stále tápají. Stojí za to pochopit, o jaké oblasti jde – a hlavně *proč* – než se začneme ptát, jestli jsou tato omezení trvalá.

## Co skutečně ukazuje výzkum

**Reasoning naráží na své limity při vysoké složitosti.** Článek Applu z roku 2025 [*The Illusion of Thinking*](https://machinelearning.apple.com/research/illusion-of-thinking) testoval špičkové reasoning modely na dobře definovaných logických úlohách a odhalil tři režimy: u jednoduchých problémů standardní modely ve skutečnosti překonávají ty s reasoningem (které mají tendenci úkoly „překombinovávat“). U středně složitých problémů reasoning modely excelují. Ale za určitým prahem složitosti se všechny modely – ať už s reasoningem, nebo bez něj – propadnou na nulovou přesnost. A to i tehdy, když výzkumníci modelům předložili přesný algoritmus potřebný k řešení.

**Kreativita naráží na strop populačního průměru.** [Studie z roku 2026 porovnávající divergentní myšlení](https://www.nature.com/articles/s41598-025-25157-3) u LLM a 100 000 lidí zjistila, že některé modely sice v průměrném skóre kreativity překonávají průměrného člověka, ale nejkreativnější lidé stále výrazně překonávají každý testovaný model. [Samostatná matematická analýza](https://futurism.com/artificial-intelligence/large-language-models-willnever-be-intelligent) dospěla k závěru, že pravděpodobnostní systémy jsou při současných principech designu principiálně omezeny na průměrný kreativní výstup – dokážou remixovat a rekombinovat, ale nedokážou přijít s něčím skutečně novým.

**Modely nedokážou rozpoznat, co nevědí.** LLM jsou trénovány tak, aby produkovaly statisticky nejpravděpodobnější odpověď, ne aby posuzovaly vlastní míru jistoty. [Studie z roku 2025 v Nature Machine Intelligence](https://www.nature.com/articles/s42256-025-01113-8) zjistila, že nedokážou spolehlivě rozlišovat mezi domněnkou, znalostí a faktem. [Halucinují](https://blogs.library.duke.edu/blog/2026/01/05/its-2026-why-are-llms-still-hallucinating/). Přitakávají vám, i [když se mýlíte](https://arxiv.org/html/2505.23840v4) (sycophancy). A když se ve vícekrokovém rozhovoru vydají špatným směrem, nedokážou chybu napravit – [studie Microsoftu a Salesforce z roku 2025](https://arxiv.org/abs/2505.06120) zjistila 39% pokles přesnosti napříč všemi modely při porovnání jednokolových a vícekolových konverzací.

**Nemají trvalou paměť.** Každá konverzace začíná od nuly. Inženýrské berličky (RAG, vektorové databáze, [paměťové frameworky](https://research.ibm.com/blog/memory-augmented-LLMs)) vytvářejí iluzi kontinuity, ale podkladová architektura je z podstaty bezstavová. Žádný současný systém nedokáže střádat zkušenosti v průběhu času tak, jako to dělá lidský expert během let praxe.

Tohle jsou reálná omezení. Ale než se začneme ptát, jestli jsou trvalá, stojí za to zpochybnit předpoklad, který leží pod většinou této debaty.

## Taky jste papoušek

„Stochastický papoušek“ je oblíbené hanlivé označení pro LLM – obvinění, že jen předpovídají nejpravděpodobnější další token a ve skutečnosti ničemu nerozumí. Má to být zdrcující kritika. Nastavme ale zrcadlo sami sobě.

Zamyslete se nad tím, co lidský mozek vlastně dělá. Je to biologická neuronová síť, která zpracovává vstupy a produkuje výstupy na základě vzorců naučených z dat. Architektura je jiná – trvalá paměť, emoční podmiňování, smyslové vnímání ukotvené v těle – ale základní mechanismus je stejný: rozpoznávání vzorců a vyvozování na základě pravděpodobnosti z nashromážděných zkušeností.

Své myšlenky si nevybíráte o nic víc, než si Claude vybírá své tokeny. Jak argumentuje Robert Sapolsky v knize [*Determined*](https://en.wikipedia.org/wiki/Determined:_A_Science_of_Life_Without_Free_Will), každé lidské rozhodnutí je nevyhnutelným produktem předchozích příčin – vaší genetiky, neurochemie a hlavně každé jediné zkušenosti, kterou jste kdy prožili, včetně těch, které jste ani vědomě nezaznamenali. V našem mozku nesedí žádný nezávislý hybatel, který by tahal za nitky. Je tam jen neuronová síť, která se nepřetržitě trénuje od narození.

Tohle není žádný okrajový názor. Je to logický důsledek současného poznání v neurovědě. Prožíváme něco, čemu říkáme „porozumění“, „intuice“ a „kreativita“, ale mohou to být jen subjektivní nálepky pro proces, který ve svém jádru dělá přesně to, z čeho jsou obviňovány LLM: sofistikované porovnávání vzorců nad nashromážděnými daty.

Pokud je vám ta představa nepříjemná, porovnejte si to vedle sebe:

|                   |Člověk                                                                                                |LLM                                                                             |
|-------------------|------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------|
|**Architektura**   |Biologická neuronová síť, ~86 miliard neuronů                                                        |Umělá neuronová síť, miliardy parametrů                                         |
|**Trénovací data** |Desítky let nepřetržitého multimodálního smyslového vstupu (zrak, sluch, hmat, čich, emoce, sociální zpětná vazba)|Převážně text, částečně obrázky                                                  |
|**Paměť**          |Trvalá, asociativní, podbarvená emocemi, konsolidovaná během spánku                                  |Bezstavová v rámci relace; paměť připojena externě                              |
|**Metoda tréninku**|Nepřetržitá, od narození, včetně nevědomých vstupů, reinforcement learning (dotknout se horkých kamen), supervised learning (zpětná vazba od rodičů)|Předtrénování na korpusu, doladění, RLHF                                        |
|**„Kreativita"**   |Rekombinace zkušeností, občas produkující něco skutečně nového                                        |Rekombinace trénovacích dat, občas produkující něco skutečně nového              |
|**„Intuice"**      |Komprimované rozpoznávání vzorců z let doménově specifické zkušenosti                                 |Zatím nedosaženo — chybí mechanismus pro dlouhodobou komprimaci zkušeností       |

Rozdíly jsou to významné. Ale všimněte si, jaké jsou povahy: jsou to rozdíly v *míře*, ne v *druhu*. Víc dat, bohatší typy dat, lepší architektura, trvalá paměť. To jsou inženýrské proměnné, ne metafyzické.

Čtyřleté dítě zpracovalo zhruba stejné množství surových smyslových dat, jako zpracovaly ty největší LLM ve formě textu – ale data toho dítěte jsou nepřetržitá, multimodální, zasazená do těla, spojená s emocemi a ukotvená v sociálním prostředí. Nejde o to, že by dítě mělo něco, co LLM nikdy mít nemůže. Jde o to, že dítě má nesrovnatelně bohatší trénovací data zpracovaná sofistikovanější architekturou v nepřerušovaném časovém rámci.

## Teze o dokumentovatelnosti

Tím se dostávám k tomu, co považuji za skutečnou otázku – ne „umí AI myslet?“, ale „dokážeme zachytit dostatek správných vstupů?“

Teze zní takto: **každý kognitivní proces vykonávaný člověkem je principiálně dokumentovatelný, pokud dostatečně zachytíme kontext, vstupy, pravidla a požadované výstupy. Překážky jsou praktické, ne teoretické.**

„Intuice“ výzkumníka ohledně toho, kterým směrem se vydat, není magie. Je to komprimovaný výsledek tisíců přečtených článků, stovek pozorovaných experimentů, desítek slepých uliček – to vše filtrováno skrze specifickou kognitivní architekturu a emocionální historii daného člověka. Kdybychom dokázali sledovat všechny tyto vstupy s dostatečnou přesností, tu intuici bychom dokázali zdokumentovat.

„Úsudek“ zkušeného manažera o obchodní příležitosti není žádná nepostižitelná kvalita. Je to rozpoznávání vzorců vybudované za desetiletí konkrétních transakcí, vyjednávání, výher a proher – usměrňované osobnostními rysy, které jsou samy o sobě produktem genetiky a výchovy.

„Cit“ mistra řemeslníka pro správný výsledek není mystický. Je to neuronová síť, která se léta trénovala ve velmi specifické smyslové doméně a zakódovala jemné vzorce pod prahem vědomí.

Nic z toho není teoreticky nezdokumentovatelné. Je to prostě těžké. A to těžké ve třech ohledech:

**Problém kontextu.** Dokumentace expertízy vyžaduje zachycení kontextu, který ji vytvořil. Intuice výzkumníka je produktem celé jeho profesní historie – a i té osobní, protože motivace, tolerance k riziku a estetické preference formují směr výzkumu. Retrospektivně sledovat něčí kontext od narození po současnost je prakticky nemožné. Ale prospektivně to nemožné není a i částečné zachycení má obrovskou hodnotu.

**Problém distribuce.** Tohle znám nejlépe z vlastní práce v IT. Znalosti potřebné pro jeden jediný proces jen zřídka sídlí v jedné hlavě. Jsou rozprostřené mezi více lidí v různých organizacích, z nichž každý drží úlomek a často si ani neuvědomuje, že ho drží. Nejtěžší na sběru požadavků není samotná dokumentace – je to jejich *„stažení“*: dostat to, co mají lidé mezi ušima, do formátu, který lze sdílet, ověřovat a prakticky využít.

**Problém nevědomého zpracování.** Velká část lidské expertízy pochází ze vstupů, které si vědomě neregistrujeme. Lékař, který zkrátka „ví“, že něco nesedí. Obchodník, který cítí, jak se trh mění. Nejsou to nadpřirozené schopnosti – jsou to výsledky skutečných smyslových dat zpracovávaných pod úrovní vědomého vnímání. Současné metody dokumentace tohle úplně míjejí, protože expert nedokáže popsat slovy to, k čemu nemá vědomý přístup.

## Filozofický přesah

Pokud přijmete tezi o dokumentovatelnosti, vede to k zajímavým a trochu znepokojivým závěrům.

Kdybych měl úplný záznam každého smyslového vstupu, který člověk od narození přijal – každý obraz, zvuk, dotek, sociální interakci, emocionální stav – a měl architekturu schopnou to zpracovat stejným způsobem jako jeho mozek, replikoval bych tím toho člověka? Ne kopii jeho znalostí, ale *jeho samotného*?

Myslím, že Sapolsky by řekl ano. Pokud je lidské poznání zcela produktem neuronální architektury plus souhrnu vstupů, pak je dokonalá simulace dokonalou replikou. Mimo tento výpočetní proces neexistuje žádné zbytkové „já“.

Tohle není jen myšlenkový experiment. Definuje to teoretický strop AI. Pokud je odpověď ano, pak je každé omezení AI inženýrským problémem – otázkou správných dat a správné architektury. Pokud je odpověď ne, pak existuje něco mimo výpočetní rámec, čemu zatím nerozumíme – říkejte tomu vědomí, svobodná vůle nebo něco, pro co zatím nemáme jméno.

K praktickým krokům nepotřebujeme tuto otázku vyřešit. Ale stojí za povšimnutí, že každé tvrzení typu „AI nikdy nedokáže…“ tiše předpokládá, že odpověď je ne. A důkazy pro tento předpoklad jsou slabší, než si většina lidí myslí.

## Co to znamená v praxi

K vytěžení ekonomické hodnoty dnes nepotřebujeme rozluštit záhady lidského vědomí. I když nedokážeme zachytit oněch 100 % potřebných k simulaci člověka, zachycení využitelných skrytých znalostí zásadně mění to, jak užitečná dokáže AI být i na dnešní úrovni „inteligence“.

Tady jsou podle mě hlavní implikace:

**Meta-dovedností éry AI je extrakce znalostí.** Ne prompt engineering. Ne schopnost „naučit se používat AI nástroje.“ Úzkým hrdlem už není samotná AI – je to naše schopnost dostat z hlav lidí to, co vědí, a zakódovat to do formy, se kterou dokážou stroje pracovat. Výzkum ukazuje, že experti při spontánním předávání znalostí [opominou 40–70 % klíčových rozhodovacích kroků](https://www.modsimworld.org/papers/2025/MODSIM_2025_paper_11.pdf), pokud se nepoužijí strukturované metody vytěžování znalostí. Už v roce 1966 Michael Polanyi zjistil, že [„víme víc, než dokážeme říct“](https://en.wikipedia.org/wiki/Polanyi%27s_paradox). Nic z toho není problém AI. Je to problém zachycení a mezilidského přenosu znalostí, který tu byl dávno před AI – umělá inteligence z něj jen udělala kritické omezení.

**Pokud jste expert, dokumentujte své myšlení teď hned.** Nejen co děláte, ale i proč to děláte. Jaké alternativy jste zvážili a zamítli. Jaké okrajové případy řešíte, aniž byste o nich vůbec přemýšleli. Jaké jemné signály mění váš přístup. Tahle „meta-kognitivní dokumentace“ je ten nejúčinnější nástroj, který většina profesionálů opomíjí. Nemusíte se stát expertem na AI. Musíte se stát [expertem na vysvětlování vlastní expertízy](https://medium.com/@shashwatabhattacharjee9/the-uncodifiable-advantage-tacit-knowledge-as-the-strategic-bottleneck-in-ai-systems-d359dfe3967b).

**Na formátu reprezentace obrovsky záleží.** Přirozený jazyk je jeden ze způsobů kódování znalostí, ale nemusí být ten nejlepší. Kód zachycuje procedurální logiku mnohem přesněji. Doménově specifické jazyky (chemické vzorce, hudební notace, matematická notace) kódují specializované znalosti ve formátech, které jsou čitelné jak pro lidi, tak snadno strojově zpracovatelné. Otázka *jak* reprezentovat zdokumentovanou expertízu je designový problém, který je zatím sotva prozkoumaný.

**Arthur C. Clarke předpověděl, že trénování skutečně lidské inteligence zabere desetiletí.** Myslím, že měl pravdu. Výpočetní výkon existuje, nebo brzy bude existovat. Co nám chybí, jsou desetiletí zachycených lidských zkušeností – ta bohatá, multimodální, nepřetržitá trénovací data, která přijímá lidský mozek a která dnes žádný AI systém nedostává. Cesta k umělé inteligenci na lidské úrovni není omezena výpočetním výkonem. Je omezena schopností zachytávat data.

## Dočasná kategorie

Pokud je teze o dokumentovatelnosti správná – pokud je každý lidský kognitivní proces zdokumentovatelný za předpokladu dostatku dat – pak „unikátně lidské“ vlastnosti nepředstavují trvalou kategorii. Je to jen dočasná kategorie, definovaná současnými limity naší schopnosti zachytit a zakódovat zkušenost.

Věci, které dnes označujeme za unikátně lidské – kreativita, intuice, úsudek, empatie – jsou takové možná jen proto, že jsme zatím nevybudovali systémy schopné zachytit vstupy, které je produkují, a architektury, které by je zpracovaly. Nejsme výjimeční svou podstatou. Jsme výjimeční tím, kolik dat jsme dokázali vstřebat a jak dlouho je už zpracováváme.

Dobrou zprávou je, že to ukazuje jasnou cestu vpřed, i když bude ještě dlouhá. A mezitím – což může trvat desetiletí – je tou nejcennější prací stát se tím, kdo tuto propast přemosťuje: někým, kdo dokáže vzít znalosti z lidských hlav a zpřístupnit je strojům. Ne proto, že by to snižovalo hodnotu lidské expertízy, ale proto, že je to jediný způsob, jak ji škálovat.

Celoživotní zkušenost experta by neměla zemřít spolu s ním, ani by se neměla vytratit ve chvíli, kdy odejde do důchodu. Měla by být zachycena, zakódována a předána dál. To není ohrožení lidské hodnoty. Je to její nejvyšší vyjádření.
