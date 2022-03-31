---
title: VIZUALIZACE PROSTOROVÝCH DAT - CHAOS V DIMENZÍCH
authors: Radek Dušek, Jakub Miřijovský
year: 2009
---
URL:  https://geografie.cz/media/pdf/geo_2009114030169.pdf, [Dušek and Miřijovský - VIZUALIZACE PROSTOROVÝCH DAT CHAOS V DIMENZÍCH.pdf](file:///C:/Users/horin/Zotero/storage/9MHY9DG5/Du%C5%A1ek%20and%20Mi%C5%99ijovsk%C3%BD%20-%20VIZUALIZACE%20PROSTOROV%C3%9DCH%20DAT%20CHAOS%20V%20DIMENZ%C3%8DCH.pdf)
ZOTERO: [See in Zotero](zotero://select/items/@dusekVIZUALIZACEPROSTOROVUCHDAT)
STATUS: #3D
TAGS: [[3D vizualizace]] 
# VIZUALIZACE PROSTOROVÝCH DAT: CHAOS V DIMENZÍCH
## Abstrakt
Clarification of common terminology for 3D. Perspective projections is not 3D view. 
## Úvod
Zabývá se polohou bodu ve smyslu X, Y, Z souřadnic - neřeší dimenze čas, aj.

Digitální modely terénu [[DMR]] jsou vytvářeny z trojrozměrných dat, tudíž je možné je považovat za 3D modely. Otázka je zdali následnou vizualizaci je také možné považovat za 3D. Při tvorbě mapy je nutné vypustit jednu dimenzi. Metody pro vyjádření této dimenze (často výšky) pak jsou vrstevnice, kóty aj. Pro vytvoření dojmu prostoru se používají stereoskopy, anaglyfy, stínování. 

Jaké metody vizualizace je možné považovat za 3D?

## Kapitola 1 - Prostorové vnímání
%%Dodelat zettle o vnímání%%
Obraz na sítnici je dvourozměrný. Pro zpracování vjemů mozek využívá *monokulární* a *binokulární* vodítka. Monokulární vodítka (relativní velikost, lineární perspektiva, překrývání, stínování, vzdušná perspektiva aj.) umožňují interpretovat prostor za "normální situace". Binokulární jsou založena na pozorování oběma očima - ze dvou různých míst - umožňuje vytváření umělých stereoskopických modelů.
## Kapitola 2 - Historie zobrazování prostorových dat
- Kroucená perspektiva - zvíře na kresleno z profilu, nohy čelně
- Egyptské kresby jako pravoúhlé průměty
- První kresby s lineární perspektivou v období antiky
- Opravdová hloubka pomocí perspektivního promítání ve 13. stol
- Renesance - hlavní vývoj perspektivního zobrazení - pojmy: hlavní bod, distance, horizont
- Kartografie - práce s prostorovými 3D daty - problém při výškopisu - Ptolemaios: metoda šikmého pohledu (vizualizace: kopečkovou metodou), kótování, sklonové šrafy, izolinie, barevná hypsometrie, stínování - **nejedná se o 3D vizualizaci**

## Kapitola 3 - Dnešní pojetí
2D: rovinná grafika
2,5D: přechod od 2D do 3D - v X a Y jedna souřandnice Z 
- v DMR nemůže být převis protože nemůže mít jedna poloha víc Z
- nezle zpracovat v klasických GIS nástrojích
 
3D: plnohodnotná tělesa
Bod musí mít X, Y, Z - nachází se tedy v 3D prostorou, pokud by se jednalo o 3D těleso pak každý bod o souřadnicích X, Y musí mít Z 

Problematika 3D vizualizace s počítači. Problém v terminologii pro samotné **3D objekty** a pro jejich **vizualizaci** - podle autorů nutné odlišovat. Záleží na volbě vizualizace 3D dat. Na obrazovku počítače to není 3D vizualizace, ale perspektivní pohled. Z obrazovky, nelze vyčíst Z. Dále autor diskutuje o metodách půdorysu a šikmého pohledu v návaznosti na zahraniční literaturu, kde zmiňuje termíny "Real 3D" (holografické metody, jiní: anaglyf, stereoskopické obrazy) a "Pseudo 3D" (perspektivní promítání). Dále autor bere v potaz posunu terminologických významů a dává jej do kontextu s budoucím vývojem 3D metod vizualizace, tedy s tím jak budou skutečné 3D vizualizace nazývány. Dálší kritika 3D vizualizce pro 2D obrazy je v souvislosti s dalšími obory. 

**Problematika pojmu 2,5D:**
1. Nesmyslný - počet dimenzí prostorou nelze vyjadřovat nepřirozeným číslem.
2. V informatice v odlišném významu
3. 3D nejčastěji chybně pro označení šíkmého perspektivního pohledu, pro vlastnosti dat označované v geoinf jako 2,5D není v kartografii vhodný ekvivalent

V oblasti informatiky je 2,5D: 
- ve hrách kdy dojem prostorou je vytvořen pomocí izometrického promítání - bez použití perspektivy 
- v CAD: 3D modely z grafických prvků (2D) - z úseček svislé roviny, z kružnic válcové plochy atd. 
- DMR - X a Y má jednu Z
- CNC - rovinné obrábění

Autor dále tvrdí, že termín 2,5 D je nelogický a nesrozumitelný. Autor dále uvádí příklad nesmyslného používání racionálních čísel na dělení kulové plochy na další zlomky zlomků.
## Kapitola 4 - Vizualizace 3D dat trojrozměrně
[[Trojrozměrný model]]: 
[[Stereoskopický model]]: 
Lentikulární folie - prakticky taky [[Stereoskopický model]] - cylindrické čočky - 3D - LCD
%%udělat zettl%%
[[Hologram]]

Principy metod:
**3D model**: používaná, jednoduchá na vjem, tvorba a archivace náročná
**Stereoskopický model**: dvojice rovinných snímků ve výsledku vnímána jako prostorový model 
**hologram**: fyzikální princip interference záření umožňuje zachytit virtuální obraz předmětu

Metody umožňují jednoznačný prostorový vjem a "odměření" všech tří rozměrů - autor je tedy považuje za 3D metody vizualizace.

## Kapitola 5 - Závěr
Autoři doporučují důsledné odlišení termínů:
- 3D vizualizace
- 3D model
- 3D data

V mnohých případech je metoda vizualizace pouze šikmé promítání, dnes je tomuto zobrazení ale říkáno 3D.  Přístup nazývání Real a Pseudo 3D nepovažují autoři za vhodný. 

2,5D považují autoři za zcela nevhodný. Doporučují nahradit zcela nový pojem pro charakteristiku DMR. 

Dále autoři zmiňují problémovost nástupu informačních teorií v kontextu kartografie a jejích metod. Autoři tedy zmiňují nutnost obezřetnosti při přejímání pojmů z jiných oborů bez ohledu na specifika oboru, který termíny přijímá. Uvádí, že je nutné v kartografii nemít *chaos v dimenzích*.

