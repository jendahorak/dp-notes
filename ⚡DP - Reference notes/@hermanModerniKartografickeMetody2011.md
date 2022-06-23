---
title: Moderní kartografické metody modelování měst
authors: Lukáš Herman
year: 2010
---
url:  https://is.muni.cz/auth/th/edmr7/
zot: [See in Zotero](zotero://select/items/@hermanModerniKartografickeMetody2011)
status:
# Moderní kartografické metody modelování měst

# ch1 cíle práce
*shrnuje cíle práce, její strukturu*
- City GML- 3D prostorová reprezentace a aplikace pro tvorbu modelů měst
- 2008 - OGC
- nejen vizualizace ale i analýza
- definování tříd a vztahů
- nejen **geometrie** ale i **topologie** a **semantika**

- shrnout východiska pro 3Dmodelování - geoinf. a počítačové grafiky

# ch2 reserse
*prehled literatury*
Literatura 3D gis je zaostalá - [[@abdul-rahmanSpatialDataModelling]] (Abdul-Rahman A., Pilouk M. (2008), Reddy M. (2008a), Reddy M. (2008b), Loidold M. (2008), Neves J. (2008), Smith S. L. (2003) a Hudson-Smith A., Evans S. (2003).
Domácí litearatura také příliš není - Voženílek (2005)
Dále autor uvádí studentské prace - Slováček, R. (2002), Podhrázský Z. (2006), Malý M. (2009), Brychtová A. (2010) nebo Rybáková H. (2010)

Nejdulezitejsi zdroj - OGC specifikace - dále autor uvádí různé částečné zdroje a webové rozcesetniky. 

Autor zmiňuje že se jedná o jedinou práci na CityGML v ceskem jazyce

# ch3 vymezeni uzemí
*popis vybraného území + mapa*

# ch4 3d v geoinformatice
4 časti:
- zisk dat
- modelování uložení (sdílení dat?)
- vizualizace
- analýzy

Autor zmiňuje rozkol  v 3D terminologii v rámci geoinf. i napříč obory. Autor souhlasí s definicí 3D prvku a používá 2,5D terminologii k vyjádření "povrchů".  

Dělení a charakteristika modelování 3D informace na základě konceptualizace
- drátěné, povrchové, objemové
- povrchové - GRID - DTM DSM, facet - TIN
- objemové - voxely - octree, CSG

## Sběr dat

- 




- dpz - fotogrametrie - stereoskopie
- lidar
- geodezie
- manuální modelování

## Formáty
Prostředí OpenGL
- VRML -> X3D (vrml v xml)
- Java3D
- KML
- SKP, COLLADA 
- 3D PDF
- IFC - objektově orientovaný datový model pro semantické modelování budov a pro oblasti facility managementu
- Multipatch
- DGN
- DWG
- DXF 

## Vizualizace
*souvislost s virtuální realitou*

Autor zde přdstavuje termín virutální reality v návaznosti na [[@slocumCognitiveUsabilityIssues2001]] a popisuje 4 zakladni faktory pro vytvoreni virtualniho prostredi. (**TODO**). VR realizována hw a sw. Dále autor řeší výpočetní náročnost.
- LOD
- pohledové redukce

### hardwarova zařízení
anaglyf - rozklad a skládání barev zpět pomocí brýlí
CAVE - na základě promítání stereoskopického obrazu na stěny kvádru
chroma stereoskopie - kodování prostorové informace do speciální barevné palety
3D LCD 
aj. 

### software
Na standardním počítači myši a monitoru, autor zde sw dělí na dvě kategorie:
1) desktopové
2) webové
Definuje zde pohyb v prostoru, který by měl umožňovat **6 stupňů volnosti** (posun a rotace kolem všech tří os).
Důležitá funkce je 3D vizualizace symbolů. 

# ch5 modely měst
Autor diskutuje možná využití. Plánování staveb -vliv na charakter zástavby. 3D katastr nemovitostí, facility management, produkotvody, analýzy šíření signálů, krizový management - analýzy. zhs, propagace a prezentace měst - arch. památek, 
## typologie modelů
dělení podle: podrobnosti, zobrazeného území, účelem
1) reálnost - míra geom detailu a textury
	1) 2d
	2) 360° výhled z jednoho bodu
	3) blokový model - extrudování o h
	4) blokový model - otexturovaný
	5) blokový model s arch. detaily
	6) plně objemové CAD modely
1) porizovani dat
	1) pozemni snimkovani - foto fasád a zdí
	2) panoramatické sním - z aut, lidí atd. (google street view)
	3) letecké sníkování
	4) lidar
5) podle funkcionality
	1) estetické - vizualizace zastavěných oblastí - pomocí grafických formátů
	2) proprietární - analytické funkce omezeny
	3) analytické modely 
	4) hybridní - kombinace virtuálních s fyz. reprezentacemi

## Příklady řešení
Virutal London
City GML - Berlín, Heidelberg, Stuttgart

Prezentace pomocí virtuálních glóbů, [Virtual Terrain Project (vterrain.org)](http://vterrain.org/)
Tvorba modelů v ČR Geodis

Autor dále uvádí přehled akademických prací řešících 3D města. 


# ch6 City GML
Standardizovaný formát umožňující modelování geometrie, topologické, semantické a atr. informace. Dále modeluje třídy objektů a vztahy mezi nimi. Složen z logických semantických celků - který odkazuje na určitý typ geometrie. Formáty KML a VRML neumožňují semantické modelování - budova je tedy jen množina polygonů. 
Obecně se CGML skládá z vertiálních  - tematické entity a horizontálních složek - strukturu.
Standardizace a spolupráce na GML skrze SIG 3D. 

Autor dále vysvětluje koncept víceúrovňové reprezentace. **LOD** City GML modeluje úrovní. V rámci jednoho modelu mohou být použity prvky z různých úrovní. 
- LOD0 - model terénu / footprint 
- LOD1 - budova beze střechy
- LOD2 - střechy a balkony
- LOD3 - okna atd.
- LOD4 - interier 

## Geometrie
Objemové - datový model hranic
Vše georeferencováno 
Opakující se prvky - ImplicitGeometry - vlastní kotevní systém - odsazení od geodetického souř. sys.
Koncept *ClosureSurface* - umožnuje modelování povrchových struktur nezávisle na vizualizaci. 
*TerrainIntersectionCurve* - slouží k topologizaci vztahu objektů a terénu

## Topologie
Není použto GML topologie. Sdílení ploch, hran a vrcholů řeseno pomocí *xlink* (viz. CityJSON - vylepšuje..). Geometrie se tedy definuje jednou a následně je na ní odkazováno pomocí Linků. Objekt v city GML může být namodelován geometricky i topologicky. 

## Textury
Textury nejsou jen vizualizační ale i k analýze. *Multitexturing* - pro jeden model exituje více textur a mění se pomocí *themes*. Umožňuje i X3D material. Připojeno promocí ImageURL. Následně se deklaruje způsob umístění textury. 

## Semantika
*popis tříd implikovaných v CityGML*

ISO 19109 
Entity jsou zjednodušeniny objektů irl. Vztahy v UML. Zákl. semant. třídy: budovy, modely terénu, hydrografie, landuse, vegetace a dopravní objekty. 
**Struktura**
- CityObject
	- ReliefFeature
		- _ ReliefComponent - RasterRelief, TINRelief

Nejvíce rozvinutá je semantika budov -> _ AbstractBuilding trida obsahuje všechny další instance. 

## Rozšiřitelnost 
Pomocí dvou konceptů 
- generické prvky v CityGML - doplnění
- ADE - definováním nových tří a prvků o zvláštní atributy a vztahy. Pomocí XSD. Nová třída musí být odvozena z abstrakní nebo konkrétní třídy z vanila CityGML. 


# ch7 CityGMl v praxi
propojení s webem a jinými formáty, vývoj aplikací na prohlížení a tvorbu modelů, tvorba ADE

## CityGML na webu
Propojení s OGC webservices - WFS, CSW, WPS aj.

## Kompatiblita
Definování materiálů v CityGML - XSD a COLLADA, VRML a X3D do CityGML.

## Software podpora
*výčet softwarových řešení pro práci s CityGML*
FME podpora pro CityGML, další klasické desktop 3D softwary - autodesk, SketchUp
Podpora na serveru 
OpenSource podpora - 3D City Database (oracle)

## Příklady ADE
**Hlukové mapování** - Rozšíření umožňoje modelovat data o hlučnosti vozovek aj. objektů a šíření hluku v rámci zástavby. 
**Tunnel ADE**
**Bridge ADE**
**Hydro ADE**
**CAFM** - rozšíření budov v interiérech 
aj. 



# ch8 Tvorba modelů
Modelování dvou variant - první vizualizační druhá analytická (Noise ADE). 
Autor uvádí východiska a podmínky pro zvolené přístupy k modelování, následně uvádí stávající přístup k modelování v rámci světa. 

## vstupní data
Hlavními vstupními daty pro modelování je model od GEODIS, ZABAGED a vlastní mapování.
Footprinty, výšky budov. terén, dopravní komunikace, landuse, vegetace (ZABAGED)
Vstupní data: blokový model od GEODIS -> footprinty okapové čáry v nejvyšším bodě střechy. Atribut výška absolutní a relativní. 
Vlastní mapování spočívalo v:  
- Doplnění potřebných atributů (využití , typy střech - číselník).
- Klasifikace budov pro texturování (barva fasády, počet pater, barva střechy).
- Data o komunikacích (povolená rychlost,), data o protihlukových bariérách.  
- Extrakce z dalších zdrojů - Hluková mapa pozemní dopravy, intenzita dopravy

## použitý software
FME, Arcgis, Photoshop, 

## Zpracování dat
**Předzpracování**
Extrakce, agregace a doplění atributů., tranformace a georeferencování rastrů
**Tvorba hluk. modelu**
Popisuje workflow v rámci FME a klade důraz na vytvoření správně sturkturovaného modelu, validní názvy tříd a jejich uspořádání. 
**Tvorba modelu pro vizualizaci**
Budovy jsou v tomto případě složeny z MultiSurface namísto Solid geometrie. Modely jsou pokryty texturami. 
**Export modelů**
3D PDF, VRML, ESRI Multipatch



# ch9 Diskuze
Autor v rámci diskuze hodnotí: 
- Data a potřebu jejich manipulace v ohledu na tvorbu CityGML modelu.
- Použité softwarové nástroje a dokumentaci ke specifikaci

Data navazovala dobře, 
S rostoucí velikostí CityGML špatná manipulace.

# ch10 Závěr
CItyGML komplexní
Autor hodnotí CityGML z hlediska jeho budoucího vývoje a návaznosti na INSPIRE
Autor zmiňuje CityGML jako výrazného hráče v budoucnosti 3D (**TODO**)




	

