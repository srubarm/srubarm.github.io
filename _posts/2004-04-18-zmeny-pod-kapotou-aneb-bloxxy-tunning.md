---
layout: post
title: Změny pod kapotou aneb Bloxxy tunning
categories: [Osobní]
permalink: /osobni/zmeny-pod-kapotou-aneb-bloxxy-tunning.html
---
# Změny pod kapotou aneb Bloxxy tunning

Jelikož vývoj Bloxxy byl bohužel ukončen a já jsem už od začátku ledna čekal na SEO odkazy, rozhodnul jsem se, že se do toho pustím sám, bez jakékoliv předchozí znalosti PHP. Výsledek s mnoha dalšími funkcemi a vylepšeními naleznete na Techblogu. Zmínil bych navíc navigaci "starší-novější příspěvek" u trvalých odkazů jednotlivých spotů, velmi uživatelsky přívětivý obsah celkových [archívů rubrik](http://www.techblog.cz/archiv.html) a seznam starších článků na konci stránek rubrik i titulní stránky.

Tuto upravenou verzi Bloxxy bych rád co nejdříve uvedl do stavu, kdy by byla vhodná k rozšíření. Teď to zcela určitě není možné. Je příliš napasována na mé potřeby a má několik nedodělků a problémů. Její největší vadou je pomalost při přeregenerování celé rubriky nebo dokonce všech rubrik, takže velmi často vyprší maximální čas přidělený serverem pro vykonání skriptu. BTW vy, kteří umíte programovat a znáte Bloxxy, nevíte, co je tou "nejvíce brzdící" částí skriptu?

Touto úpravou se IMHO z Bloxxy stal navenek velmi kvalitní systém s mnoha funkcemi postačující k vedení docela luxusního blogu.
  *[SEO odkazy]: Odkazy vypovídající o obsahu stránky
  *[PHP]: PHP Hypertext Preprocesor
  *[IMHO]: Dle mého skromného názoru


<section id='comments-section'>
<div class='commentsheader'>Komentáře</div>        
<div class='comment-item-header' markdown=1>
Martin - Techblog  &ndash; 18.4.2004
</div>

Test

<div class='comment-item-header' markdown=1>
Jan Bien &ndash; [WWW](http://www.mraveniste.org/) &ndash; 19.4.2004
</div>

Myslím, že největším problémem jsou regulární výrazy. Ale kde je přesně problém, to Ti bez znalosti Tvého řešení neřeknu.

<div class='comment-item-header' markdown=1>
Martin - Techblog &ndash; [WWW](http://techblog.srubar.net/) &ndash; 19.4.2004
</div>

Díky, taky mě to napadlo už jsem ty nepoužívané ořezal, ale právě reg. výrazy používám (ve fci tuším getAutotitle) pro generování názvů stránek, takže se často používá, ale zkusím to trochu upravit.

<div class='comment-item-header' markdown=1>
pavelm &ndash; [WWW](http://pavelm.net) &ndash; 19.4.2004
</div>

Přeji hodně úspěchů při tunningu. Už jsem zvědav na výsledek. Jinak také jsem trochu upravoval, nebo spíš rozšiřoval funkčnost o vyhledávání. Moje řešení ale není úplně dokonalé. Prostě jsem se s tím pak už nechtěl... :)Já se zas v poslední době chystal naprogramovat si  zvášť skript, který bych si vždy třeba jednou za půl hodiny spouštěl přes Cron a nechal bych si na hlavní stránku vkládat odkazy na nejnovější články z vybraných zdrojů - takový soukromý blogportál. Zatím ale vítězí lenost. :/[2] Sám jsem nedávno přecházel z Bloxxy 0.5b na 0.63b - hlavně kvůli lépe řešeným komentářům (ty adresy u 0.5b byly prostě šílenost. Nevím jak je to možné, ale přegenerování mi teď trvá o DOST delší dobu než s verzí 0.5b. Zatím jsem to ale nijak neřešil.

<div class='comment-item-header' markdown=1>
Martin - Techblog &ndash; [WWW](http://techblog.srubar.net/) &ndash; 19.4.2004
</div>

[4] Tvé komentáře už mám připravené ke spuštění (viz zdroj), ale zapomněl jsem, že Ty tam nějakým způsobem generuješ i odkazy na stránky s hledaným slovem, takže to u mě nefunguje a budu to muset trochu poupravit (nebude-li Ti to vadit).

<div class='comment-item-header' markdown=1>
Miroslav Navrátil &ndash; [WWW](http://kanevinternetu.blacksuns.net/weblog) &ndash; 20.4.2004
</div>

Jelikož jsem líný si do bloxxy cokoliv programovat, tak si programuju systém vlastní - nedokonalý, ale lepší než Bloxxy. I s fulltextem a komentáři :) akorát nevím, jestli udělám seo odkazy.

<div class='comment-item-header' markdown=1>
llook &ndash; [WWW](http://llook.wz.cz/weblog/) &ndash; 8.5.2004
</div>

Co jsem koukal do bloxxy na publikování, tak mě docela zaráží, jak často používá ereg_replace namísto str_replace.Co se týče autotitlu, možná by šlo text rozdělit na řádky a pak hledat řádek po řádku první nadpis.Zhruba nějak takhle:$line = strtok ($_POST['itemtext'], "\n");while ($line){  if (($pos = strpos($line, ': ')) <== 3)  {    $istitle = true;    for ($i=0; $i<$pos; $i++)      if ($line[$i] != ':')        $istitle = false;    if ($istitle)    {      $titlearray = explode(' ', $line, 1);      $title = $titlearray[1]      break;    }  }  $line = strtok ("\n");}Ale nevim, jestli by nebyly rychlejší ty regulární výrazy.Každopádně by bylo možné vymyslet spoustu jiných možností, jak nahradit reg. výrazy.

</section>