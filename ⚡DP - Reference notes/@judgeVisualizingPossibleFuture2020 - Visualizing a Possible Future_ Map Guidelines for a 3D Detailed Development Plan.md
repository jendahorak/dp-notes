---
title: Visualizing a Possible Future: Map Guidelines for a 3D Detailed Development Plan
authors: Stephanie Judge, Lars Harrie
year: 2020
---
url:  https://link.springer.com/10.1007/s41651-020-00049-4
zot: [See in Zotero](zotero://select/items/@judgeVisualizingPossibleFuture2020)
status: #done
# Visualizing a Possible Future: Map Guidelines for a 3D Detailed Development Plan

# Přínos do DP
- Potvrzení že přechod ke 3D je dobrý, potvrzení že interaktivita je žádaná. 
- Vztah mezi přechodem 2D do 3D a vývojem daného záměru. Na začátku 2D dobrý - čím detailnější tak tím víc 3D potřeba. 
- #todo zjistit ekvivalent DPP v cr - ekvivalent k DPP je ÚAP, popř. ÚS - #todo zeptat se v práci
- prerekvizita pro rozšířené využití 3D DPP je 3D model města
- počítačová grafika je prevaletnější v tomto zaměření nežli 3D GIS
- Vizualizace závisí na:
	- DoA
	- LoD
	- grafické proměnné
- Kibria et al. (2009) - LoD should match the planning phase
Rady:
1. vyhnout se vizuálnímkonfliktům v 3D prostoru - stínování, průhlednost
	1. transparentnost good nakonec
	2. stíny na webu dynamické a volitelné
2. nedělat vysoce realistické viz.
3. Minimalizovat text
	1. nepřehnat jednoduchost

- 3d semantic model - retaining attributes
- Detailně sdělit co daná vizualizace zobrazuje - o to víc pokud LoA je nízké
	- explicitně: text
	- implicitně: vizuální pomůcky
	- 

- Otázky v dotazníku

# Shrnutí
DDP - detailed developement plan legally define what can be built on a specific property. 
Good visualisation is important so movement into 3D *interactive* maps. This sentiment may be beneficial in communication improvement between public and plan proposal.  DPP znázornuje co by mohlo být postaveno v dané oblasti. Z toho plyne že v rámci vizualizace musí být znázorněna nejasnost (uncerainty).
Článek shrnuje a implementuje pokyny k tvorbe 3D podrobných vývojových plánů. 
Evaluace spočívá v semi strukturovaných dotaznících s profesionály v urbánním plánování. 
Přechod k 3D PVP vizualizacím byl ohodnocen jako důležitý k vývoji participace a obecného pochopení procesu územního plánování, za předpokladu že cartografické postupy a funkce jsou korektně aplikovány. 

# Intro
ÚP a goevizualizace jsou úzce spjaty v celém procesu up.
Jednou casti v procesu jsou DPP - PVP - oficialni uredni dokument o parametrech nových budov
Možné parametry: 
1. prostorové limitace
2. výška
3. explotation grade - footprint / total plan area
4. single building max / min size

Možné realizace jsou k PVP doplňkem. 
Z kartografického hlediska se jedná o mapování neznámého / uncertain. Z legálního hlediska - veškeré budovy v PVP jsou možné k postavení. PVP vizualizace by tedy měla vyjadřovat určitou úroveň nejasnosti, aby uživatel věděl, že je "na výběr". **3durban design**- (Wanarat and Nuanwan 2013; Biljecki et al. 2015; Combrinck et al. 2015; Herbert and Chen 2015; Onyimbi et al. 2018). 
3D je populární v urban designu 
**plus** - větší zájem ze strany veřejnosti
**mínus** - zvýšená víra v PVP viz. - kort když jsou fotorealistické
-> vede to k tomu že je nutný správná kartografická vizualizace

**Development**
1. 2D -> 3D
2. static -> interactive web based systems (zoom level, observation points, retrieve infromation)

### Cíle práce
- vylepšit DPP vizualizace
- zlepšit přítomnost veřejnosti
- vytvořit kartografický návod pro tvorbu 3D DPP
- metodika k vizualizaci nejastnosti
- 2D to 3D viz. improvement? 
- Hlavní otázka výzkumu: jaké kratografické metody použít aby bylo vylepšeno předání informace veřejnosti
	- konkrétní PVP - jsou velice informačně plné - barvy, symobly, text


# review of 3d visualizations
**obecně**
- (Kibria et al. 2009) - vnímání vizualizace se zvyšuje při přechodu na 3D, preference 3D viz se zvyšuje s konkretizací vývoje budov, 2D plány a vizualizace jsou dobré v prvotních fázích plánování
- (Wanarat and Nuanwan 2013) - iterace hustoty budov - komunikativní aspekt s verejnosti byl zapřičiněn 3D
- (Herbert and Chen 2015). - 3D přidává kontext do vizualizace návrhu - využití stínu
- Biljecki et al. (2015) - 3D city model aplikace: UP je běžná
- Julin et al. (2018) - 19 model měst velkým měst ve finsku spíš z oblasti počítačové grafiky  a né 3D GIS
- Stouffs et al. (2018) and Sun et al. (2019) - BIM -> CityGML

**geovizalizace / kartografie**
- Herbert and Chen (2015, p. 22) - "the cartographic theory that may inform these geovisualizations generally trails the technology,
- photorealistic vs  symbolic representation
	- domain expert prefer symbolic
	- photorealistic - moc infromace?
- (Semmo et al. 2015; Peters et al. 2017) - kombinace obe strany DoA (Degree of Abstraction)
- LoD - viz. je vylepšena zjednodušením (Kada 2007; Fan and Meng 2012; Baig and Abdul-Rahman 2013; Mao and Harrie 2016)
	- perfomance
	- vizuální kvalita
- Jaké použít grafické proměnné?
- Neuville et al. (2018) - grafické proměnné které jsou v konfliktu ve 3D 
	- stíny
	- průhlednost
	- ideální "view point" - tak aby se nepřekrývalo

**gaming industry - cp graphics**
- (Alatalo et al. 2017) - vzhleda a interaktivita je lepší
- (Reika and Weimin 2011; Yan et al. 2011) - game like 3D prostředí ve hrách pro ÚP - architektura 
- Laksono (2019) - data do game enginů problémy
- Mather and Robinson (2016) - vyuziti existujicich hernich prostredi
- Ljungblom et al. (2017) - převzetí barev z 2D úp do 3D, spíš málo textu v 3D viz. - měl by být nalezitelný 
- Herbert and Chen (2015) - lepší volumetric stíny než ground-draped stíny, transparentnost a spíše modrá barva než šedá, text = vizuální bordel, možnost měni angle a pozici jako největší advantages 3D modelů

 **uncertainty**
 - intrinsic - barva, průhlednost - (Djurcilov et al. 2002; Seipel and Lim 2017)
 - extrinsic - (e.g., Bevis et al. 2017) - 3D - sequences of alternative visualisations
 - Jones et al. (2013) - 3D building objects uncertainty
 - Dübel et al. (2017) - prioritizovat informaci a jen to co je důležité zobrazit v největším detailu
 - Smallman and St. John (2005). - display should higlight task-relevant info

**public participation**
- aby participace veřejnosti byla úspěšná veřejnost musí pochopit prezentovanou informaci
- Alatalo et al. (2017) - 3D vis se ukázali jako užitečné pro zajištění komunikace mezi veřejností a profesionálama - 3D dělá - Integration a Independence
- Onyimbi et al. (2018) 3D web based city models for electronic participation - efficiency in which 3D envs could be understood depends on prof. background
- Lantmäteriet 2019 - The Swedish Mapping Agency - 3d viz == cesta k dosažení digitálního dialogu


# Methodology
Improvement of DPP vis thru web based models. 
Jaké viz. jsou preferované? - kvalitativní výzkum, více holistické a více do hloubky
Rozhovor je lepší než dotazník
Semi strukturovaný rozhovor použit

**Jak to dělaly**
- 4 varianty vizualizace
- různé kartografické principy
- kvalitativní analýza s experty 
![[Pasted image 20221016114508.png]]


##  Map design
 **Co**
 - reálná developement area

**Preliminary Map design**
Rady:
1. vyhnout se vizuálnímkonfliktům v 3D prostoru - stínování, průhlednost
2. nedělat vysoce realistické viz.
3. Minimalizovat text

Výsledek: 4 různé verze - (Judge 2019).
1. Barvy z origo UP - kategorizace
2. detail v okolí a malý detail v zájmovém území
3. stejné jako 2. ale detailnějí okolí - textury nd such
4. abstraktní vzhled obou

**Nejasnost metody**
Rady:
1. nepoužívat intrinsic metody jako barvy a průhlednost k reprezentaci nejasnosti
2. nekombinovat moc 3D geodata a tematickejch dat dohromady

Byly vybrány extrinsic metody - porovnání více možných scénarií

## Vstupní data
![[Pasted image 20221016115905.png]]


## Implementace
### Requirement specification
1. import data
2. share data with participants
3. možnost porovnat dvě různá scénaria

Vybrán by CityEngine - umožnuje porovnávací mód

### Postup
DPP -> FME -> shapefiles -> Arcmap -> City Engine -> CGA -> 3D semantic model retaining attributes
Jen pro jednu lokaci
3 scénária pro lokaci: 
- possible realization of buildings
- maximum height building envelopes
- existing buildings in area

Export do CityEngine Web scenes -> ArcGISOnline -> CityEngineWebViewer



### Interviews
- profesionals
- small sample size

Účastníků byly zaslány otázky a link na web, před samotným rozhovorem. Open-ended questions. 
Zpracování výsledků z rozhovorů -> přepsání, sumarizace
Na základě sumarizace byly mapové doporučení upraveny do finální podoby. #todo tabulka s requirementy (https://docs.google.com/spreadsheets/d/1w4R7GDaF5KIg1SgezoQR7L2xmP4-g6dlz08aWVMprqg/edit#gid=0)
![[Guidlines.png]]


# Discusion
Standardisation and Guidlines
Autoři tvrdí, že je potřeba standardizovat 3D vizualizace UP. Města by měla mít takovéto produkty aby docházelo ke komunikaci. Vizualizacční standard (map guidelines). Software and web aplication / technologies are limitations for achivemenet of desired funcitonality. Standardizace je a softwarový vývoj je neodvratně propojen pokud se jedná o 3D digitální prostředí. Vzít si inspiraci z herního průmyslu, ale nutné rozlišovat mezi herním a utilitním softwarem. 

# Conclusion
Cíl: zlepšit DPP vizualizaci za účelem zlepšení participace veřejnosti

Dosažení: 
Vývoj kartografických doporučení
Evaluace metodologie pro mapování nejistoty
Diskuze o benefitech interaktivních webových 3D územních plánech
Semi strukturované rozhovory s profesionály
3D vizualizace napomáhá v komunikaci možností

Zlepšení vizualizace není  jediným klíčovým faktorem ve zlepšení veřejné participace. 
Vizualizace je nedílně propojena s technologií, kteoru využívá.



# References 
- [x] [[@onyimbiPublicParticipationUsing2018 - Public Participation Using 3D Web-Based City Models_ Opportunities for E-Participation in Kisumu, Kenya]]
- [x] [[@rautenbachEvaluatingProceduralModelling2015 - Evaluating procedural modelling for 3D models of informal settlements in urban design activities]]
- [ ] [[@herbertComparisonUsefulness2D2015 - A comparison of usefulness of 2D and 3D representations of urban planning]]
- [ ] [[@biljeckiApplications3DCity2015 - Applications of 3D City Models_ State of the Art Review]]
- [ ] [[@laksonoUtilizingGameEngine2019 - Utilizing A Game Engine for Interactive 3D Topographic Data Visualization]]
