---
title: Usability of WebXR Visualizations in Urban Planning
authors: Michał Rzeszewski, Matuesz Orylski
year: 2021
---
URL:  https://www.mdpi.com/2220-9964/10/11/721
ZOTERO: [See in Zotero](zotero://select/items/@rzeszewskiUsabilityWebXRVisualizations2021)
STATUS:
TAGS: 
# Usability of WebXR Visualizations in Urban Planning
**ToDo**-- *projít relevantní navazující literaturu*-- *projít codebase - inspirace pro strukturu projektu* -- *kritika*

# Abstract
XR - extended reality - běžněji zvažována pro praktické využití v urbánním plánování a "smart city managementu". Nová vizualizační technologie, která umožňuje přístup na místa, která nejsou v reálném světě přístupna. V rámci výzkumu autoři testují 6 - VR a AR případových studií aplikovatelných v civilním plánování pomocí WebXR technologie. Tyto případové studie jsou v rámci článku evaluovány. Výstupy tvrdí, že použitá technologie je vhodná pro použití v civilním plánování. 

# ch01 - Intro
Zde autoři představují moderní přístup k participativnímu územnímu plánování jakožto podnět k průzkumu WebXR technologie jakožto platformy pro tvorbu veřejnosti dostupných VGE. Dále článek stručně shrnuje zapojení XR do domény geografie a GIS. Popularitu VR podporují zmínkou o technologiích jako je *digital earth*, *digital twins*, *spatial computing*. Dále článek srovnává výhody a nevýhody tradičních "headset - only" a mobilních VR aplikací s WebXR přístupem.



# ch02 - XR terminologie a dosavadní znalost

## Definice XR - AR - MR - VR
VR - *an alternate world filled with computer-generated images*
4 Is Virtuální reality
WebXR nepřináší nové typy popř. definice vizualizací a tvorby prostředí rozšířené reality, ale je nástrojem pro vytváření rozšířené reality ve webových prohlížečích. WebXR je hlavní stavební kámen tzv. immersive web movement za kterým stojí W3C Immersive Web Community Group. WebXR poskytuje platformě nezávislý framework umožňující implementaci pro AR a VR zařízení. Čímž umožňuje vytvořit aplikaci, která bude vhodná pro VR i AR. 

## XR v územním plánování a GIS
Zde autoři zasazují XR do kontextu vužití z hlediska urbanního plánovaní a GIS expertýzy. Stručně popisují historii XR a následně jemenují různé případové studie, které se využitím nějaké úrovně XR zabývaly. Na závěr zmiňují problematiku spojenou s širší adopcí XR v praxi, za kterou považují nedostatečnou iniciativu produkce "dobrých" 3D modelů. 

# ch03 - Metody
1) Vytvoření WebXR aplikace s VR a AR případovými studiemi. 
2) Testování na potenciálních uživatelých. 
3) Data - 3D model města Poznaň. 

## WebApp
Techstack - three.js, WebXR API, Canvas UI library
Three.js - pro tvorbu, renderování a animaci 3D modelů v prohlížeči skrze WebGL
WebXR -  VR a AR schopnost

## Data
3D budovy - Poznaň - LOD2 (střechy?)
Renovace prostředí - 2D - přidány 3D modely pro dané body zájmu
Google Earth data

## Software
Blender - BlenderGIS  - glTG format

## Testování
Autoři testovali použitelnost na nereprezentativním vzorku 15 lidí, kteří s konceptem územního plánování byly profesně obeznámeni (architekti, urbanisté - studenti, GIS specialisté). Každá z aplikací obsahovala určitý jednoduchý úkol. Průběh testování byl pozorován na separátním zařízení. Následně po dokončení úkolů ve XR aplikacích vyplnili uživatelé dotazník a byl s nimi proveden rozhovor. Kvatitativně byli výsledky zpracovány pomocí [[Brook System Usability Scale]]

# ch04 Výsledky
V rámci dotazníku vyplňovaného po průchodu XR prostředím uživatelé ohodnotili zážitek na SUS (system usability scale) a vyplnili otevřené otázky na téma problémů aplikací a možného využití. Do výsledků jsou zahrnuty i poznámky získané z hlediska autorů práce při testování aplikací. Následně práce evaluuje získané výsledky. Podrobně porovnává jednotlivé aplikace mezi s sebou a identifikuje problematické aspekty. Aplikace byly vyhodnoceny jako vhodné pro využití v urbánním plánování. Z hlediska dalších využití XR byly nejlépe hodnoceny využití pro získání "sense of scale" a to především v oboru architektury. 
Práce dále hodnotí WebXR i z developerského hlediska a to poměrně kladně. Zmiňuje možnost propojení GIS a Web vývojových ekosystémů. Jako negativum práce uvádí nutnost grafické optimalizace prezentovaných dat pro dosažení optimální výkonnosti na různých výstupních zařízeních. Jako další nevýhodou z vývojářského hlediska je fakt, že WebXR a celkově virtuální realita na webu je stále velice novou technologií, tudíž není tolik návodů a "správných" přístupů k tvorbě jako u jiných webových technologií. 

# ch05 Diskuze
- webxr může být vhodné pro územní plánování
	- dostupnost urbánních dat
- i základní aplikace jako tyto jsou použitelné a užitečné
- autoři zmiňují že převážně kladné výsledky mohou být ovlivněny tím že participanti nebyli dříve s technologií XR seznámeni, tudíž kladná hodnocení plynula z novoty technologie a nikoliv ze způsobu provedení
- pro tvorbu dostupných XR aplikací je vhodné zahrnout nějakou míru již známých konceptů (obraz tradiční mapy - aj.) za účelem familiarizace uživatele s prostředím. 
- nové způsoby interakce a zapojení které XR nabízí nejou až tak vyžadované - budoucnost XR je více limitována tím na co je možné ji využít
- limitace WebXR spočívá v simplicitě UI a nedostatku grafické optimalizace
- při dalším vývoji je vhodné zaměřit se na jeden aspekt XR 


- práce hodnotí WebXR jako vhodné řešení pro rozšíření aktivit v oblasti územního plánování
- za účelem jednodušší a více přístupné implementace této technologie studie vyzdvihuje potřebu širší integrace GIS dat a XR a webu
- dále práce zmiňuje potřebu dalšího výzkumu v možnostech "XR systémů nové generace?" 
- LOD 3D modelů na webu - práce diskutuje zda opravu vyšší LOR (level of realism) vede k vyšší imerzi a zda imerze není vázána také na určitý use-case (účel vizualizace, zadaný úkol aj.)
-  
	- 




