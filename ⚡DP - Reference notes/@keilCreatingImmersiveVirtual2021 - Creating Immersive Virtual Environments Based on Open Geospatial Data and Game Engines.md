---
title: Creating Immersive Virtual Environments Based on Open Geospatial Data and Game Engines
authors: Julian Keil, Dennis Edler, Thomas Schmitt, Frank Dickmann
year: 2021
---
url:  http://link.springer.com/10.1007/s42489-020-00069-6
zot: [See in Zotero](zotero://select/items/@keilCreatingImmersiveVirtual2021)
status:
# Creating Immersive Virtual Environments Based on Open Geospatial Data and Game Engines

# Creating Immersive Virtual Environments Based on Open Geospatial Data and Game Engines

- [ ] literatura 
	- [ ] First approaches already exist (e.g., Edler et al. 2018a, b; Hruby et al. 2017; Lütjens et al. 2019) t
	- [ ] + zalozky rozklikane
	- [ ] Petridis et al. 2012).
	- [ ] (Biljecki et al. 2015; Haithcoat et al. 2019; Ribarsky 2005)
	- [ ] (Kersten et al. 2018; Mütterlein 2018; Noor 2016).
	- [ ] (Caserman et al. 2019)
# Abstract
- game engine - 3D allow users to creeate realistic 3D enviroments with terrains artifical object easily and swiflty
	- effortless implementation of VR compatiblity
- egocentric and stereoscopic perspective
	- better immersion than *classical screen*
- usefullnes outside of gaming industry: construction planning, spatial hazard sumulations, historical places
- free data - but not standardized format - format transformation needed 
- #dmr #unity #opennrw
- advantages and disadvantages of different sources, VR compatiblity is described


# Introduction
- data geoprocessing - complex 3d landscapes in VR
- two methodological aproaches 
- VR -> better immersion -> being present in the representation
- level of immersion doesnt depend only on general VR chars. such as stereoscopic perspective, tracking  etc. but also on quality of the used geospatial data ad technical chars of the used HMD

# The Potential of VR for Multi‑perspective Research Approaches in Geography
- VR 3D allows synthetizing approach to geographic work 
	- subdisciplines such as urban planning and spatial perception research can be combined
- VR is characterized by immersion which considerably intesifies the communication of spatial information
	- Immersion describes the potential of a technology to create a feeling of presence in a virtual enviroment
	- so it is similar to real  space more
- Integration of differnet geospatial data formats and geospatial datasets 
	- building information
	- urban climatological data
	- elevation data
	- vegetation data
	- noise data

# Creating VR Enviroments 
## Engine
- free engines Unity, Unreal, CryEngine
- enviroments can be percieved thru immersive stereoscopic perspective
- much more tools to present data  - argument v práci #todo
- examples
	- archeology
	- history
	- urban planning
	- solar energy potential
	- hazardous enviroments exploration
	- underground mine 
	- spatial user studies - all distractor stimuli can be eliminated and arbitrary visual and auditory stimuly can be rpesented at desired location

	## Open data
	 Advantages - if resolution good enough - realism, lot of data has been gathered  - easy to get #comment Neplatí pro všechna data, ještě když chceme data s dobrým rozlišením / realismem. 
**Problem**
- multiple data formats
- required transformation

## Geospatial data
vegetace
landuse
state boundaries
terrain
residential propperty

## Focus on DEM a 3D city models
## DEM
Quality of DEM is reflected by - reliability of measures, spatial data resolution, hustota
- arguments on why VGI a lowcost DEM is bad
- Open.NRW DEM - 1m res
- Unity max 4097x4097 terrains larger than that data point losses 
- .xyz -> - QGIS - .tif - GIMP -> grescale - .raw - 2049x2049
- rescale back to original tile size in Unity, depth 8bit and flip verticaly (gimp other rotation)

## 3D city models
spatial representaiton of natural and artificial spatial elements as buildings, roads and vegetation
Quality parameters
- spatial accuracy of object location
- level of detail

**Aproaches to generating 3D city modes**
Automated - aerial photography, laser scanning, cadastral information - consisten LOD
Manual - modelling and placement of 3d models by hand - inconsitent LOD

![[Pasted image 20220626174229.png]]

**Official vs VGI based 3D models***
Official - CityGML - LOD2 - Berlin, City of New York, Den Haag, Kolin - tilex 2x2km - Unity doesnt support CityGML - *citygml - tools* - tranformace do CityJSON - *Blender CityJSON Plugin*- import do Unity

OSM - *blender osm* - differences in LOD - 

# Increasing Immersion and Presence with VR
- Adding VR capabilities to a virtual 3D enviroment helps to create a sense of presence within this enviroment
- sense of presence have been found to imporve procedural memory, interpretation, of volumetric data and performance on visual tasks as mental rotation navigation and te formation of cognitive maps
- Unity implementation
	- SteamVR plugin
- Main immersive characteristics 
	- binocular displays - presents the virtual enviroment in a stereoscopic perspecitve
	- tracking


## What affects immersion
**Resolution**
- resolution of HMD screens - malá - malá imerze - good performance X velká - good data - velká imerze - bad performance (GPU)

**FOV**
**Frame rate**
- visual lag - VR sickness
- high frame rate is imortant - 90Hz

**Type of tracking system**
- inside out tracking 
	- cameras to record the enviroment around
	- calclate HMD location based on the location of object in the enviroment 
- outside in tracking
	- record tracked space form fixed locations or use base statiosn 
	- tracking accuracy doesnt depend on availability of sufficient spatial elements
	- HMD must be fixed 
	- less flexible
- 
# Summary
- VR has been identified as a promising approach to representing interactive geographic applications. 
- Availability of spatial data and free sw (engines) enable cartographers to create immersive 3D VR enviroments. 
- Immersion does not only depend on the quality of the used geospatial data but also on hardware characteriics. 


