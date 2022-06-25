---
title: Essence of linear algebra - YouTube
authors: 
year: 
---
url:  https://www.youtube.com/playlist?list=PLZHQObOWTQDPD3MizzM2xVFitgF8hE_ab
zot: [See in Zotero](zotero://select/items/@EssenceLinearAlgebra)
status:
# Essence of linear algebra - YouTube

# Chapter 1
**Adding vectors** 
![[Pasted image 20220624172716.png]]
Thinking of it as taking steps in value of the vectors - one could walk directly 4 to the right and 1 up instead of 2 up one right and then 3 right and one down.  Better is to go 1 + 3 to the right then 2 - 1 up. 
![[Pasted image 20220624173012.png]]
*Matching and adding.*


**Multiplication by number** - scaling - Scalars 
- multiplying each of the components by two
- ![[Pasted image 20220624173141.png]]
Way to give computer graphics language to describe world. 

# Chapter 2
- each coordinate as a scalar - that scales unit vector (i, j) - so vector 3, 2 is 3 * i and j * 2
- i and j are basis vectors of the coordinate system
- when desrcibing vectors numericaly it depends on what basis vectors are we using 
- scaling and adding is *linear combination* - every possible combination is a span (plocha or linie)

## how to think about vectors 
- one vector - arrow - span is line
- multiple - points - span is plane
- in 3D - pro 2 vektory plocha for real  - pro 4 vektory - 
	- když bude span stejnej jako span x y tak zase plocha
	- everypossible of space
	- když je jeden zbytečnej - linear dependent 

# Chapter 3 - Linear transformations
## Linear transformation
- transformation - function - I/O
	- take some vector and output some vector
	- tranformation as a movement - for space it is every possible vector moving to its ouput vector - therefore transforming the space
- liniar
	- lines remain lines
	- origin mus remain in space
	- grid lines paralel and evenly spaced

How to do it numericly? How to program animation. 
![[Pasted image 20220624180959.png]]
Only where basis vectors land. - other is just a addition and salar multiplication of those basis vectors
![[Pasted image 20220624181234.png]]
 ![[Pasted image 20220624181342.png]]

Complete linear transformation is described just by 4 numbers. Coordinates for I and coords for j.  - 2x2 matrix 
![[Pasted image 20220624181500.png]]
Where does it take the given vector. 
![[Pasted image 20220624181526.png]]
![[Pasted image 20220624181615.png]]
**Sheer** - i remains fixed - 


# - important
Linear transformations are way to move space such as the lines remain paralel and evenly spaced and such that the origin remains fixed. Transformation of space can be desrcibed with coordinates of basis vectors after the transformation. These coordinates are written as a **matrix** . Matrix - vector multiplication is just what that transformation does to the given vector eg. every possible vector (space).


# Chapter 4 
How to describe effect of multiple transforms. 
**Composition** - of rotation and sheer (two separate tranformations)
Like any linear transformation it can be described with matrix of i an j. 

Apply rotation then a sheer to given vector: 
![[Pasted image 20220624183011.png]]
same as
![[Pasted image 20220624183024.png]]
Composition is a product of those before. 

How to do it numericly. - wher does i hat goes 

# Chapter 5  - 3D
![[Pasted image 20220624185826.png]]
Where does the basis vector lands
90 degree rotation around y
![[Pasted image 20220624185921.png]]

When there are matricies multiplied it is just appling multiple transformations  starting with the right one than the left one and so on. Roations of space are dificoult so  it is easier to think about htem as a components of simpler transformations. 

# Chapter 6
How much does transformation squishes space? 
How does given region area changes.  

Determinant of that transformation is number of how much does given area changes. 
Negative value?? - orientation - inverted space whend d = - 



****

