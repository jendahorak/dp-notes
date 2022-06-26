---
title: Building VR and AR experiences using HTML | HTTP 203
authors: 
year: 2021
---
url:  https://www.youtube.com/watch?v=XF29nLkkeLo
zot: [See in Zotero](zotero://select/items/@googlechromedevelopersBuildingVRAR2022)
status:
# Building VR and AR experiences using HTML | HTTP 203

WebGL scene
- webxr requires user interaction

If someone wants to deliver XR experience on the web
- create app for every device
- make it on the web and use WebXR

# WebGL
How to not work with it
## Three.js
## A-Frame
- web component wrapper for Three.js
- writing 3D using markup - VRML - its like it
- simple to get into
``` html
<a-scene>
	<a-box position='...' rotation='...' color='...'></a-box>
</a-scene>
```
- in VR units matter - users have a height
- default units - meters, y - is up
- sky is a inside out sphere - with a texture 


### Div for Aframe
``` html
<a-entity>
```
![[Pasted image 20220626193956.png]]

Custom entity can be defined

Normaly WebXR is WebGL only 
- API that is possible to be placed HTML element on top of WebGL scene
- in AR objects get ligting of a scene
- anochors the placed objects


## Babylon.js
## PlayCanvas
## Wonderland engine
## Unity



