## Index

 1. Shaders <!-- .element: class="fragment" data-fragment-index="1"-->
 2. Traslation, rotation, scaling and sheared --> 2d, nonlinear,.. <!-- .element: class="fragment" data-fragment-index="2" -->
 3. Homogeneous space <!-- .element: class="fragment" data-fragment-index="3" -->
 4.  Traslation, rotation(Euler), scaling and sheared --> 3d, linear,.. <!-- .element: class="fragment" data-fragment-index="4" -->
 5.  Orthogonal Matrix Rotations <!-- .element: class="fragment" data-fragment-index="5" -->
 6. Quaternion Rotations <!-- .element: class="fragment" data-fragment-index="6" -->
 7. Modeling Transformations <!-- .element: class="fragment" data-fragment-index="7" -->



## PIPELINE

<a href ="http://processing.org/tutorials/pshader/">
Shaders
</a>
In Processing
```
uniform mat4 transform;
attribute vec4 vertex;
attribute vec4 color;
varying vec4 vertColor;

void main(){
   gl_Position = transform * vertex;
   vertColor = color;
}
```
```
varying vec4 vertColor;

void main(){
  gl_FragColor = vertColor;
}
```



## Two-dimensional transformations 
<img wigth ="500" height="500" src="lectures/2/fig/image1.JPG">


## Two-dimensional transformations 

<font color="yellow"> Object Transformations vs Coordinate System Transformation</font>

<img wigth ="400" height="400" src="lectures/2/fig/image2.JPG">


## Two-dimensional transformations

<font color="yellow"> Active Transformation (Standard Basis) vs Passive Transformation (change of base)</font>

<img src="lectures/2/fig/image3.JPG">


## Two-dimensional transformations

<p align ="left"><font color="yellow">Traslation</font></p>
<img wigth ="400" height="400" src="lectures/2/fig/image4.JPG" align ="left">
<p align ="right">Vectorially we have:</p>
</br>
<p align ="right"><p align ="botton"><font color="#00FFFF">
$\begin{bmatrix} 
x \cr 
y \end{bmatrix}
\begin{bmatrix} 
d_x \cr 
d_y \end{bmatrix}
\begin{bmatrix} 
x' \cr 
y' \end{bmatrix}$
</font></p></p>
</br>
<p align ="right"><p align ="botton"><font color="#01DF3A">
$
P'= P + T
$
</font></p></p>


## Two-dimensional transformations

<p align ="left"><font color="yellow">Scaling</font></p>
<img wigth ="400" height="400" src="lectures/2/fig/image5.JPG" align ="left">
<p align ="right">Vectorially we have:</p>
</br>
<p align ="right"><p align ="botton"><font color="#00FFFF">
$\begin{bmatrix} 
x \cr 
y \end{bmatrix}
\begin{bmatrix} 
s_x & 0 \cr 
0 & s_y \end{bmatrix}
\begin{bmatrix} 
x' \cr 
y' \end{bmatrix}$
</font></p></p>
</br>
<p align ="right"><p align ="botton"><font color="#01DF3A">
$
P'= S * P
$
</font></p></p>


## Two-dimensional transformations

<p align ="left"><font color="yellow">Rotation</font></p>
<img wigth ="400" height="400" src="lectures/2/fig/image6.JPG">


## Two-dimensional transformations
<table width="350" heigth="500" border="0" align ="right">
<tr>
<td>
<img src="lectures/2/fig/image7.JPG" width="350" heigth="350">
</td>
</tr>
<tr>
<td>
<font size ="5">Vectorially we have:</font>
</br>
<font size ="5" color="#00FFFF">
$\begin{bmatrix} 
x \cr 
y \end{bmatrix}
\begin{bmatrix} 
cos\beta & -sen \beta  \cr 
sen \beta & cos \beta \end{bmatrix}
\begin{bmatrix} 
x' \cr 
y' \end{bmatrix}$
</font>
</br>
<font size ="5" color="#01DF3A">
$
P'= R * P
$
</font>
</td>
</tr>
</table> 
<p align ="left"><font color="yellow">Rotation</font></p>
</font></p>
<p align ="left"><font size ="6">From the triangulation:</font></p>
<p align ="left"><font size ="6" color="blue">
$x = rcos \alpha$
</font></p>
<p align ="left"><font size ="6" color="blue">
$y= rsen \alpha$
</font></p>
<p align ="left"><font size ="5" color="red">
$x'= rcos (\alpha+\beta) = rcos \alpha cos \beta - rsen \alpha sen \beta $
</font></p>
<p align ="left"><font size ="5" color="red">
$y'= rsen (\alpha+\beta) = rcos \alpha sen \beta - rsen \alpha cos \beta $
</font></p>
<p align ="left"><font size ="6" color="#01DF3A">
$\boxed {x'= xcos \beta - ysen \beta}$
</font></p>
<p align ="left"><font size ="6" color="#01DF3A">
$\boxed {y'= xsen \beta + ycos \beta}$
</font></p>


## Two-dimensional transformations
<p align ="left"><font color="red">Rotation</font></p>
<img wigth ="800" height="250" src="lectures/2/fig/image8.JPG">
<p align ="left">We have </p>
$x' = x + h *y, y'=y$
<p align ="left">,where h is the sheared parameter, to obtain:</p>
<font size ="5" color="yellow">
$
D_x=\begin{bmatrix} 
1 & h \cr 
0 & 1 \end{bmatrix}
D_y=\begin{bmatrix} 
1 & 0 \cr 
h & 1 \end{bmatrix}
P'= {D_x \above 1.5pt D_y} * P
$
</font>


## Two-dimensional transformations

<table width="350" heigth="500" border="0" align ="right">
<tr>
<td>
<br/>
<br/>
<p><font size ="5" color="yellow">
$
T=\begin{bmatrix} 
d_x \cr 
d_y \end{bmatrix}
$
</font></p>
<br/>
<p><font size ="5" color="#00FFFF">
$
S=\begin{bmatrix} 
s_x & 0 \cr 
0 & s_y \end{bmatrix}
$
</font></p>
<br/>
<p><font size ="5">
$
R=\begin{bmatrix} 
cos\beta & -sen \beta  \cr 
sen \beta & cos \beta \end{bmatrix}
$
</font></p>
<br/>
<p><font size ="5" color="red">
$
D_x=\begin{bmatrix} 
1 & h \cr 
0 & 1 \end{bmatrix}
D_y=\begin{bmatrix} 
1 & 0 \cr 
h & 1 \end{bmatrix}
$
</font></p>
</td>
</tr>
</table> 

<p align ="left"><font color="blue">Trasformations Summary</font></p>
<p align ="left"><font color="yellow" size ="6">Traslation</font></p>
<p align ="left"><font size ="6" color="yellow">
$P' = P+T$
</font></p>
<p align ="left"><font color="#00FFFF"size ="6">Scaling</font></p>
<p align ="left"><font size ="6" color="#00FFFF">
$P' = S\ast P$
</font></p>
<p align ="left"><font size ="6">Rotation</font></p>
<p align ="left"><font size ="6">
$P' = R\ast P$
</font></p>
<p align ="left"><font color="red"size ="6">Sheared</font></p>
<p align ="left"><font size ="6" color="red">
$P'= {D_x \above 1.5pt D_y} * P$
</font></p>



## Types of Transformations 

<p align ="left"><font color="#00FFFF">1. Linear</font></p>
<p align ="left">
$
F(a+b)= F(a)+ F(b)
$
$
F(\lambda a) = \lambda F(a)\rightarrow F(0) = 0
$
, Thus is a nonlinear transformation
</p>
<p align ="center"><font color="yellow">Note:</font> Matrix multiplication is always linear</p>
<p align ="left"><font color="#00FFFF">2. Related</font></p>
<p align ="center">
Linear $+$ Traslation $\rightarrow p' = M\ast p + b $
</p>
<p align ="left"><font color="#00FFFF">3. Invertibles</font></p>
<p align ="center"> 
Lets take a look at <font color="red">$M^{-1}$ </font>, the inverse matrix of the general transformation matrix <font color="red">$M$</font>
</p>
$
P'= M\ast P,\space \space \space \space \space \space \space  M^{-1}P' = M^{-1}M P
$



## Homogeneous space
<table width="350" heigth="500" border="0" align ="left">
<tr>
<td>
<img src="lectures/2/fig/image9.JPG" width="400" heigth="400">
</td>
</tr>
</table>
<p><font color="#00FFFF">
Homogeneous coordinates</font></p>
$
(x,y,w)
$
<p>
2D Space $\rightarrow$ Homogeneous Space
</p>
<p>
$
(x,y) \rightarrow (x,y,1)
$
</p>
<p>
$
(\frac xw, \frac yw) \rightarrow (x,y,w)
$
</p>
<font color ="#868A08"><p>
3D Space $\rightarrow$ Homogeneous Space
</p>
<p>
$
(x,y,z) \rightarrow (x,y,z,1)
$
</p>
<p>
$
(\frac xw, \frac yw, \frac zw) \rightarrow (x,y,z,w)
$
</p>
</font>


## Summary 
<table width="350" heigth="500" border="0" align ="right">
<tr>
<td>
<br/>
<br/>
<p><font size ="4" color="yellow">
$
T=\begin{bmatrix} 
1 & 0 & d_x \cr
0 & 1 & d_y \cr 
0 & 0 & 1 \end{bmatrix}
$
</font></p>
<br/>
<p><font size ="4" color="#00FFFF">
$
S=\begin{bmatrix} 
s_x & 0 & 0 \cr
0 & s_y & 0 \cr 
0 & 0 & 1 \end{bmatrix}
$
</font></p>
<br/>
<p><font size ="4">
$
R=\begin{bmatrix} 
cos\beta & -sen \beta & 0  \cr 
sen \beta & cos \beta & 0  \cr
0 & 0 & 1\end{bmatrix}
$
</font></p>
<br/>
<p><font size ="4" color="red">
$
D_x=\begin{bmatrix} 
1 & h & 0\cr
0 & 1 & 0\cr 
0 & 0 & 1 \end{bmatrix}
D_y=\begin{bmatrix} 
1 & 0 & 0 \cr 
h & 1 & 0 \cr 
0 & 0 & 1\end{bmatrix}
$
</font></p>
</td>
</tr>
</table> 

<p align ="left"><font color="blue" size="4">
$
P'=\begin{bmatrix} 
x' \cr 
y' \cr 
1\end{bmatrix}
$
$
P=\begin{bmatrix} 
x \cr 
y \cr 
1\end{bmatrix}
$
</font></p>
<p align ="left"><font color="yellow" size ="5">Traslation</font></p>
<p align ="left"><font size ="5" color="yellow">
$P' = T(d_x,d_y)\ast P $
</font></p>
<p align ="left"><font color="#00FFFF"size ="5">Scaling</font></p>
<p align ="left"><font size ="5" color="#00FFFF">
$P' = T(s_x,s_y)\ast P$
</font></p>
<p align ="left"><font size ="5">Rotation</font></p>
<p align ="left"><font size ="5">
$P' = R(\beta)\ast P$
</font></p>
<p align ="left"><font color="red"size ="5">Sheared</font></p>
<p align ="left"><font size ="5" color="red">
$P'= {D_x \above 1.5pt D_y} * P$
</font></p>



##Homogeneous coordinates
<p align ="left"><font color="blue"> Observation about the inverse matrix of the transformation matrix</p></font>
<table width="650" heigth="500" border="0" align ="right">
<tr>
<td>
<p align ="left"><font size="4"> 
Lets take a look at <font color="red">$M^{-1}$ </font>, the inverse matrix of the general transformation matrix <font color="red">$M$</font></font>
</p>
</td>
</tr>
<tr>
<td>
<font size="4"> 
$
P'= M\ast P,\space \space \space \space \space \space \space  M^{-1}P' = M^{-1}M P
$
</font>
<p><font size="4">
$
M^{-1}P' = I \space \space \space P=P
$
</font></p>

<p><font size ="4" color="yellow">
$
T=\begin{bmatrix} 
1 & 0 & d_x \cr
0 & 1 & d_y \cr 
0 & 0 & 1 \end{bmatrix}
$

$
T^{-1}=\begin{bmatrix} 
1 & 0 & -d_x \cr
0 & 1 & -d_y \cr 
0 & 0 & 1 \end{bmatrix}
$
</font></p>
<br/>
<p><font size ="4" color="#00FFFF">
$
S=\begin{bmatrix} 
s_x & 0 & 0 \cr
0 & s_y & 0 \cr 
0 & 0 & 1 \end{bmatrix}
$
$
S^{-1}=\begin{bmatrix} 
\frac 1s_x & 0 & 0 \cr
0 & \frac 1s_y & 0 \cr 
0 & 0 & 1 \end{bmatrix}
$
</font></p>

</tr>
</td>
</table> 
<table width="310" heigth="500" border="0" align ="left">
<tr>
<td>
<br/> 
<p align ="left"><font color="blue" size="5">
$
P'=\begin{bmatrix}
x' \cr 
y' \cr 
1\end{bmatrix}
$
$
P=\begin{bmatrix} 
x \cr 
y \cr 
1\end{bmatrix}
$
</font></p>
<p align ="left"><font color="yellow" size ="5">Traslation</font></p>
<p align ="left"><font size ="5" color="yellow">
$P' = T(d_x,d_y)\ast P $
</font></p>
<p align ="left"><font color="#00FFFF" size ="5">Scaling</font></p>
<p align ="left"><font size ="5" color="#00FFFF">
$P' = T(s_x,s_y)\ast P $
</font></p>
</table> 


##Homogeneous coordinates
<p align ="left"><font color="blue"> Observation about the inverse matrix of the transformation matrix</p></font>

