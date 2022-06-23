---
title: Virtual and Immersive Environments
authors: Zdenik Stachon, Petr Kubicek, Lukas Herman
year: 2020
---
URL:  https://gistbok.ucgis.org/bok-topics/virtual-and-immersive-environments
ZOTERO: [See in Zotero](zotero://select/items/@stachonVirtualImmersiveEnvironments2020)
STATUS: #reference
TAGS:  
# Virtual and Immersive Environments
# Shrnutí
1) stručná historie virtuální reality a imerzních prostředí
2) představení obecného přístupu k popisu VE
3) přehled 4 designových přístupů k VE
	1) cognitivní přístup - úroveň vnímání VE
	2) metodologický přístup - metody pro sběr, processing, a vizualizace VEs
	3) technologický přístup - průzkum technologií umožňující input, výpočet a ouptut a to jak HW tak SW (desktop, web)
	4) sociální přístup - představení konkrétních využití VE v různých oborech (geografie, rozhodování, krizový management)

**Co je *virtual enviroment* (VE)**
počítačová 3d simulace reálného nebo imaginárního prostředí ve kterém se uživatel může pohybovat a interagovat s virtuálními objekty. 

# ch01 - definice a terminologie
Přehled používané terminologie
*AR - augmented reality* - real world enviroment enhanced by computer generated information
*CAVE* - Cave Automatic Virtual Enviroment - a  virtual reality enviroment where images are projected onto three-to-six of the walls of a room-sized cube
*depth cues* - prostorová vodítka - vizuální nebo jiné senzorové vjemy podporující percepci třídimenzionálních dat
*XR* - rozšířená realita - obecný termín zahrnující celé spektrum terminologie "realit" - VR, AR, MR
*HMD* - head mounted display - přístroj nošený na hlavě s apaerátem pro vizualizaci
*immersion* - pocit bytí v daném prostředí
*immersive virtual enviroments (IVEs)* - VE představující velice životu podpobnou úroveň imerze
*information density* - realističnost VE a a LOD
*MR* - realný a virtuální dohromady
*pseudo 3D or 2.5D* - monoskopická vizualizace na plochém médiu (pc) 
*monocular - monokulární vodítka* - vizuální vodítka viditelná v 2D reprezentacích a pozorovatelná jedním okem
*binocular - binokulární vodítka* - v.v. vnímatelná pouze dvěma očima 
*real 3D* - vizualizace obashující jak monokulární tak binokulární ukazatele hloubky
*VR* - medium zkonstruované na základě počítačových simulací, které detekují uživatelovy polohu a pohyb - a následně předává jednomu nebo více smyslům zpětnou vazbu tak aby byl dosažen cíl imerze a přitomnosti v daném prsotředí - VR je subset VE

# ch02 Úvod do VE a IVE
*Historie a rozdělení VE a IVE*
Prvním z význých byl CAVE Automatic Virtual Enviroment. Dále se VE rozvíjeli díky rozvoji v oblasti mobilních telefonů a jiných low-cost VR přístrojů, čímž také vznikla stabilní technologická základna pro AR. Vývoj VR technologií je velice dynamický a tudíž se nástroje rychle mění. Charakterizovat je je možné pomocí 4 základních parametrů ([[@shermanUnderstandingVirtualReality2002]]): 1) virtuální svět, 2) imerze, 3) smyslová zpětná vazba, 4) interakce. Tyto parametry by měly být nezávislé na daném technologickém provedení. Dalším z velice významných faktorů definující VR je úroveň realističnosti jakou je VE vizualizováno, což ovlivňuje úroveň imerze a efektivity uživatele interagovat v rámci VE. 

Na kvalitu imerze mají vliv další faktory: 1) technické parametry - způsob vizualizace (stereoscopic), obnovovací frekvenci, úrovni realismu, způsob pohledu (field of view), tracking. [[CV16_Fig2.png]]

## VE v Geoprostoru a kartografii
GeoVE - MacEachren et al. (1999)
popis VE - immersion, interactivity, information density, intelligence - obdobně jako [[@shermanUnderstandingVirtualReality2002]], [[4-is-of-VE.png]]

## CVE - collaborative virtual enviroment - VRChat?
- distribuované virtuální prostředí 
## VR sytem architecture
[components of a VR system](https://gistbok.ucgis.org/sites/default/files/CV16_Fig3.png)

# ch03 zásady a důsledky 3D vizualizace
Monocular a Binocular cues
**Monocular**
1) static - lighting, size, occlusion/interposition, relative size of objects, linear perspective, texture gradients, aerial perspective
2) dynamic - motion parallax, also referred to as kinetic depth
**Binocular**
1) *binocular disparity, convergence*  

Jen monokulární se nazývají pseudo 3D, real 3D využívá obou. Z informačního pohledu oba přístupy mohou být považovány za ekvivalentní, ale každý využívá jiného vjemového kognitivního procesu.  
[depth cues of 3d environments](https://gistbok.ucgis.org/sites/default/files/CV16_Fig4.png)

# ch04 Technologie pro VE
## HW
1) Vstupní HW 
2) výpočetní jednotka
3) Výstupní HW pro vizualizaci e.g. stimulaci jiných smyslů

### Input
Velice důležitý je pohyb - motion capture. Různé způsoby sledování pohybu: akustické, elektromagnetické, mechanické. Nejvíce využívané je optické - kdy jsou sledovány specifické reflexní body na uživateli. Důležitou součástí je IMU (Inertial measuring unit) - sledující rychlost akcelerace a změny v rotaci. IMU nejsou v "low-cost" řešeních. 

Sledování pohybu je často kombinováno s různými specifickými vstupními nástroji, které umožňují různé úrovně [[DoF - degrees of freedom]]. Tradiční desktop platformy umožňují pouze 2 DoF, pohyb v 3D je pak nahrazován klávesovými zkratkami, tedy kombinací tradičních vstupů (přepínání mezi módy pohybu atd.) herní kontroléry umožňují více. 

### Výpočetní jednotka
Úrovně renderování mají vysoký dopad na úroveň imerze ve VE (vysoká snímková frekvence a nízká [[latence]]) . Procesingové jednotky jsou propojeny s vstupními a výstupními technologiemi. [[⚡DP - Otázky a nápady]]

### Výstupní hardware
[[type_of_display_devices.png]]
Možné dělit podle smyslu na který fungují. Hlavní jsou vizualizační, které je možné dělit na tradiční displaye, semi-imerzivní systémy a HMD. Tradiční monitory poskytují pouze monokulární vodítka a nejsou tedy příliš imerzivní. HMD jsou nejvíce imerzivní technologií. HMDs je možné dělit dle výpočetní síly a mobility. 
Mobilní HMDs - Google Cardboard, Google Daydream, Lenovo Mirage Solo, Oculus Go, and Samsung GearVR. -- AR a spolu se smartphonem
Stacionární HMDs - Fove0, HTC Vive, PlayStation VR, and Oculus Rift -- detailní imerze 

*Njevhodnější output zařízení by mělo být určeno primárně na základě účelu daného VE.*  


## SW
CAD, GIS, 3D graphics - engines, photogrametry, web technologies
### Desktop
CAD -> 3D modeling software / GIS modelling (less detailed) -> game engines 
viz. tab. https://gistbok.ucgis.org/bok-topics/virtual-and-immersive-environments
### Web
Z výpočetního hlediska jsou na webu publikovány spíše jednodušší a menší 3D vizualizace, které není možné považovat přímo za imerzivní. Dříve standard VRML je nahrazován technologiemi jako jsou [[3D Tiles]] [[glTF]]  . Dříve 3d vizualizace závisela na pluginech do daného prohlížeče. Dnes se 3D vizualizace staví na HTML5 a WebGL. (three.js, X3DOM, XML3D, SpiderGL). O kompatiblitu webových technologií a VR se stará dříve WebVR dnes WebXR framework. 


# ch05 - Možné využití
Článek zde řeší primárně vnímání terénu a emergency management. 


