---
title: Interoperable information model for geovisualization and interaction in XR environments
authors: Daeil Seo, Byounghyun Yoo
year: 2020
---
URL:  https://doi.org/10.1080/13658816.2019.1706739
ZOTERO: [See in Zotero](zotero://select/items/@seoInteroperableInformationModel2020) 
# Interoperable information model for geovisualization and interaction in XR environments
# Přínos pro DP
Práce detailně rozebírá informační model pro geovizualiace v XR prostředích. Na konceptuální úrovni představuje způsoby řešení integrace jednotlivých vrstev potřebných pro tvorbu aplikace (datové, interakční, vizualizační). Předstvený model je vystavěn na základě webových technologíí a zažitých postupů za účelem udržení interoperability. Z tohoto důvodu představuje práce hodnotný zdroj z hlediska architektury aplikace. 


# Abstrakt
# ch01 - Úvod
Práce představuje koncept Digital Earth (DE) a následně představuje termín geo-prohlížeč. Dále práce představuje řadu geoprohlížečů v pořadí od 2D zobrazní přes 3D až po AR. Práce zdůrazňuje fakt, že všechny zmíněné aplikace jsou technicky vertikálně interoperabilní - integrované a to přes obsah, aplikaci po "domain-specific" UX.
- aplikace by měli chtít interakci s běžným uživatelem

## obsah
- related work 
- diskuze problémů a principů tvorby informačního modelu pro DE v XR 
- samotný informační model
- popis vyvinutého prototypu
- výsledky a diskuze

# ch02 - Related work
*Interoperable content model for digital earth*
- nedostatek ID v tradičních OGC ML
- modelování ve VR -> deklarativní metody - VRML - 1. web-based 3D format - X3D - následník 
- Declarative 3D for the Web Architecture Community Group - přidání interkativní high-level  deklarativní 3D objekty jakou součást HTML dokumentu -- Mozzila -- Aframe
- A-frame -- entity component system 
Výše zmíněné technologie a přístupy jsou náročné na implementaci v případě dat reálného světa (location based).

Většina - "location-based" AR content specifications jsou vytvořeny na základě OGC standardu KML-ARML-KARML-ARML 2.0
- specifické tagy pro dané prohlížeče jako rozšíření - vztahy mezi geolokací a augmentací reality 

Přístup skrze principy sémantického webu - integrace dat z různých datových zdrojů do kontextuální AR systém.

AR a VR je možné reprezentovat v rámci jednoho prostředí - nejdříve koncept virtuálního kontinua, které reprezentuje MR (mixed reality) - dále přišel XR koncept jako extenze MR - Khronos Group -  OpenXR - APIs pro přístup všech různých XR vstupních zařízení - Mozzila přišla s WebVR specifikací - nyní nahrazeno WebXR - W3C spec

*Geo-tagged user-generated content on the Web*
- VGI
- georeferencovaná data ze sociálních sítí
- VGE - jako nová generace nástrojů pro geografickou analýzu

# ch03 Design principles for the DE in XR environments
* architektura DE aplikací dělena na - Data - Content - Application
* u dřívějších aplikací ve všech vrstvách specifická implementace pro danou aplikaci - kritika vertiální integrace naproti integraci meziaplikační
* Pro realizace DE v XR by měl informační mode lpodprovat in-situ uživatelskou interakci v XR prostředí.
* Cíle designu:
	* Interoperabilita - obsah vygenerovaný v jedné aplikaci by měl být interoperabilní s jinou,  přístup k obsahu bez potřeby dodatečných zásuvných modulů
	* Otevřenost - kdokoliv by měl být schopen tvořit a editovat obsah bez předešlé (rozsáhlejší) znalosti technologie, obsah je uložen v dcentralizovaných rozšiřitelných (scalable) úložištích přístupných všem
	* In-situ interakce s uživatele - context aware interface*

[[DE-VR-app-architecture.png]]
[[proposed-DE-VR-app-architecture.png]]

## Principy navrženého modelu
Horizontal integration - znamená, že to co zařizuje interaktivitu a XR rendering je přístupné přes všechny platformy (GIS, Web, SensorData). Autoři tvrdí, že DE - obsah by měl mít jeden univerzální formát... (reálně?).  -- *DE content?* -- XR enviroment independent -- HTML nástavba s linky na klasické formáty -- KML, X3D, ARML 
Samotná aplikace je pak rozdělena na: vizualizační, interakční a aplikační část.

Práce představuje porovnání existujících geovizualizačních aplikací s navrženým modelem. 
1) geobrowsery - vlastní informační model - velice specifický pro dané aplikace 
2) OGC - markup languages - snaha řešit interoperabilitu - problematické pro in-situ interakci - např. ARML vhodné pro AR content a in-situ, ale XML dialekt a problémový pro tvorbu AR contentu.

Inf. model který práce přestavuje používá webové standardy
- HTML - content representation 
- accesed using URIs and rendered on the web
- JS pro in-situ interakci skrze HTML DOM

# ch04 Information model of geographic XR interaction space
Představený model - GXRIS - geographic XR interaction space
Podporuje požadavky existuijících  VR a AR prostředí
1. maptiles
2. pin markers
3. information windows pro interaktivitu
4. scene graph - VR rendering space

V GXRIS autoři propojují místa a objekty v zájomovém prostoru pomocí vztahů. 
1. Place - seamless combination of digital augemnted physical a  immersive virtual enviroment
2. Object - věc v prostoru
3. Annotation - atributy objektu popř. místa (place)

[[inf-models.png]]

## Modelling
Popis jendnotlivých prvků informačního modelu.
[[Pasted image 20220405092410.png]]

## User interaction
1. Pohyb uživatele
2. Přímá interkace s některým z prvků (Place, Object, Annotation)

Typ uživatelské interakce závisí na XR prostředí. - viz. *state diagram*
1. User-related: Moved, ChangedHeading
2. Place-related: check in, check out
3. object-related: když je objekt viditelný, (detected, moved, missed aj.) 

## Webized content approach to geographic XR interaction space
Způsob publikování informace na webu zajišťuje interkaci mezi prvky pomocí uri a HTML struktury popř. dodatečné informace v JSON. 
GXRIS umožňuje organizaci, indezaci a vizualizaci LOD. Autoři představují concept sub-míst, kdy jsou místa, která jsou v zájmu uživatele dále dělena a je tím tvořena hierarchická struktura.

**Deklarace Place, Obj. a Anotace**
- custom elements -- interoperabilita?
- custom css rules
[[custom-css.png]]
[[custom-tags.png]]

# ch05 Implementace
![[GXRIS-app-architecture.png]]

![[Pasted image 20220405100139.png]]
![[Pasted image 20220405100146.png]]