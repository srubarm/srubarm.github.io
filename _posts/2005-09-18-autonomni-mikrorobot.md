---
layout: post
title: Autonomní mikrorobot
categories: [Nano]
permalink: /nano/autonomni-mikrorobot.html
---
# Autonomní mikrorobot

Stále se snažíme vytvořit roboty, které by byly nezávislé na vnějších zdrojích energie, mohly by se volně pohybovat a my bychom je mohli na dálku ovládat. Nyní se podařilo sestrojit mikrorobota, který tyto požadavky splňuje. Zbývá již jen jeden krok k tomu, abychom realizovali vizi nanobotů, které by autonomně manipulovaly s jednotlivými molekulami.

## Robot se pohybuje jako housenka

<div class="obry" style="width:197px"><div class="leftbox"><a href="http://www.techblog.cz/images/mikrorobot-deska.jpg"><img alt="Mikrorobot na speciální desce" height="135" src="http://www.techblog.cz/images/mikrorobot-deska-nahled.jpg" width="180"/></a><a href="http://www.techblog.cz/images/mikrorobot-deska.jpg"></a></div>Zvětšit<br/>Mikrorobot na speciální desce<br/>Credit: Bruce Donald, Dartmouth College</div> 

Mikrorobot se nepohybuje tak, jak bychom možná čekali – na kolečkách, pásech či nožkách, ale obdobně jako housenka prohýbáním svého těla. Jeho rozměry jsou 60 krát 250 mikrometrů. Je schopen pohybu dopředu a zatáčení. Plazí se rychlostí 50 µm/s, což znamená, že za minutu urazí 3 mm. Vzhledem malosti mikrorobota to není špatné, protože kdybychom rychlost vztáhli na velikost, jednometrový robot by "ušel" 50 metrů za minutu. Nejmenší poloměr zatáčení vědci naměřili 162 µm.

<div class="obryleft" style="width:187px"><div class="leftbox"><a href="http://www.techblog.cz/images/mikrorobot-pohyb-princip.gif"><img alt="Ilustrace principu pohybu robota" height="200" src="http://www.techblog.cz/images/mikrorobot-pohyb-princip-nahled.gif" width="170"/></a></div><a href="http://www.techblog.cz/images/mikrorobot-pohyb-princip.gif">Zvětšit</a><br/>Ilustrace principu pohybu robota<br/>Credit: Bruce Donald, Dartmouth College</div> 

Samotný vznik dopředného pohybu ilustruje obrázek. Robot se neprohýbá na délku, jak by se zdálo přirozenější, ale na šířku. Jako zdroj energie slouží elektrické napětí, které si robot bere z podložky, po které se pohybuje. Tady se dostáváme ke zmíněné autonomii. Mikrorobot je autonomní pouze na desce, která mu energii dodává. Mimo ni je to pouze mrtvá hmota. Prohnutí destičky robota a její přilepení k podkladové desce docílíme tak, že na destičku přivedeme záporný náboj a na desku po které se pohybuje náboj kladný. A jak mikrorobot zatáčí? Na to má protáhlé rameno s kolečkem na konci. Když chce zatočit "zapíchne" (stejným principem jako se prohýbá destička) rameno do desky, takže je nepohyblivé, a pokračuje v "chůzi". Tím je dáno další omezení, že zatáčet může pouze v jednom směru. Chce-li zatočit na druhou stranu, musí se přetočit o 270° navíc.

## Konstrukce a ovládání

Mikrorobot je zkonstruován z materiálů, které se prohnou, když na ně přivedeme elektrický proud. Uspořádání kontaktů na spodní straně robota a základní desky pokrytá elektrodami zajišťuje, že mikrorobot má v každé poloze přívod energie. Elektrické napětí z desky zároveň robota ovládá. Pulzy nižšího napětí prohýbají destičku způsobující dopředný pohyb a pulzy vyššího napětí "zabodávají" rameno pro zatáčení. Všechno se to odehrává docela rychle. Základní pulzy pohybující s mikrorobotem mají frekvenci 4 kHz – destička se tedy prohýbá 4 tisíckrát za sekundu.

## Uplatnění v praxi

<div class="obry" style="width:187px"><div class="leftbox"><a href="http://www.techblog.cz/images/mikrorobot-rameno-zataceni.jpg"><img alt="Detail ramene pro zatáčení" height="131" src="http://www.techblog.cz/images/mikrorobot-rameno-zataceni-nahled.jpg" width="170"/></a></div><a href="http://www.techblog.cz/images/mikrorobot-rameno-zataceni.jpg">Zvětšit</a><br/>Detail ramene pro zatáčení<br/>Credit: Bruce Donald, Dartmouth College</div> 

Vědci předpokládají, že mikroroboti naleznou uplatnění ve zkoumání nebezpečného prostředí, kontrole složitých zařízení nebo dokonce budou manipulovat s buňkami a tkáněmi v našem těle. Avšak tento robot nic takového nedokáže. Jeho jedinou schopností je to, že se umí pohybovat po speciální desce. Už jen princip, že pro jeho pohyb je nutné speciální prostředí je zcela špatný. Je nesmyslné, aby se robot mohl pohybovat po omezeném prostoru, protože tak ztrácí svou jedinou výhodu. Může jej nahradit jakékoliv zařízení jezdící po lanku či kolejničkách. Jestli by se podařilo zajistit bezkontaktní dodávku energie, měli bychom napůl vyhráno. Ale zmiňovaný mechanizmus "chůze" je vhodný jedině pro kvalitní povrchy. Na zaprášené betonové podlaze by se mikrorobot ani nehnul. Čeká nás dlouhá cesta k miniaturizovaným strojům, které by byly schopné něco užitečného dělat, ale když už je sestrojíme, další zmenšování už nebude příliš problematické. A potom už jsme pouze krok od manipulace s jednotlivými molekulami.

## Další informace

  * [Dartmouth researchers build world's smallest mobile robot](http://www.dartmouth.edu/~news/releases/2005/09/14.html) (14. 9. 2005) – Docela nezajímavá tisková zpráva k mikrorobotovi
  * [An Untethered, Electrostatic, Globally-Controllable MEMS Micro-Robot](http://www.cs.dartmouth.edu/brd/4/jmems05/donald-jmems05.pdf) PDF 18,5 MB – Kompletní informace o výzkumu mikrorobotů tohoto typu
  * [Stránka s videy pohybu mikrorobotů](http://www.cs.dartmouth.edu/reports/TR2005-553.CD/index.html)



