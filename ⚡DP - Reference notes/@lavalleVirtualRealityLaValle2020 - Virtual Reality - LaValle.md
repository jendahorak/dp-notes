---
title: Virtual Reality - LaValle
authors: Steven LaValle
year: 2020
---
url:  http://lavalle.pl/vr/
zot: [See in Zotero](zotero://select/items/@lavalleVirtualRealityLaValle2020)
status:
# Virtual Reality - LaValle

# do DP
Dobrý z obecného pohledu 



# Birds eye view
## Software
- Examples available today are OpenSimulator, Vizard by WorldViz, Unity 3D, and Unreal Engine by Epic Games
- locomotion
- physics
- networked experiences
## Sensation and perception
- Classification of senses
- Proprioception
	- efference copies
- Fusion of senses
	- Signals from multiple senses and proprioception are being processed and combined with our experiences by our neural structures throughout our lives. Any attempt to interfere with these operations is likely to cause a mismatch among the data from our senses.
	- bad sensory conflict
		- *vection*
			- caused by the locomotion operation
			- if you accelerate yourself forward using a controller, rather than moving forward in the real world, then you perceive acceleration with your eyes, but not your vestibular organ
				- see Section 10.2
- Adaptation
	- perceptual training
		- human can be adapted to VR motion
	- developers may become comfortable with an experience that is nauseating to a newcomer
		- A large amount of tracking latency has appeared, which interferes with the perception of stationarity.
		- The left and right eye views are swapped.
		- Objects appear to one eye but not the other.
		- One eye view has significantly more latency than the other.
- Psychophysics
	- probability of detection - red or not red
	- Steven’s power law
		- relationship between the magnitude of a physical stimulus and its perceived magnitude

# Geometry
## AWG - geometric modelling of alternate worlds
World that has **geometry** and **physics**. Y aixis is up in game engines.  Models are contructed from triangls because it is computionaly simpler and more efficient.

## Models
1. Stacionary
2. Movable

Choose coordinates wisely. 
Viewing the models
- **where the points in the virtual world should appear on the display?**
- **how each part of the model should appear after taking into account lighting sources and surface properties**

## Representation
- Solid representation - 3D primitives 
- Boundary representations - 2D primitives 

model coherency - better to have solid representation so there is easier colision detection
normals - problem of rendering surfaces, because surface normal switched 

In engines, there are 2D boundary representations - triangles that sit in 3D space. 



## Triangles 
How to glue triangles together. Making a datastructures as a strip or meshes. 
- shared verticies and edges
	- doubtly conected edge list

## Changing position and orientation
Why do we transform?
- Movable objects
- Perception of movement / simulation of stationarity - when CAVE or other fixed system - when moving a head the "outer world" should change - world has to counter rotate
	- in VR HMD it is needed to counter transform real world body transformations 
	- **inverse transformation**
		- requires tracking, estimation of motion
		- we need to know how the body has transformed in real world so we can apply a invere of the transformation to have a **perception of stacionarity**


## Transformation of rigid bodies
Transformation of each vertex of each triangle
3 cases:
1. Translation  - DOFs - in 2D - 2, in 3D - 3
2. Rotation - DOFs - 2D - 1, 3D - 3 
3. Rotation + Translation - place anything anywhere, without distortion of the body

So we have 3 degrees of freedom in 2D and 6 degrees of freedom in 3D
  
**Translation**
viz. sešit

# **Rotation**
2D rotations are easy - one parameter on unit circle - in 2D parameter of theta is proportional to the rotation of the rigid body
- in 3D its not that easy 
- one DOF - one parameter


## 3D rotation - part of rotation
- bigger matrices
- for 3x3 - 9DOFs
	- if we apply all the constraints 
		- No stretching of axes
		- No sheering
		- No mirror images
	- 3 DOFs remaining
		- yaw - y, pitch - x, roll - z 


**YAW**
![[Pasted image 20230115163810.png]]
- undisturbed y coord
**PITCH**
![[Pasted image 20230115164045.png]]

**ROLL**
![[Pasted image 20230115164119.png]]


Sequentialy put together we can get any rotation we want. However there are problems.
1. Order matter 3D rotation not comutative
2. Kinematic singularities 
   

## Quaternions
- 4D vectors with 4 parameters - with constraint that they are on the sphere


## Chain of Transformations so we can see anything in 3D space - where does everything go? and where does it appear?
1. Define bodies (models) in each own local / body frame. -> transformation (rotation and translation)
3. Global frame  include all the models that don't change -> Eye transformation (all the models in eyes coordinates / perspective)
4. -> Canonical view transform - so the graphics operation can be applied easily
5. -> Viewport transformation - render the body onto screen of pixels

![[Pasted image 20230116153545.png]]
![[Pasted image 20230116153811.png]]
![[Pasted image 20230116153858.png]]
![[Pasted image 20230116154013.png]]


transformation pipeline
T = Tdist Tcan Tl Tr Teye Trb
rendering pipeline - figuring out what needs to be thrown away 

We need to figurate a viewing (camera) transform. Somewhere in the world there is a body with a camera. 
**Eye transformation** - expression of all of the points of the world into the coordinate system of the eye

Viewing frustum.
![[Pasted image 20230116184513.png]]


...




# Light and Optics

## How light travels and behaves with  materials
- transmition
- absorbtion
- reflection 
	- specular
	- diffuse
- spektrální rozlišení


## Lenses
How much rays of light bend when entering or exiting a transparent material
... viz. 4.2 Lenses [[@lavalleVirtualRealityLaValle2020 - Virtual Reality - LaValle]]


# Optical Aberrations
## Spherical aberration
- make aspheric lenses

## Optical distortion



# The Physiology of Human Vision
How large resolution to not see the pixels. 


Because of rodes and cones we have scotopic vision (monochromatic) and photopic vision (trichromatic). Into scotopic mode it takes about 30 mins. Going into photopic vision it takes about 10mins.


## Eye movement
1. Saccades
2. Smooth pursuit
3. Vestibulo-ocular reflex
	1. image stabilization
4. Optokinetic reflex
	1. train tracking
5. Vergence - converging and diverging
6. Microsaccades


# Tracking
## 2D and 3D orientation of the head











