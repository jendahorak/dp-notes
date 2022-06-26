---
title: An intro to modern OpenGL. Chapter 1: The Graphics Pipeline
authors: 
year: 
---
url:  https://duriansoftware.com/joe/an-intro-to-modern-opengl.-chapter-1:-the-graphics-pipeline
zot: [See in Zotero](zotero://select/items/@IntroModernOpenGL)
status:
# An intro to modern OpenGL. Chapter 1: The Graphics Pipeline

# OpenGL
Cross platform library for interfacing with programmable GPUs for the prupouse of rendering real time 3D graphics. Became standard along Microsofts Direct3d. Khoronos group maintains OpenGL. 

## The Graphics pipeline
Trinagle is the main building block of computer graphics. GPU knows only triangles. 
The graphics pipeline that OpenGL implements reflects this - host program fills OpenGL managed memory buffers with arrays of vertices, these vertices are projected *graphical projection* into screen space, assembled into triangles and rasterized into pixel-sized fragments. Those fragments are assigned color values and drawn to the framebuffer.  "project into screen space" - "assign color values are done by **shaders** 
![[Pasted image 20220626141951.png]]

# 1. The vertex and element arrays
**vertex buffer** -> filled with array of **vertex attributes**  - attributes are used as inputs to the vertex shader
Common vertex attributes include the location of the vertex in 3d space 

# 2. Uniform state and textures
- state contains textures - one, two or threedimensional arrays that can be sampled by shaders

# 3. The vertex shader
GPU reads each selected vertex out of the vertex array and running it through the **vertex shader**  a program that takes a set of vertex attrs as inputs and outs a new set of attrs **varrying values** that go to rasterizer - vertex shader calculates the projected position of the vertex in **screen space** - shader also can generate other varying outputs such as a color or texture coordinates for the rasterizer to blend across the surface of the triangles connecting the vertex.

# 4. Triangle assembly
GPU takes projected verticies to form a triangle. It groups them based on element array into sets of three.  3 ways of making triangles - viz url
![[Pasted image 20220626143954.png]]
# 5. rasterization
Rasterizer takes each triangle clips it and discards parts that are outside of the screen and breaks the remaining visible parts into pixel sizes fragments.  Vertex shader varying outputs are interpolated accros the rasterized surface of each triangle. 
![[Pasted image 20220626144130.png]]

# 6. fragment shader
these fragments pass thru **fragment shader** - outputs color and depth values that then get drawn into the framebuffer - texture mapping and lighting - runs on every pixel drawn - most sophisitcated effects but also most performance sensitive part 

# 7. framebuffers  testing and blending
**freamebuffer** - is the final destination for the rendering job output. 
**framebuffer objects**- draw into**renderbuffers**


# Conclusion
Process from vertex buffers to framebuffers - data goes through when making a single **draw**- call 
Rendering a scene often involves multiple draw jobs - swithcing textures - uniform state - shaders 


