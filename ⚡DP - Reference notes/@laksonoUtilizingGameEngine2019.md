---
title: Utilizing A Game Engine for Interactive 3D Topographic Data Visualization
authors: Dany Laksono, Trias Aditya
year: 2019
---
url:  https://www.mdpi.com/2220-9964/8/8/361
zot: [See in Zotero](zotero://select/items/@laksonoUtilizingGameEngine2019)
status:
# Utilizing A Game Engine for Interactive 3D Topographic Data Visualization

# TODO
Vytahat další literaturu
[[@trubkaWebbased3DVisualisation2016]]

# Abstract
Using real world data is chalanging task
- Unity3D - large scale topographic data 
- data from LIDAR a topo maps
- LOD 3 - buildings - FBX
- Mapbox for GIS - roads and geolocation
- Unity for interaction
- Result - multiplatform 3D vis. capable of siplayin 3D models in LOD3, user interfaces for exploring on the ground and from the air. 


# Intro
- Virtual globes - Google Earth, Cesium
- 3D world data interaction
	- evni. proteciton
	- disaster response
	- platform colaboration
- 3D in games
	- interactive vis.
	- game engines good for vis. of geospatial data 
		- BIM, Archeology, Architecture etc.
- Game engines are better than virtual globes in interaction
	- FPV - first person view
	- data format support
- Game engines have potential in geospatial application because  *high user interaction with large-scale topographic databases derived from different data sources, which can be useful for supporting human analytical reasoning and communication*.

Authors address a challenge in utilisation of mixed sources of large scale topographic data into a game engine for more meaningful 3D vis.
Autor dále uvádí že herní enginy jsou vhoné pro vzdělávací aplikace a nejen pro hry. Uvádí příklady: vzdělávání simulace, škola hrou, vzdělávání ohledně katastrof, militární simulace a vizualizace měst, ochrana přírody. 
Dále autor uvádí příklady, kdy byly herní enginy využity k vizualizaci irl dat. 

Práce se snaží představit možnosti Unity3D pro vizualizaci univerzitního kampusu. 

## Data 
Footprints, roads, terrains - topo maps
LOD3 models - LIDAR
atributes a visualisation - added manualy


# Related work
Three dimensional platfroms are common with interactivity features.  - WebGL
Research into geospatial-related application
- Popis unity - geospatial?
- Mapbox Unity SDK - slippy map tiles from mapbox - terrain - 

# Metodika
## Předzpracování dat
- 1:2500
![[Pasted image 20220623141730.png]]

- 2D topographic data 
	- buildings, roads, parks, city forests, fields, contours - Mapbox Tile Set
	- Into Unity -> Unity Game Component
- 3D - DXF - Blender (simplification) - FBX - Unity

Mapbox for Unity was used to overlay both datasets into Unity3D. 

### Layers:
Imagery,Terrain - Mapbox slippy maps
Vector - Mapbox tile sets

### Scripts and modifiers - skybox
- Colliders
![[Pasted image 20220623142550.png]]

Most importat was to place accurate 3D model into real world position. It was rotated and rescaled. To position it it was used *Replace Feature Modifier*. 
![[Pasted image 20220623142749.png]]

## Interaction
User logic  - C# scripts for user navigation 
UI - buttons - Minimap, FPV, Drone, Reset Camera position, Help
**Minimap** - C# script
UI with Unity UI and controled with C# 

**Logical flow of application UI**
![[Pasted image 20220623143142.png]]

**Scripts**
- mouse movements
- displayed information
- covnerted user screen to coordinates
- UI
- loaded attributes


# Results
- Online version - interactive 3D viewver - Unity WebGL converter - Unity web - Apache server
- Windows and android version 

# Discussion
Poor performance - Loading data Tilesets - from server
Tiling of 3D model?  - more research into optimissation
Problem with multi accuracy data

**#TODO** Further usability assesment - narative cartography - story telling - 
 
# Conclusion
- Unity and Mapbox - https://geoinsight.ugm.ac.id/ugm3d. 
- 