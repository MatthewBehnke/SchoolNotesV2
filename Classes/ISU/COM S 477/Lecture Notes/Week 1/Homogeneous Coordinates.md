# Homogeneous Coordinates


## 1. Introduction 

## 2. Planar Transformations 

## 2.1 Translation 

## 2.2 Scaling 

## 2.3 Reflection 

## 2.4 Rotation about the origin

### Example: Robot manipulation 

The u - v frame rotates from the x -y frame through $d_1 + d_2$
 $\Rightarrow p - e = R(d_1 + d_2)(u v)$ 


## 2.5 Shear

## 3 Consecutive transformations 

## 4 Definition of Homogeneous Coordinates

### Example: Intersecting two lines 

$l_1: x -y7 + 8 = 0$ 
$l_2: 3x - 4y + 1 =0$

$(1, -7, 8) \times (x, y , 1) = 0$
$(3, -4, 1) \times (x, y , 1) = 0$
$\Rightarrow (x, y, 1) \bot (1, -7, 8)$  
$(x, y, 1) \bot (3, -4, 1)$  

$\Rightarrow 9x, y, 1 // (1, -7, 8) \times (2, -4, 1)$ = $(25, 23, 17)$
$\Rightarrow (x, y, 1) = (\frac{25}{17}, \frac{23}{17}, 1)$

$(2, 23, 17) \sim (\frac{25}{17}, \frac{23}{17}, 1)$

Equivalence relation on $S = \mathbb{R^3}$
(x, y, x) $\sim$ (u, v, w) if (x , y, z) = r(u, v, w) , r $\not=0$

- reflective (x, y, z)$\sim$ (x, y ,x)
- symmetric (x, y, z) $\sim$ (u, v, w) whenever (u, v, w) $\sim$ (x, y, z)
- transitive (x, y, z) $\sim$ (u, v, w) whenever (x, y, z) $\sim$ (a, b, c) and (a, b ,c) $\sim$ (u, v, w)

All the points on a line through the origin in $\mathbb{R^3}$. except for the origin, are equivalent 

The equivalence class of (x, y, z) is the set 

$[(x, y, z)] = \{r(x, y, x) | r \in \mathbb{R} \text{ and } r \not= 0\}$ 

homogeneous coordinates 

$[(0,0,0)] = \{(0, 0, 0)\}$ 


Projection Plane $\mathbb{P}^2 = \{[x, y, z] | x \not= 0, y \not= 0, z \not= 0\}$ 


## Points at Infinity 

(x, y, 0)? infinity point in the direction (x, y) 



Line (a + tx , b + ty) $t \in \mathbb{R}$

(a, tx, b + ty, 1) $\sim$ ($\frac{a}{t} + x, \frac{b}{t} + y, \frac{1}{t})$

$limit_{t \rightarrow \inf}$ 



## Cartesian | Homogeneous 

- Point : (x, y)  | (x, y, 1)
- line: ax + by +x = 0 | au + bv + cw = 0

Line vector $l = (a, b, c)$
For $x -7 y + 8 = 0$ $l = (1, -7, 8)$


point P = (u, v,w) on the line if P * l = 0

