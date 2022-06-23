---
title: Unreal Engine 5: The OpenXR Convergence
authors: 
year: 2021
---
url:  https://www.youtube.com/watch?v=0kRoGjvlXbQ
zot: [See in Zotero](zotero://select/items/@microsoftdeveloperUnrealEngineOpenXR2022)
status:
# Unreal Engine 5: The OpenXR Convergence
#  Unreal Engine 5 
- good tools, profesional
- OpenXR - free open standard for devices and platforms - middle man pro XR devices
- Windows mixed reality and hololens - API 


![[Pasted image 20220621170017.png]]
3 main parts:
1. Application - here created by Unreal Engine
2.  OpenXR Runtime - Implementation of OpenXR API - exposing features of the platform and device to the app
	1. Device can have multiple OpenXR runtimes (Windows Mixed reality, Meta, SteamVR, others )
3. Device - HMD - output hardware and sensors

![[Pasted image 20220621170913.png]]

App uses OpenXR loader - registry setting pointing to the runtime json manifest file??
Third party apps to see what runtime currently using. 
Multiple devices  
Multiple applications 


# OpenXR API CORE
Khronos - Essential and universal API to make XR functions - device tracking, input. lifecycle of conecting to the hardware
- use of extensions for specific functions such as hand movement - eg. platform specific requirements 


We have OXR a ways to extend it - plugins to Unreal engine
- OpenXR plugin 


# Input
Action based - Input for application - click on mouse/controler 
- needs to be asociated with hardware - cannot be bound to specific 
- how to make it forward compatible - compatible with future hardware
-  Descriptions of physical hardware - interaction profiles - např. microsoft/motion_controler

 ![[Pasted image 20220621174905.png]]

Description of current hardware - binding actions to specific buttons - **Action mapping**
After specifing actions to specific OpenXRRuntime finds interaction profile that best matches and binds it


