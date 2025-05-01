---
layout: post
title: Proč webdesigneři nepoužívají CSS
categories: [Osobní]
permalink: /osobni/proc-webdesigneri-nepouzivaji-css.html
---
# Proč webdesigneři nepoužívají CSS

Nejsem sice webdesigner, ale velmi mě zaujal spot na Acidlogu [Prečo webdesigneri nepoužívajú CSS](http://acidlog.fczbkk.com/blog.php?entry=1047392314). Tento článek rozděluje webdesigery na dva druhy: grafiky a kodery. Grafici mají sice grafické cítění, ale neovládají CSS a u koderů je to naopak. Grafici si tudíž při pohledu na stránky vytvořené kodery myslí, že CSS nelze použít k napsání graficky zajímavých stránek.

Ale jedna věc podle mě v čistém CSS nejde, a to nastavit délku jednoho nebo více sloupců tak, aby jejich výška odpovídala výšce nejdelšího sloupce, který je na stránce. Typické použití by bylo na vícesloupcovém layoutu Techblogu. Takhle mám nastavenu výšku sloupců napevno. Ale budu rád, vyvedete-li mě z omylu.


<section id='comments-section'>
<div class='commentsheader'>Komentáře</div>        
<div class='comment-item-header' markdown=1>
[Slávek Pecina](mailto:magic@pecomp.cz) &ndash; [WWW](http://p-cut.com/) &ndash; 31.1.2007
</div>

předpokládám, že jste odpověď již mezitím našel, například na pixyho stránkách, nicméně mohu to zopakovat i zde , vytvoření například třísloupcového pružného layoutu s y-repeat podklady a "stejnou výškou" sloupců je jednoduchá záležitost počítejte se mnou div id hlavni / h1 span --hlavičkadiv id obal (float left, 70procent)-- poslouží nám jako kontejner pro obsah a levý sloupecdiv id obsah (float right 60procent)div id levy (float right 40procent)uzavreme div obal a pridame jeste pravy sloupec iv id pravy (float left, 30procent)nasleduje hr cleaner ktera nam tlaci paticku a natahuje celkove stranku tj. div hlavniposledni div je id pata vsimnete si jedne veci , mame dva kontejnery , jeden obaluje celou stranku druhy obsahovy a levy sloupec - k nicemu jinemu nez k udrzeni velikosti nam zatim neslouzi , problem je , ze div obal se bude roztahovat na vysku nezavisle na sloupci pravem, takze ... kolik mame divu ?hlavni/obal/obsah/levy/pravy/pata = 6 to prece neni zle , pata muze byt resena pomoci odstavce a div obal je pouzit jen proto, abychom dostali div obsah tesne za h1 span (cili kvuli SEO)cili stacily by i 4 divy http://p-cut.com/ coz na trisloupcovy layout neni rozhodne mnoho :)) ... k jadru pudla: staci nam pridat jediny div ktery bude plnit funkci obalu a tomuto pridelime pozadi s opakovanim v y ose zarovnano doprava , tim mame z krku pravy sloupec , pridanim pozadi s opakovanim v y ose zarovnano doleva u divu hlavni ziskame pozadi pro levy sloupec a tim je cely problem vyresen , tyto bloky se vzdy roztahnou pres celou vysku. Vice divu jiz neni treba pokud se uzivaji marginy a paddingy a cely obsah tvorite elementy jez prislusi spravnemu strukturovani dokumentu, muze pribyt nejaky ten div s absolutni pozici (vetsinou prave na nejakou tu grafickou serepeticku)nerekl bych ze s dobrou znalosti css nejdou delat pohledne weby, pokud ale webdesigner uvazuje komplexne (cili i nad SEO a timpadem poctem objektu velikosti obrazku atp.) pak i celou konstrukci co nejvice zjednodusuje.Se zjednodusovanim to je zbytecne nejak extremne prehanet, pokud se budete pohybovat v radu do 10ti divu , meli byste zkonstruovat prakticky cokoli.Otazkou tak nejspis i do budoucna zustane uvazeni ucelu webu a zvoleni te spravne cesty, kazdopadne na pouzitelny a pristupny web si kazdy casem zvykne a nauci se ocenovat jeho prednosti (prestoze neni koder :) )

</section>