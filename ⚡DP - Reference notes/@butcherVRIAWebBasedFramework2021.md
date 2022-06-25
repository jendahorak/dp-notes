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
- starting assumption - dataset for visualisation - JSON or CSV
![[Pasted image 20220624104713.png]]

## VRIA Builder - Beginners
- non-programmers
- packaged with VRIA Node.js package
- learning grammar of VRIA
- rapid protoyping and iterative developement
- GUI wrapper for VRIA scenes
- browse gallery of example plots 

## Non WebVR devs
- new React project - A-Frame scens
- config files can be written 


# The framework
![[Pasted image 20220624105522.png]]
- browser acts as a rendering engine - WebVR manages the interaface with HMD - or non immersive displays - WebGL handels hardware acceleration - 3D managed by Three.js and wrapped by Aframe - on top UI controled by React and D3
- nodejs module written in React and Aframe
- Aframe - entity component framework that provides declarative, extensible and composable structure to Three.js
- Three uses canvas, SVG of WebGL as a rendering engines and features a scene-graph, cameras, navigation modes, shaders and material support.
- VRIA thru Aframe supports all major HMDs - 6 degrees of freedom
- More importantly - Aframe exposes DOM scene graph which is used by React to update only the parts of scene that  require rerendering.  
- Searching, modifying, adding and removing nodes from HTML DOM are very fast - repainting large parts of the DOM tree is expensive
- React uses *virtual DOM* - to calculate difference in the HTML DOM berfore and after a change - so only affected nodes get rerendered. 

## How does it work
- dataset + vis. config. file => immersive visualization 
- ![[Pasted image 20220624110527.png]]
1. interpretation of config file
2. mapping of data to graphical marks and their visual encoding channels
3. mappings are passed thru renderer which constructs the vis. - UI controls - axes and legends

config interpetation and data mapping happens at runtime - real time respond - details on demand

## Architecture
NodeJS module that exposes React component of the same name plus an API for extended func. 
Exact  architecture is up to user - it doesnt have to be written in react 
It can be integrated in different kinds of applications  as long as it makes use of Aframe scenes to present a vritual enviroment ini which the visualisations can be placed
![[Pasted image 20220624111350.png]]


**vis config**
- dataset, type of graphical mark to use and set of visual encoding channels which ap to individual data points (x,y,z, color, opacity etc.)
- in JSON file or as  JS module
- custom can be created with Aframe and VRIA API

## VRIA API
- sufficient built in flexibility to design basic charts for many differnet applications
- more customisation? - ability to customize axies, titles, legends and UI controls thru vis config
- custom marks or interaction -> VRIA API 
- any primitive shapes, models, animation and any physics based UI controls (buttons, sliders atd.) can be created with Afreame and then integrated into vis. via API and *vis config*. 
- API reports current state of each vis. including all current visible data points
- usefull to integrate other tools
- data transofrmations can be implemented from this data with existing libarries

## Interaction mech.
- A frame provides progresive enhancement
- should work on all devices
- *selection*, *filetering*, *detail on demand* - facilitated through a set of interaction types which can be selectively enabled or disabled via the *vis config*
- brushing and linking

## Performance and scalability
- most challanging to maintain FPS
  If frame budget is exceeded the browser is unable to render a new frame which results in a lost fram, leading to uncomfortable VR exp and cybersikness
  optimisation is necessary
- labeling can have impact on render speeds - VRIA uses Signed Distance Field fonts - crisp edges with good perforamance
- performance opts. incorporated at the React level and are intended to provide fine control on when the componet should be updated.
- *shouldComponentUpdate*
- opts. in Three level - reuse and emrgin of object geometries to save on memory and the number of draw calls per frame
- complex scene - chppines - jank - "debounce" - limiting the rate at which a funciton can be triggered. Batching computations over multiple frames and only render the result once. 

# UseCases
## cartesian plots
- simple cartesian plots - mapping data fields to x,y,z  in vis. config

## Interaction
- selectively enabled or disabled - in config file - selection and filtering tools
- new interaction thru VRIA API

##  Assets - Embeded visualisations
A-frame assets - upon which data can be embeded
What assets:
- Aframe primitives
- models
- combination of those


## Linked views and custom marks
Allows for one selection be linked to another
- linking is done via the *vis config views array*
- mark type and and encoding channels

## Multiple users
Support for colaborative enviromets - real time interaciton - can be integrated with existing JS networking libraries to offer func. 
- Aframe component - WebRTC and WebSockets


# Limitations and future work
*Vis. types* - Cartesian plots  - other geographical systems **#TOOD** 
*Data model*- tabular JSON or CSV - next work - hierarchical, network , relational data models - node linked diagrams - GeoJson TopoJSON
*UX* - 
*Visual Vocab. and Immersive Analytics* - suitable vocab. for VR/MR worlds that facilitates visualisation pipelinie. 
*Future dev* - aggregation, binning and other more advanced filtering operations, build vis inside VR
*XR* - 

# Lessons
3 years from simple, single stand alone Aframe vis application of a 3D barchart to the current framework

## Chalanges 
1. constantly changing and updating libs and tech - bleeding edge WebXR
2. XR is new - position sensing, computer vision, context awareness 

# Conclusion
Interest in Immersive data visualisation incerases - investigation of vis. techniques tailor-made for immersive 3D graphical enviromets. 