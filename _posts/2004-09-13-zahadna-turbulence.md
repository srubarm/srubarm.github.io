---
layout: post
title: Záhadná turbulence
categories: [Fyzika]
permalink: /fyzika/zahadna-turbulence.html
---
# Záhadná turbulence

Turbulenci zná každý, ale nikdo jí nerozumí. Vidíme ji, když si myjeme ruce, houpe nás, když sedíme v letadle a je všude kolem nás. Problémem je, že nikdo nedokáže předvídat, jak se bude chovat.

## Klasická teorie víření nezná

<div class="obry"><div class="leftbox"><img alt="Turbulentní proudění způsobující indukovaný odpor křídla" height="152" src="http://www.techblog.cz/images/turbulence-indukovany-odpor.jpg" width="150"/></div></div> 

Klasické teorie proudění předpokládají, že např. proud tekutiny (vzduchu/kapaliny) v trubce zůstává hladký (tzv. laminární) nezávisle na tom, jak rychle je tekutina trubkou pohybuje. To samozřejmě není pravda. Turbulentnost proudění se mění jak rychlostí toku, tak s velikostí "zúčastněných" (v tomto případě zrovna průměr, či spíše světlost, trubky). Obrovský vliv na ni má tvar a kvalita povrchu obtékaného prostředí. Tudíž je nemožné vytvořit soustavu potrubí, kde by nebyla žádná turbulence. A turbulence (tj. vířivé proudění) znamená ztráty.

## Nestabilní výsledky jsou správné – mohou za to vlny

<div class="obryleft"><div class="leftbox"><img alt="Porovnání teoretických a naměřených hodnot proudění" height="95" src="http://www.techblog.cz/images/turbulence-porovnani.jpg" width="150"/></div></div> 

Nejnovější teorie už s vířivým prouděním počítají. Pro [jejich ověření](http://physicsweb.org/article/news/8/9/6/1) vědci sestrojili [aparaturu](http://physicsweb.org/box/news/8/9/6/040906) s 26 m dlouhou trubkou, ve které proudí voda. U jejího počátku vstřikovali paprsek vody do trubky kolmo k protékající kapalině a vytvářeli tak turbulenci. O dále v různých vzdálenostech sledovali, jak se turbulence vyvíjí. Dělali to tak, že měřili směr a rychlost proudění kapaliny v trubce v jejím průřezu pomocí laseru. Naměřené hodnoty porovnali s teoreticky vypočtenými. I vy se můžete podívat (nahoře naměřené a dole vypočtené proudění), že [si velmi dobře odpovídají](http://physicsweb.org/box/news/8/9/6/0409061).

Nová teorie pracuje s tlakovými vlnami, které se nerovnoměrně šíří tekutinou a tím způsobují přenos a rozvoj turbulence. Proto pohybové rovnice kapaliny v trubce mají nestabilní řešení, čili ~~zadání a rovnice je stále stejná, ale pokaždé vám vyjde něco trochu jiného.~~ malá změna ve vstupních datech způsobí velkou změnu ve výsledku. Je to stejný případ jako u [předpovídání počasí](http://www.techblog.cz/veda/predpovidani-pocasi.html).

Tento výzkum je skutečně velmi zajímavý, už proto, že turbulence je všude a nemusí být vždy jen negativní. Na křídlech letadel bývají tzv. turbulátory, které ji uměle vyvolávají a třeba takový čmelák ji vděčí za to, že může létat.

Myslím, že o turbulenci se na Techblogu ještě zmíním a to už do toho zkusím zamotat nějaké to Reynoldsovo číslo.


<section id='comments-section'>
<div class='commentsheader'>Komentáře</div>        
<div class='comment-item-header' markdown=1>
[Pavel](mailto:ja@tady.cz)  &ndash; 15.9.2004
</div>

Nedá mi to, musím článku vytknout jednu podstatnou chybu (která možná vznila příličným zjednodušením). Rovnice pro pohyb kapaliny mají nestabilní řešení, ale to neznamená, že při stejném zadaní dají různé výsledky. Při stejném zadání vyjde samozřejmě totéž. Problém je v tom, že už nepatrná změna zadání může způsobit velkou změnu ve výsledku - to je (zjednodušeně) definice nestabilního řešení. A ta nepatrná změna může být i různé zaokrouhlení při numerickýách výpočtech. Z toho možná vyplynulo původní tvrzení, že při stejném zadání vyjdou různé výsledky.

<div class='comment-item-header' markdown=1>
Martin &ndash; [WWW](http://techblog.srubar.net/) &ndash; 15.9.2004
</div>

Děkuji za opravu. Bohužel tato chyba nevznikla z přílišného zjednodušení, ale z toho, že jsem si nevzpoměl na hodiny numerické matematiky. :-) A tak jsem si dokonce myslel, že výsledkem zmiňovaných rovnic bude dokonce nějaká periodická funkce času.Ale jakto, že jim nakonec vypočet dobře odpovídá s naměřenými hodnotami? U takového nestabilního řešení by to měla být spíše náhoda.

<div class='comment-item-header' markdown=1>
[Alex](mailto:zephir@atlas.cz)  &ndash; 25.12.2004
</div>

Simulovat turbulenci s dnešními počítači není příliš obtížné a omezeném souboru dat má zcela deterministický průběh.http://193.85.233.106/home/SRNKA/fluid.htm

<div class='comment-item-header' markdown=1>
Martin &ndash; [WWW](http://techblog.srubar.net) &ndash; 26.12.2004
</div>

Díky za doplnění. Jenže v podmínkách praxe rozhodně nemáme omezený soubor dat a těžko postihneme kompletně podmínky, ve kterých proudění probíhá. Ale je pravda, že v tomto modelovém případě to mohli všechno zahrnout do výpočtového modelu, takže ten jejích výpočet nemusí být až takovým úspěchem.

</section>