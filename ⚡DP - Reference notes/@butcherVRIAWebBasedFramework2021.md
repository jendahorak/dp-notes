---
title: VRIA A Web-Based Framework for Creating Immersive Analytics Experiences
authors: Peter W. S. Butcher, Nigel W. John, Panagiotis D. Ritsos
year: 2021
---
url:  
zot: [See in Zotero](zotero://select/items/@butcherVRIAWebBasedFramework2021)
status:
# VRIA: A Web-Based Framework for Creating Immersive Analytics Experiences

# Shrnutí
- WebVR - A-frame, React, D3
- Immersive analytics on the web
- HTML DOM
- platform agnostic


# Immersive Analytics
- novel display methods in reasoning and decision making
- goal to develop - multi-sensory - collaborative - interactive systems that allow users to be immersed in their data
- VR as a medium to IA
- previous work  - viz. [[⚡ DP - Rešerše]]

**Contributions**
 - workflow description
 - how doees VRIA work
 - usecases
 - discusion on limitations

# Motivation and background
WEB = platform independent
- tech. for vis. na webu založeny na otevřených standardech (D3, Processing.js, Ptorovis, Vega)
- daata visualisations který jsou sharable, reusable and cosumable as components that can be integrated with DOM 
- DOM - common abstraction layer comprising of set of intrinsic object fucntions and their properties - canvas, datastructures (JSON), formatting (CSS), WebVR. 
- Alongside DOM Web provides execution enviroment (JS)
- Based on this abstraction - posiblity of consumption among other tech is possible
	- not only re-displaying or extracting base info
- VR apps created with a game engine - and WebGL export - not truly consumable as those build for the web specificly
- WebVR and WebXR - provide link between VR and the DOm via JS
	- open spec API
	- allows VR and MR apps to be in browser - with use of HTML DOM
	- Platform independence beyond browser - detect current user HW setup - *progessive enhancement*
	- VR scene with single codebase - compliant browser - contemporary HMDs, monitors, smartphones
- VRIA high level features -
	- build on open-standards
	- platform independence
	- declarative - Vega-lite
	- sharable, distributable, consumable immersive visualisations
	- VRIA Builder - for noobs
	- VRIA API - for notnoobs 

# Related Work
Work on how to move visualization and data to be platform, sw and hw agnostic. Next work on how VR could be helpful in data analysis. Biggest problems are: display tech., rendering performance, collaboration facilitation and interaction **lack of standardisation**.  -> web technologies

MR - also an interest 
Creating VRIA as a framework upon which researchers can build similar, multifaceted investigations on the Web by combining different peripherals, libraries and system over the unified abstraction alyer that is HTML DOM.

## Immersive Vis. Toolkits
Reliance on game engines is traded for reliance on open standards. 
![[Pasted image 20220623224223.png]]

**Unity based**
- ImAxes
	- IATK
	- DXR - rapid prototyping data visualisations for XR - declarative - rendering as unity game objects - lower performance than IATK where it is single mesh so GPU can do it
		- both can be exported to Web via WebAssembly WebGL export. 
	- VRIA 
		- similar philosophy
		- declarative grammar
		- linked-views
		- custom mark spec. via A-frame ??
		- genuine platform independence
		- vendor-agnostic
		- sharable and consumable output without wasm
	- VR-VIZ
		- Aframe and React
		- Vega-Lite
		- visualisations baked into renderer mechanisms
	- Stardust 
		- GPU based vis. lib
		- WebGL
		- alternative to HTML canvas, D3 and Vega 
		- similarities with VRIA - declarative, web, WebXR

## Influences of Information Visualization Toolkits
VRIA is build as to provide support for contemporary approaches of crating vis. Be viable for nonimersive vis and secondly be primarly for Immersive Analytics - not being an addon to game engine that has wider scope and purpose. 
**Examples**
- vis. specification is is spearated from implementation
- building block for crating custom visualisations - Prefuse - Info-Vis toolkit
- rapid prototyping via configs with Aframe and React components and VRIA API
- D3 for data manipulation

VRIA is similar to Webstrates - Vistrates 

# VISUALIZATION CREATION WORKFLOW




