---
title: Interoperable information model for geovisualization and interaction in XR environments
authors: Daeil Seo, Byounghyun Yoo
year: 2020
---
URL:  https://doi.org/10.1080/13658816.2019.1706739
ZOTERO: [See in Zotero](zotero://select/items/@seoInteroperableInformationModel2020) 
# Interoperable information model for geovisualization and interaction in XR environments

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
	* Interoperabilita - obsah vygenerovaný v jedné aplikaci by měl být interoperabilní s jinou
	* Otevřenost - kdokoliv by měl být schopen tvořit a editovat obsah bez předešlé (rozsáhlejší) znalosti technologie
	* In-situ interakce s uživatelem - ... 
* 