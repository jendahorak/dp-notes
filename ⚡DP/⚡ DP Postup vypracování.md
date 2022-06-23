---
created: 2022-03-31 - 11:44
status/tags: 
---
# [[⚡ DP Postup vypracování]]
# Zadání
Práce bude zaměřena na technologie pro tvorbu virtuální reality v rámci webového prostředí (např. WebXR, Three.js). Tyto technologie jsou podporovány na různých hardwarových a softwarových platformách, jejich funkcionalita se může v různých podmínkách lišit. Na základě srovnání dostupných technologiích bude vybrána technologie pro vytvoření vlastní vizualizace prostorových dat z vybrané aplikační oblasti. Vytvořená vizualizace bude následně uživatelsky evaluována a zhodnocena tak její funkcionalita.

# Postup
Pro naplnění hlavního cíle diplomové práce postupujte přes následující dílčí cíle: 
1. Popis a analýza technologií pro tvorbu virtuální reality v rámci webového prostředí 
2. Praktické porovnání konkrétních technologií na různých hardwarových a softwarových platformách 
3. Návrh a implementace vlastní aplikace na principech virtuální reality 
4. Uživatelské ověření vytvořené aplikace 
5. Diskuse zjištěných výsledků a závěr 

# Vypracování
## K01 - Popis a analýza technologií pro tvorbu virtuální reality v rámci webového prostředí

**Otázky**
Co je to rozšířená realita (XR) co jsou principy virtuální reality?
Jaké je využití XR v geografii - kartografii - GIS?
Jak je možné dělit technologie umožňující XR?
Jaké existují HW pro XR?
Jaké existují SW (hlavně web) technologie pro XR?
- Integrace XR zařízení na webu - WebXR, Mozila Hubs
- Vizualizace, rendering na webu - vybrat knihovnu (three, babylon, cesium, aframe atd.)
- Způsob předzpracování dat ?
	- GIS -> Web (QGIS - QGIStothreejs, ESRI API for JS,)
	- GIS + graf. software + game enginy ( Unity (C#?), Maptiler - World Creator, Blender - OSM aj. GIS a neGIS data (3D model brna - KAM?)
Jsou vybrané aplikace vhodné pro potřeby kartografie - geoinformatiky?
- Jsou vybrané aplikace vhodné pro vlastní use-case

### ToDo
- [ ] koncept rozšířené reality -- stručné textové zpracování
- [ ] XR na webu - technologie, vývoj aktuální stav, specifika, předešlé případové studie -- tabulky kompatibilit HW, prohlížeče, data
- [ ] Zvolit tech stack -- textové odůvodnění zvolených technologií vhodných pro daný use-case


### Vypracování
**Seznam technologií** 
https://docs.google.com/spreadsheets/d/1daRg5jo2H6Z3chwf-ZCmyoM8zfnfrb1Yx4x3YoZpcME/edit?usp=sharing

### Výstupy
- [ ] Převážně text objasňující situaci ohledně technologií 
- [ ] odůvodněný soubor technologií pro vlastní vizualizaci (spolu s následující kapitolou)

**Kritéria hodnocení:**
1) Technická 
	- vývojová: náročnost na tvorbu 
	- softwarová: jak moc aktuální daná technologie je, zda má podporu a bude mít podporu  podpora napříč prohlížeči (*rešerše jader prohlížečů - analýza podpory pro jednotlivé technologie (knihovny, api atd.*) volně dostupná?
 2) Kartografická:
	 - je daná technologie vhodná pro danou aplikaci v geografii/kartografii - bude záležet na specifikaci aplikační oblasti a vizualizace  

## K02 - Praktické porovnání konkrétních technologií na různých hardwarových a softwarových platformách 
**Otázky**
Jaká je metodika pro porovnávání technologíí - co se porovnává? 
- výkon 
- UX
- developer exp. 
- vhodnost pro kartografické účely?

### ToDo
- [ ] různých úrovních náročnosti vizualizace
- [ ] různé vstupní zařízení
- [ ] různé zobrazovací zařízení
	- [ ] sw
	- [ ] hw - nutnost responzivního designu pro mobilní zařízení (google cardboard - pokud bude zvolen jako validní)

### Výstupy
- [ ] Popis testování - výsledky testů - vyhodnocení technologií
- [ ] odůvodněný soubor technologií pro vlastní vizualizaci (spolu s následující kapitolou)


 ## K03 - Návrh a implementace vlastní aplikace na principech virtuální reality 
**Otázky**
Jaké jsou dosavadní use-case v geoinformatice a XR?
Jaké use-case jsou vhodné pro web?
Jak vybrat vhodný use-case?
- problematická prezentace dat konvenčními způsoby - lepší v XR
- vhodně "jednoduchá" vizualizace pro webový prohlížeč resp. mobilní zařízení
- relevantnost pro kartografii

Jakým způsobem bude aplikace prezentována? 
- jen front-end - github pages
- bude potřeba backend - cloudfare, aws, azure, firebase?

### ToDo
Výběr aplikační oblasti.
- [ ] Rešerše existujících aplikacích VR  v geografii / kartografii - (**relevantní už pro první krok**) 
- [ ] Tabulka možných use-case - vypsat klady a zápory
Schopnost pracovat s tech.
- [ ] JavaScript - nutnost hlubší znalost
- [ ] 

**Kritéria výběru:**
**Data**
- dostupnost dat
- interoperabilita dat

**Technologie** - na základě zvoleného techstacku
- schopnost autora danou vizualizaci implementovat - protrénovat JavaScript


## K04 - Uživatelské ověření vytvořené aplikace
**Otázky?**
- Co testovat? 
	- Použitelnost aplikace?
	- Úroveň provedení?
	- Splnění definovaného účelu vizualizace?
	- Zvolenou technologii?
	- Zvolenou technologii v kontextu použití pro prezentaci geografických dat a v kontextu jiných způsobů vizualizace?
- Na kom testovat - podle účelu viz.?
	- úroveň vzdělání
	- možnost testovat na žácích ZŠ Kamenická Děčín
	- možnost testovat v prostředí vysoké školy - Geogr. ústav
	- možnost testovat v prostředí vysoké školy - FI MUNI - psychologie?
- Jaká je  metodika pro testování a následnou kvantifikaci výsledků ? 
	[[Brook System Usability Scale]]


Na základě zvolené aplikační oblasti definovat reprezentativní testovací skupinu. Na základě zvolené oblasti testování vytvořit testovací prostředí - pokud prostředí bude obsahovat interakci tak jednoduché úkoly. Pokud se bude jednat pouze o vizualizaci tak následný dotazník zahrnující UX s technologiíí s provedením vizualizace popř. rozhovor v průběhu testování a po testování. 



## K05 - Diskuse zjištěných výsledků a závěr 





---


