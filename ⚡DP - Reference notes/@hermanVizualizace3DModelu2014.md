---
title: Vizualizace 3D modelů měst na webu
authors: Lukáš Herman
year: 2013
---
url:  https://is.muni.cz/auth/th/ci12f/?cop=3846004
zot: [See in Zotero](zotero://select/items/@hermanVizualizace3DModelu2014)
status:
# Vizualizace 3D modelů měst na webu
*Práce se zabývá tematikou konstrukce a zásad tvorby 3D vizualizací. Typologií modelů měst. Srovnáním a testováním dostupných 3D webových techonolgií. Vlastní tvorba 3D vizualizace pomocí technologie X3DOM a diskuze jejích výhod a nevýhod*

# Úvod
3D vizualizace je ve vědě i v běžném životě
Výpočetní technika umožňuje virtuální realitu i interkaci v ní. 
## Cíle práce
Vytvoření zastavěné oblasti pomocí webových technologií na základě kartografických zásad. 
Popis současného pohledu na problematiku uživatelsky orientované 3D vizualizace v kontextu *kombinace* s dodatečnou 2D informací. Shrnutí technických východisek tvorby 3D modelů (dat. modely, formáty, hw a sw prostředky, vykreslování a postup tvorby vr). Analýza využití 3D viz. 
Vizualizace realizována v X3DOM. Zejména pro interaktivní propojení 3D objektů s atr. údaji a dalšími typy vizualizací.
## Soudobý stav - literatura
syntéza počítačové kartografie, geoinformatiky, počítačové grafiky
3D modelování je progresivní obor - *použití co nejrelevantnější nejnovější literatury*
Kartografie se 3D vizualizaci věnuje jen okrajově, lépe ve vyjemnovaných monografiích. 
## Vymezení území
## 3D v kart. a geoinf
sběr, modelování, vizualizace, analýza
## Terminologie
Autor uvádí rozkol v terminologii 3D v GIS a kartografii. Zmiňuje rozdělení terminologie na samotná data a na jejich vizualizaci. Autor respektuje definici kdy 3D jsou data, když je možné uložit více nežli jednu souř. Z. [[@kempEncyclopediaGeographicInformation2007]] a odvíjí se od toho, že konzumace vizualizace bude probíhat na standardním "plochém" monitoru. 
## V kart.
Autor zde dává důvod pro zkoumání nových 3D technologíi a ověřování jejich potenciálu. Odkazuje se na autory, kteří tvrdí že soudobá kartografie je ovlivněna více technickými limity nežli teorií. Autor odkazuje na [[@woodUsing3DVisualization2005]]
**Proces vizualizace**
management dat -> predzpracovani dat -> vizualni mapovani -> vykreslovani -> zobrazeni
Uspěšnost je determinována na základě úspěšnosti převodu mezi těmito kroky.

Autor zmiňuje velký význam herního a zábavního průmyslu na 3D vizualizace - realtime rendering a interaktivita. 

## 3D geovizualizace
Definice geovizualizace *plánování a generování znázornění digitálních geografických dat realizované podle daných pravidel nebo algoritmů prostředky počítačové grafiky na displeji*
/+ 3D - *plánování a generování znázornění digitálních geografických dat realizované podle daných pravidel nebo algoritmů prostředky počítačové grafiky na displeji* + interkativita
Dělení dle ([[@bleisch3DGEOVISUALIZATIONDEFINITION2012]]):
- 3D pro abstrakci 
- verna reprezentace sveta
Autor dále rozvádí koncept použití 3D vizualizace jako věrné reprezentace irl. Dále pak uvádí pravidla optimalizace uživatelských rozhraní pro 3D. (viz. pdf) Autor zdůrazňuje důležitost pohledu na 3D vizualizaci jako celek: brát v úvahu nejen technologické aspekty ale i uživatelské.

## Semiotika a 3D vizualizace
Vizualizace je převedení charakteristik dat do grafických proměnných. 3D přidává ke klasickým Bertainovským další proměnné. Jiný přístup je pomocí menšího počtu graf. proměnných a mechanismů designu (globální - osvětlení, stínování, atmos. efekty, objektové - materiál, textury, průhlednost a orientace). Autor také uvádí nedostatečnou rigorozní znalost vlivu "nových proměnných" na kongnitivní schopnosti, tudíž dochází k nesprávnému použití a uživatel pak může zaží stimulační saturaci vnímání.  Dále autor v referenci na další výzkumy uvádí možné komplikace užívání daných grafických proměnných. 
Hlavní role semiotiky ve 3D spočívá v seřazení grafických proměnných dle vhodnosti. 

**Nejvhodnější**
- tvar, textura, barevné odstíny
- problematické jsou kvantitativní vizualizace - velikost, výška i sytost podléhají zkreslení

=> nutné použití speciálních postupů

## Percepce 3D obrazu
Autor zde podrobně popisuje aspekty kognitivního vnímání hloubky pomocí konceptu prostorových vodítek. Autor dále podrobně rozepisuje implikace, které vnímání 3D přináší pro 3D vizualizaci. 

![[Pasted image 20220618192659.png]]


## Uživatelské nároky a testování percepce
Autor zde uvádí výsledky výzkumů řešících perference uživatelů při práci s 3D vizualizacemi urbánních prostředí. Proces identifikace nároků: identifikace účelu, vyžadovaná podrobnost objektů.
Zjišťování požadavků má velký vliv na další konstrukci 3d vizualizací... jelikož je nutná maximální generalizace z technických i percepčních důvodů. Nejdůležitějším faktorem stejně jako u klasických map je **ÚČEL**. 

## Co je fotorealistické - různé úrovně abstrakce scény
LOA - level of abstraction
Techniky nefotorealistické vizualizace:
- Osvětlení
- Vybarvení a stínování
- Hrany a siluety
- Textury

## Adaptivní 3D vizualizace
Ze stejných dat - různé vizualizace - různé kontexty - scenaria
![[Pasted image 20220618194138.png]]



# 3D varianty kar. metod
Vstupní geometrická data mají geometrii bodovou, liniovou, plošnou a objemovou. Lze je zobrazit pomocí různých metod. Kartografické metody pro 3D vycházejí z 2D metod a jsou rozšířeny o jeden rozměr. 

## Kvalitativní
Informace o poloze, existenci a významu znázr. objetku
Hranice mezi znaky objemovými a ostatními jsou neostré. 
Volba použité geometrie znaku je závisla ná účelu. Podle [[@peggDesignIssues3D]]
autor uvádí zásady tvorby 3D znaků. 
- symboly podobné objektům irl
- stejnou dimenzionalitu jako irl
- pro různé účely na základě uživatele
- co nejméně polygonů

Bodové znaky neodpovídají rozloze reálně - jsou **mimoměřítkové**. Do 3D scény pomocí vztažného bodu. Dále autor uvádí rozdělení dle Kaňoka - geometrické, symbolické, obrázkové, alfanumerické

liniové, plošné i objemové znaky mohou být nahrazeny množinou rozmístěných bodově lokalizovaných znaků. 

## Metody Kvantitativní
kvant. údaj je takový který mimo inf. o poloze a kvalitě nesei informaci o množství. Součástí 3D abstraktních vizualizací. 3D tečky, kartogramy, kartodiagramy, izopletové mapy
Lze používat 2D s 3D dohromady. 

Autor dále rozebírá zmíněné metody a jejich 3D aplikaci. 

## Popis
Autor uvádí dva základní způsoby umistovani popisu:
1. součást textury
2. popis jako 2D nebo 3D objekt

## Multiperspektivní projekce
3D ekvivalent anamorfozy - deformace pohledů na 3D modely nebo modelů samotných. 

## Výhody 3D viz
- více využitelného prostoru
- velikost může nést více informací 
- překrývání symbolů nad sebe

## Nevýhody 3D 
Problematika v 3D je srovnávání - 3D viz. představuje nestejné měřítko. Metody vylepšující srovnatelnost: 
- referenční rám
- srovnávací roviny
- symboly složené ze segmentů
- **rovnoběžné promítání**

Metody řešící překryv:
- Nezobrazení přerytých
- redukce velikosti
- Odsunutí
- deformace pohledu
- rotace změna polohy pohledu
- průhlednost objektů 
- stínování
- **provázané pohledy na data** - 3D pohled + 2D mapa pro lokalizaci



# Technologie pro 3D modelování a vizualizaci
*datové modely, formáty, webové služby, problematika využití virutálních prostředí v kart. a geoinf, dostupné technologie pro 3D web.*


## Datové modely
Drátěný, Povrchové (TIN, GRID, reprezentace hranic - B-rep), Objemové, 

### Nadstavbove vlastnosti
- deformace -> ?
- topologické a semantické informace 
	- union, intersection, difference
	- např. pomocí XLink (XML Linking Language)
- semantika
	- význam dat
	- možnost vyhledávání a prostorových analýz
	- umožnuje taxonomie
## 3D formáty a služby
Formáty se liší účelem a otevřeností. 

**OpenGL**
**VRML**
**X3D**

**KML**- souř. sys. a xml
**Collada**
**3DMLW** - struktura OBJ
**3DPDF** - **U3D**, **PRC** - velké množství 3D dat
**OBJ**
**3DS**
**U3D** - ECMA - kontinualni stupne detailu a progresivní datový tok
**IFC** - CSG - objektově orientované semantické modelování  budov ve FM (facility amangementu)
**CityGML**- 
**Multipatch** - Brep 
**CADy**

Dále autor prezentuje matici požadavků na dané formáty -> uvádí řadu parametrů

## Webové služby
WPVS - WTS - vrací na serveru vyrenderované pohledy na scénu - *GetCapabilities, GetView, GetDescription, GetLegendGraphic*
W3DS - vrací 3D geometrii - X3D výstup - klient provádí vykreslování - serverové řešení CityServer3D - klientská aplikace = XNavigator, BSContact Geo - OGC 3D Potrayal  (**#TODO** - kouknout na soucasny stav)
WFS - GML a CityGML

## Virtuální prostředí
poskytnutí iloze v umělém prostředí - dobré pro laiky
Základem je tvorba 3D objektů a scén, manipulace s nimi, pohyb v prostředí, detekce kolizí, a real time rendering.  Metody jsou umocněny pomocí hardwarových prostředků jako: 
- stereoskopické plochy
- snímače polohy prostoru
- HMD
- běžný pc

Klíčové charakteristiky VR:
- rtr
- 3D scene
- navigace
- interaktivita
- multimedia -zvuk atd.

## Dělení virutální reality
**Immersive VR** - speciální tech zařízení, odříznutí uživatele od světa, 
**Augmented VR** - kombinace skutečného světa a virutálního, synchronizace pohybu uživatele
**jednoduchá VR**- nevyžaduje spec, tech zařízení 

Jde dělit i na množství skutečnýcha  virtuálních prvků prezentovaných uživately.  *reality-virtuality continuum* -> Žára 2004, Slocum 2005 - různí autoři různě dělí tento přechod
Dle hlediska počtu uživatelů se dá mluvit o - multiuser vr
Distribuovaná VR - ?? 


Bodum 2005 - dva parametry virtuálních prostředí: 
- úroveň reprezentace - *level of representation*
- časová složka - *temporal characteristic*
Dělení VR pomocí míry abstrakce na různé úrovně reprezentace. 

## Vztah VR a GIS
terminy - VRGIS, virtual GIS + internet => *colaborative virtual enviroment* = distribuovaná virtuální realita
Jiné definice - virtual enviroment
Lin(2010) - VGE => prostředí jako platforma - model chování, geometrický a fyzický model
VGE:
- virtuální svět 
- avatar

GIs - data
VGE - clovek
CVGE - distribuovaný grafický svět reprezentující a simulující geografické objekty a procesy, který umžňuje užviatelům z různých msít zkoumat problémy, vytvářet hypotézy a plánovat.

## Faktory virtuální reality
**Immersion - Vnoření** - subjektivní psych. stav jak moc je uživatel spjat s okolním virt. prostředím.  Zjednodušení někdy přednost
**Intenzita informace** - jak detailní je prostředí - LOD LOA - měřítko generalizace
**Inteligence objektů** - vyspělost interakce objektů v prostředí
**Interaktivita** - metody ovládání vytvořené světa a pohybu v něm - interakce a manipulace s objekty - ovlivněno SW a hW

"Bez dostatečné informační kapacity prostředí není možné generovat přesvědčivě vypadající virtuální prostředí. Tento faktor je však nejvýznamněji ovlivněn výkonem dostupného hardware a software (Oršulák, Pacina, 2012, s. 58-62)."

## Zobrazení virt. prostředí
Avatar
- virtuální kamera

Transformace 3D do 2D monitoru - promítání (rovinné projekce). Dochází ke ztrátě prost. informace.  -> r;ůzné metody projekce

**Rovnoběžné**
- všechny paprsky mají rovnoběžný směr
- zachovává relativní velikost modelu
- Mongeovo, izometrie
- vypuštěna vodítka - relativní velikost obrazu na sítnici
-

**Perspektivní** (středové)
- odpovídá modelu lidského vidění
- zmenšuje se to co je dál, nezachování rovnoběžnosti úseček

## Pohyb ve virt. prostorou
ideálně 6 stupňů volnosti - pohyb kolem 3 os a rotace kolem 3 os
vázaná a volná kamera
Při použití volné kamery na ní zpravidla působí fyzikální zákony (zrychlen atd.)

Základní 3 typy:
- chůze  - gravitace, kopírování terénu
- létání  - bez gravitace 
- zkoumání - bez kolize

Další pohyby - uhel natoceni, pan, zoom, lookat, 
Nej. - tracking

## Osvětlení a stínování
Dělení způsobu osvětlení (podle tvaru zdroje)
- bod - omni light
	- žárovka - spotlight
- plocha - area light
	- parallel light (stíny stejný směr
	- simulace slunce
- ambient light - fixně celou scénu
- klíčové světlo - hlavní světlo pro scénu - definuje směr stínů
- výplňové světlo - osvětluje stíny vytvořené hlavním světlem

Stínování se definuje jako kolísání barvy a jasu povrchu v závislosti na osvětlení. 
- konstantní
- Phongovo
- Gouraudovo

## Reprezentace virtuálních scén
*Co je to 3D scéna*
Množina 3d objektů doplněná dalšími informacemi potřebnými pro její zobrazení. Scéna je uspořádána do hierarchické struktury. - *scene graph*

### optimalizace 3D scén
= dosažení dostatečné intenzity a minimalizace výpočetní náročnosti 
- pohledová redukce - renderovány jen modely v aktuálním pohledu a na LOD

LoD je bezrozměrný údaj, chápaný jako možnost odebírat a přidávat daným objektům jejich detaily.
Pro náročnost se používají diskrétní stupně detailu. 
Pro objekty kterých je hodně -> bilboard / sprite (pruhledný polygon s texturou otáčejcí se na uživatele)
Vykreslení pozadí scény - místo objektů vzdálených od kamery
Samotné objekty se generalizují. 
Rastrová data se tilují
Textury se převzorkovávají - downsampling


# Hardware
jak využít stereoskopii - dívání se na věci z dvou bodů (očí) od sebe vzdálených d

**anaglyf**
**pasivní 3d stereoskopie** - polarizační filtry v brýlých - promítáno dvěma projektory
**aktivní 3d stereoskopie** - aktivní brýle - projekční plocha střídá obrazy pro levé a pravé oko
**autostereoskopické monitory** - 3D LCD - maska před monitorem vychyluje obrazy pro jednotlivé oči
**CAVE** - stereoskopie na kvádru
**HMD** - prostorová iluze odděleně prezentovány dva obrazy pro každé oko jeden - snímá pohyby hlavy 
**Laserové projekce** 
**3D tisk**


# Software
1. desktop
	1. GIS - povrchy, objekty, morfometrické analýzy
	2. CAD
	3. DCC
2. web
Autor uvádí dostupnost analytických nástrojů v GIS sw. Dále pak uvádí souhrn užívaného sw a kompatibility s formáty dat. Kompatibilita formátů je klíčová. 

# 3D vizualizace na webu
Internet  umožňuje kombinaci s virt. realitou a  tedy i přístupem více uživatelů. *distributed virtual reality* *collaborative virtual enviroment*. 
Různé technologie, žádná zatím správně multiplatformní. Pluginy.. (**#TODO** už je jinak WebGL a HTML5).

## Pluginy
Problematické protože se musí intalovat a nejsou bezpečné. Nezle přitupovat k zobrazní pomocí DOM. Jediný úspěšný Flash.
Microsoft Silverlight
O3D - Google API - obdobné X3D - interakce v JS
java3d - NasaWorldWind
XNavigator - pro 3D webové služby
MPEG-4 - zvuk a 3D 
GoogleEarth plugin - KML

## Bez pluginů
HTML5 - semantické tagy, úložiště pomocí asociativního pole, multimedia, canvas, svg 
HTML5 canvas - OSM Buildings - Leaflet OpenLayers
HTML5 - 3D - X3D - není popsána manipulace  s grafem scény - neuvádí jak by implementace a integrace do HTML5 měla vypadat - přímo v HTML jako SVG nebo v DOM jako kotainery

## WebGL
 - 3D přímo na stránce skrze canvas - nutná podporvaná GPU - *shader rendering* 
- bezpečnostní rizika webgl 
- Google vypropagoval WebGL - WebGL Earth - MapTiler
- CesiumJS - obdobná manipulace s globem - + konverze dat do potřebných formátů
- WebGL pro vizualizaci bodových mračen
- CityEngineWebViewer - Scény z CityEnginu
- ReadyMapSDK 
- OpenLayers s HTML5, CSS a WebGL skrze Cesium
- WebGLU - JQuery pro WebGLU? 
- C3DL 
- X3DOM - v JS - vložení X3D do HTML - manipulace skrze DOM - vykreslování skrze samotné X3D, WebGL a Flash
- XML3D - integrace s DOM
- SpiderGL
- GLGE
- SceneJS
- CooperLicht 

Mnoho knihoven a technologií použivá XMLHttRequest (XHR) - komunikace aplikace se serverem - prostřednictvím HTTP protokolu - změna načtení části obsahu stránky. 


# Modely měst
*varianty 3D modelů, možnosti jejich využití, typologie konkrétní řešení*
2mapy, 3D blokové i tematické modely

## Oblast využiti
Územní plánování / architektura - výškové zonování, viditelnosti, 
3D katastr nemovitostí
Facility management
Inženýrské sítě
Šíření signálu

Propagace a prezentace měst a jejich části
ochrana životního prostředí
únik nebezpečných látek, biogeografické bariéry

hlukové mapování
městské klima
umístění solárních panelů
energetické nároky budov

krizový management
kriminalita

## Typologie
**Podle způsobu vizualizace:**
- fotorealistické - co největší podobnost s irl
	- geom. detail, textura atd. 
- nefotoreal
	- blíží se reálnému vzhledu
	- tematické mapy
- kombinace

**Podle úrovně podrobnosti**
míra geom. detailů a detail textur
- 2D a ortofota
- panoramatické snímky - pseudo 3D modely - 360 rozhled - posun z jednoho místa na další
- blokové modely - extruze 2D pudorysu
- blokove modely s texturami
- modely s arch. detaily a strukturou střech
- plně objemové  CAD

Dělení se primárně odvíjí od úrovně abstrakce.

**Podle rozsahu**

**Způsob pořizování dat**
často kombinace metod
- pozemní snímkování - prim. textury
- panoramatické fotografování - 
- letecké snímkování - 
- lidar

**funkcionalita**
-  estetické
- proprietární s analytikou
- plně analytické
- hybridní

ovlivněno výrazně použitým softwarem

**časové hledisko**
Podle toho jestli zobrazují minulost, budoucnost či současnost
Dělení na statické a dynamické - zda zobrazují v jednom čase nebo vývoj

## Řešení
1) Virtual London
2) Model Berlína - Solar atlas - Wirtschaftsatlas
	1) Google earth KML
	2) Simkas 3D - inž. sítě
3)  Heidelberg, Mainz nebo Stuttgart
4) Virtuální glóby
	1) Google Earth
	2) Esri??
3) 3D model města prahy
4) Geodis
5) rekonstrukce stavu - model brna 1645, model prahy Langweilův, opevnění olomouce
6) vysokoškolské prostředí - menší modely - tematické - klima 

# Tvorba 3D modelu města pro prez. na webu
*požadavky 3D webové vizualizace - srovnání tech. - navržení vhodné - srovnání s 2D mapami*
## Požadavek
Specifikace, popis vlastností a funkcí, které by měl výsledný systém mít. "přání uživatele" (vývojáře??)
## Nefunkční požadavky
- podmínky omezující fungování systému - příkazy a zákazy
- **cena** - data, sw, pracnost, developement
	- technologie - free SKD, knihovny a API
	- data - ?? - vlastní tvorba? - získat free? - cena
	- pracnost vývoje - jak moc je nutné data upravovat, jak složitá aplikace bude- 
- **použittelnsot**  - user friendly, intuitivní 
	- ve 3D - OVLÁDÁNÍ A NAVIGACE
	- doba zaškolení uživatele co nejkratší - hned po prostud. nápovědy - co nejkratší
- **dokumentace**
	-  vývoje a aplikace, nápověda práce s app
- **výkonnost**
	-  1MB za sekundu - odpověď
	- kapacita 5požd. za sekundu
	-  dostupnost - 99%
	-  aspon 25fps
- **přístupnost**
	-  device agnostic
- **rozšiřitelnost**
	- možnost následných vylepšení
- **interoperabilita**
	- spolupráce systémů
	- využít datové standardy a standardní technologie
- **přenositelnost**
	- minimalizace závislého kódu
	- externí datové zdroje ve formě služeb
	- CDN


## Funkční požadavky
**Pohyb 3D scénou a navigace**
- interaktivní pohyb by měl být intuitivní
	- přednost zoomování před létáním a chůzí
- zjištování polohy a orientace
	- souřadnice nebo 2D mapa
	- orientace virt. kamery

**vizuální stránka 3D scény**
- přehlednost a srozumitelnost
	- vhodné grafické proměnné, úprava 3D dat, omezení textur, 
- srovnání výšky a velikosti
	- implementace různých promítání - rovnoběžného
	- alternativní pohledy na data - text, grafy, tabulky
- překrytí objektů 
	- implementace pohybu - interaktivní i neinteraktivní pohyb
	- průhlednost
- omezení informací za účelem zachování přehlednosti - *details on demand*
	- popups, tabs, hypertext, externí zdroje inf.
- zdůraznění klíčových prvků a míst scény
- silnější imerze - přidání prostorových vodítek (atmosférická perspektiva) 

# Volba technologie
*autor uvádí podrobnou analýzu dostupných technologií a následně metodicky vybírá X3DOM pro praktickou implementaci*

2013 - 13 WebGL aplikací
Testovací případy - geovizualizace - modely terénu, glóby, virtuální glóby
Správnost zobrazení souzena v prohlížeči Google Chrome 
- manipulace
Nej: X3DOM - *fallback* model - rozšiřuje okruh potenciálních uživatelů
V IE pomocí Falshe
Hodnocení nejen knihoven ale i prohlížečů. 
![[Pasted image 20220620130336.png]]

Hodnocení kolik uživatelů používá jaký prohlížeč.

## Další tech. podmínky
### vkládání dat
- využití existujícíc deklarativních struktur - VRML, X3D -> html, 
- VRML -> X3D 
- X3D - pomocí XSLT
- COLLADA

### prog. jazyk
- WebGL na webu je abstrahován skrze JS API nebo JavaAPI
- Cesium a OpenWebGlobe - C#

 ### rychlost vykreslování
 - nebyla testována

### rozšiřitelnost
- webové standardy - nebyl schválen standard 3D grafiky

### podpora geogr. souřadnic
- nutnost podpory zemských souř. systémů

## Netechnologické parametry
- kvalitní dokumentace
- licence


# X3DOM
- živá datová struktura skrze HTML DOM - přímá manipulace s DOM - není potřeba žádný plugin - klasické HTML eventy
- UA - User Agent - udržuje DOM - integruje finální obraz a resolvuje URI
- X3D runtime - funkce pro změnu 3D scény
- Connector - jádro propojuje DOM s X3D runtime - přenos změn v obou směrech. 

![[Pasted image 20220620131714.png]]

X3DOM - v JS
X3D root
- detekovatelný z JS
- seznam X3D profilů
- JS vrstva buduje a ruší backend
- monitoring změny v DOM a graf X3D scény

=> *fallback model* - uspořádávání pomocí rychlosti vykreslování
Další backendová řešení...
- Plugin v C++
- WebGL backend - JS a canvas - aktualizace mezi DOM  a grafem X3D jsou pomalé. 
- Adobe flash - nejpomalejší

Vkládání scény pomocí XML zápisu - existuje i možnost bin dat 

## Graf. primitiva a manipulace s nimi
*struktura X3D a implemetace X3DOM*
- X3DOM využívá vybranou část X3D dat 
- definovat v html není vhodné protože moc dlouhé -> inline
- html DOM má vždy jen jednoho rodiče - X3D více rodičů (defs...)
- seskupení pomocí Group

## Vzhled a osvětlení
- využívá Materiálů - jaký model PBR ??
- textury


 ## Integrace s CSS a JS
 - X3D neodděluje stylování
 - klasicky pomocí selektorů (tag, id, class)
	 - jen na html elementy
 - ne na X3DOM elementy 

- Přístup přes JS
	- klasicky přes selektory
	- manipulace přes klasické metody appendChild, removeChild
	- události
		- onkeypress, onclick, onload, mutation - změna dom struktury, touchstart, touchmove

## Promítání prohlížení a navigace
Nastavení parametrů pohledu a pohybu virtuální kamery

## API
funkce umožňující modifikaci scény a interaktivitu


# Samotné vypracování
Autor shrnuje požadavky na vybranou případovou studii.
Vytvořeny byly dvě varinaty
1. znázornění hlukové zátěže - tematické
2. vizualizace vzhledu území - více fotorealistické

## Data
- blokový model budov - shp, upravený, upravený CityGML
- vrstva protihlukových bariér
- ZABAGED - polohopis i vyskopi
- Hlukové mapy
- ortofoto
- intenzita dopravy

### zpracování dat
ArcGIS ANALYST - VRML - X3D
převod hlukových map - Gimp


# Tvorba X3DOM webGIS
## Uživatelské rozhraní
- JQuery
- design layoutu aplikace
- doplńujícíc aspekty orientace 
-  severka SVG
	- rotace severky 
- přehledová mapa
	- střed mapy odpovídá souř. kamery
	- svg navigace
	- OpenLayers 
- atributy vrstev
	- vyskakovací okno pomocí JQueryUI
- interaktivita bočního panelu
	- vrstvy
	- pohledy
	- scéna

## Optimalizace pro snížení obejm dat
- seskupení objektů do DEFS - na LODy - automatizované odvození LOD na serveru
- komprimace - zip
- binárky
- SW aopt  - CLI pro komprese

## Atributy
- umístění atributů do nevých elementů a externích souborů

## XSLT transformace
??

## X3DOM rozhraní web služeb
WMS - zdroj textury - X3DOM neumožnuje fetchovat
- workaround - PHP skript na stahování WMS, popř. WFS

## Rozsirezni X3D a X3DOM vizualizace
- animace, zvýšení realnosti scény

Základní prvek, který ovlivňuje reálnost výsledné 3D scény je použitý typ promítání. (středové - perspektivní x rovnoběžné).  Osvětlení je důležité. 
Přidán fog - atmosférická perspektiva

Větší imerze pomocí anaglyfu - pomocí Instant PLayer - následně nelze použít barevný odstín jako graf. proměnnou. Pomocí stereoskopie lze použít HMD. - posunutí obrazů

## Animace
X3D umožnuje
Možnost video textur


# Diskuze
Testování velikosti vrstev, rychlosti načtení scény a odezva na XHR požadavky. Testováno na Mozzila, Chorme, a Opera. Nešla přehledka. Flash backend nedělla textury. 
Autor dále porovnává aplikaci s existujícími aplikacemi vyvinutými stejnou technologíí. 

# Závěr
Autor shrnuje úspěsnot samotné aplikace v kontextu vývoje technologie X3D a následně zmiňuje možnosti a budoucnost 3D vizualizace v kartografii. 




