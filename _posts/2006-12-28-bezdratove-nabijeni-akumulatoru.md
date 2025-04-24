---
layout: post
title: Bezdrátové nabíjení akumulátorů
categories: [Technologie]
permalink: /technologie/bezdratove-nabijeni-akumulatoru.html
---
# Bezdrátové nabíjení akumulátorů

Představte si, že k vašemu notebooku na stole nevedou žádné dráty, a přesto můžete pracovat libovolně dlouho. Co je to nabíjení mobilu? Na to už jste dávno zapomněli. Taková je vize pohánění elektroniky budoucnosti. Toužíme po tom všichni. Jak toho dosáhnout? Způsoby bezdrátového přenosu elektrické energie jsou známé, ale ne vždy vhodné pro tento účel.

## Bezdrátové nabíjení s problémy

<div class="obry" style="width:167px"><div class="leftbox"><img alt="NiMH akumulátory" height="200" src="http://www.techblog.cz/images/bezdratove-nabijeni-akumulatory.jpg" width="150"/></div></div> 

Technologie bezdrátového přenosu energie jsou známy již velmi dlouho. Jsou to zejména přenos elektromagnetickou indukcí nebo elektromagnetickými vlnami. Nesou s sebou však problémy. Pokud mají pracovat na velkou vzdálenost, stávají se výrazně méně efektivní a zároveň jejich okolí není zrovna příznivé k dlouhodobému pobytu živých organizmů. Nový způsob využívající tlumených elektromagnetických vln zatím nebyl prakticky otestován.

## Elektromagnetická indukce

[Elektromagnetická indukce](http://en.wikipedia.org/wiki/Electromagnetic_induction) je zcela nejběžnější způsob bezdrátového přenosu, ale i přeměny elektrické energie vůbec. Používá se ve velké elektroenergetice – od generátoru v elektrárně přes transformátory až po nabíječky na mobil. Několik zařízení pro bezdrátové nabíjení indukci také využívá, ovšem ne zrovna efektivně. Telefon, PDA nebo cokoliv chceme nabíjet se přiloží k desce a nabíjí se. nepotřebujeme konektor a drát, ale elektronika řídící nabíjení je složitější, přenos indukcí neefektivní. Jedná se v podstatě o transformátor bez železného jádra. A v tom je problém – jádro běžného transformátoru v sobě uzavírá magnetický tok, a tak výrazně snižuje ztráty. Má-li být zařízení odnímatelné, toto možné není, a účinnost tedy klesá.

<div class="obryleft" style="width:187px"><div class="leftbox"><img alt="Schematický nákres cívky vytvířející ve svém okolí magnetické pole" height="72" src="http://www.techblog.cz/images/prenos-energie-civka.gif" width="170"/></div>Schematický nákres cívky vytvářející ve svém okolí magnetické pole</div> 

Zásadním problémem je, že indukci nelze použít pro přenos na větší vzdálenosti. Ne že by tomu bránily nějaké fyzikální principy, ale pro člověka není dobré se dlouhodobě pohybovat v intenzivním elektromagnetickém poli. Některé lékařské studie zjistily, že lidé bydlící v okolí do půl kilometru od vedení velmi vysokého napětí jsou vystaveni několikanásobně vyššímu riziku vzniku leukémie než lidé bydlící dále. I když byl výzkum různě zpochybňován, minimálně z psychologického hlediska tento způsob není k dálkovému nabíjení vhodný. Proměnné elektrické pole by také indukovalo proud v každé smyčce z vodivého materiálu, čímž by znemožnilo funkci jakéhokoliv dalšího zařízení v dosahu bezdrátové nabíječky. Evidentně tudy cesta nevede.

## Elektromagnetické vlny

<div class="obry" style="width:187px"><div class="leftbox"><img alt="Modrý laser" height="115" src="http://www.techblog.cz/images/bezdratovy-prenos-energie-laser.jpg" width="170"/></div>Laserem je možné přenášet velké množství energie</div> 

Opět běžně používaný způsob přenosu energie. Nejběžnější [laser](http://cs.wikipedia.org/wiki/Laser) a [mikrovlny](http://en.wikipedia.org/wiki/Microwave) vidíme všude kolem sebe. Laser tvoří elektromagnetické vlny nízké vlnové délce obvykle z oblasti viditelného světla. Vzhledem k principu fungování laseru se energie přenáší ve velmi úzkém paprsku. To je na jednu stranu dobře, ale na druhou to vyžaduje přímou viditelnost mezi zdrojem a příjemcem, což je pro předpokládané použití zcela nevhodné. Navíc transformace elektrické energie na laserové světlo a zpět je velice neefektivní. Kolečko elektřina – laser – elektřina má účinnost 1 až 5 %. Nic moc. Tudy také ne.

O něco slibněji se jeví mikrovlny. Tytéž mikrovlny, které v troubě ohřejí cokoliv od pizzy po mokrou kočku. Lze je snadno a efektivně generovat a dokonce s pomocí [rektifikační antény](http://en.wikipedia.org/wiki/Rectenna) zachycovat a přímo měnit na elektřinu s účinností až 90 %. Avšak jak už případ s kočkou, která se v mikrovlnce upekla, místo aby se usušila, ukázal, lidem by mikrovlnné záření neprospívalo.

Takže jak tedy můžeme přenášet efektivně a bezpečně elektrickou energii bez drátů?

## Přenos tlumenými vlnami

<div class="obry" style="width:187px"><div class="leftbox"><img alt="Červeno modrá plocha se dvěmi body uprostřed" height="119" src="http://www.techblog.cz/images/bezdratovy-prenos-energie-vysledek-simulace.jpg" width="170"/></div>Výsledek numerického modelování přenosu energie tlumenými vlnami</div> 

Energii lze přenášet také [tlumenými elektromagnetickými vlnami](http://en.wikipedia.org/wiki/Evanescent_waves). Vědci nedávno přišli na to, jak využít nezářivého elektromagnetického pole, které tvoří tlumené elektromagnetické vlny. Vytvářené pole by mělo být netečné ke všemu ve svém okolí kromě speciálních přijímačů z dielektrika (nevodivého materiálu), které s vytvářeným polem rezonují, vytvářejí běžné elektromagnetické vlny, které se poté opět rektifikují, a tak přímo mění na elektrické napětí. Bohužel tomuto jevu nijak nerozumím, takže lepší vysvětlení podat nedokáži. Zajímají-li vás tlumené vlny více, můžete si přečíst články na Wikipedii [Evanescent wave coupling](http://en.wikipedia.org/wiki/Evanescent_wave_coupling) a příslušnou část článků [Wireless energy transfer](http://en.wikipedia.org/wiki/Wireless_energy_transfer#Evanescent_wave_coupling).

Tento perspektivní způsob přenosu by měl být schopný vysílat energii až do vzdálenosti pěti metrů bez sebemenších problémů. Všechno, co bylo zjištěno, bylo pouze vypočítáno. Experimenty ověřující praktické výkony a chování v běžných podmínkách ještě neproběhly.

## Svět bez drátů

Ač žádné z uvedených technologií zatím nemá praktické využití, vývoj a zejména poptávka uživatelů nutí firmy se bezdrátovými přenosy energie, ale i dat intenzivně zabývat. V budoucnu bude běžné, že v místnostech bude univerzální dálkový zdroj energie pro všechna zařízení s malou spotřebou, a dojde tak k pročištění "zadrátovaných" domácností a firem. V blízké budoucnosti se bude jednat zejména o věci, u nichž je nabíjení skutečně otravné – mobily, notebooky, PDA. To jsou zařízení, u kterých bychom byli nejraději, kdyby fungovaly samy o sobě bez toho, aniž bychom se o cokoliv museli starat. Rozšíření pro další použití závisí na efektivitě bezdrátového přenosu elektrické energie.

<div class="obryleft" style="width:167px"><div class="leftbox"><img alt="PDA" height="184" src="http://www.techblog.cz/images/pda-nabijeni-bez-dratu.jpg" width="150"/></div>Budeme někdy moci nabíjet PDA bez drátů?</div> 

Doprava ve městech by se obešla bez trolejového vedení a místo toho by pouze byly zářiče pod povrchem. Při opravdu velkém dosahu by i letadla mohla být poháněna vzdáleným zdrojem energie a co teprve kosmické lodě? To už začíná být zajímavé. Cena dopravy nákladu na oběžnou dráhu by tak mohla být mnohem jednodušší i levnější. To už jsme od nabíjení mobilů hodně vzdáleni. Každopádně považuji vyřešení efektivního přenosu energie bez drátů na větší vzdálenosti za věc, kterou firmy i vědci řešit chtějí, a tudíž ji i brzy vyřeší.

## Další zdroje informací

  * [Wireless energy could power consumer, industrial electronics](http://web.mit.edu/newsoffice/2006/wireless.html) – tisková zpráva MIT
  * [Gadget recharging goes wireless](http://physicsweb.org/articles/news/10/11/12/1) – článek na PhysicsWeb.org
  * [Wireless energy could power consumer, industrial electronics](http://www.physorg.com/news82754873.html) – článek na Physorg.com
  * [Wireless Non-Radiative Energy Transfer](http://arxiv.org/abs/physics/0611063) – vědecká zpráva popisující výpočtové zkoumání dálkového přenosu energie pomocí tlumených vln



