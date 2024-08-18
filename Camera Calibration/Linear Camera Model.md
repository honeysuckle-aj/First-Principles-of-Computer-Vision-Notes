# [[Forward Imaging Model]]

3D to 2D
![[Pasted image 20240808235709.png]]

the **Z axis** of the **camera coordinate frame** is aligned with the **optical axis** of the camera

- $f$: focal length
- $x_w$: x in the World coodinates
- $x_c$: x in the Camera coodinates
- $x_i$: x in the Image coodinates

# [[Perspective Projection]]

Camera to Image

![[Pasted image 20240808235743.png]]

## Image plane to Image sensor plane

Image plane(milimeter)

Image sensor(pixel)
![[Pasted image 20240808235806.png]]

- Pixels may be recrangular
- $（o_x,o_y)$: Principle Point. We always treat the top-left corner as the beginning of the Image Sensor which is easier to indexing. Principle Point is where the **optical axis** pierces the sensor.
- **$m_x,m_y$ : Pixel Density(pixel/mm) of axis x and y
- **$u=m_x x_i=m_x f\frac{x_c}{z_c}+o_x$**
- **$v=m_yy_i=m_yf\frac{y_c}{z_c}+o_y$ -> non linear

Let $(f_x,f_y)=(fm_x,fm_y)$ be the focal lengthof the pixels of the x and y directions.

Typically one camera only has one exffective focal length. But considering ==there might be different pixel densities in x and y directions,== we use $（f_x, f_y)$ to represent these two focal length of pixels.

$(f_x,f_y,o_x,o_y)$ are the intrinsic parameters of a camera. They represents the camera's internal geometry.

## [[Homogeneos Coordinates]]

The homogeneos representation of a *2D* point $\textbf{u}=(u,v)$ is a *3D* point $\tilde{\textbf{u}}=(\tilde u,\tilde v, \tilde w)$ . The third coordinate $\tilde{w}\not= 0$  is fictitious such that 
![[Pasted image 20240809105303.png]]
*3D -> 4D*:
![[Pasted image 20240809105517.png]]
Then the [[Perspective Projection]] equations can be reformatted:
![[Pasted image 20240809105650.png]] #formula #intrinsic-matrix
![[Pasted image 20240809110137.png]] #formula #calibration-matrix #camera-matrix
![[Pasted image 20240809110205.png]] #formula #intrinsic-matrix 
![[Pasted image 20240810105840.png]]
# External Paremeters
World coordinates to Camera coordinates
![[Pasted image 20240809110432.png]]  #formula #orientation
## [[Orthonormal Matrix]]
![[Pasted image 20240809110606.png]] 
A [[rotation matrix]] is an [[Orthonormal Matrix]]
## World-to-Camera Transformation
Given the [[extrinsic parameters]] $(R,c_w)$ of the camera, the camera-centric location of the point P in the world coordinat frame is:
![[Pasted image 20240809111044.png]]
![[Pasted image 20240809111114.png]]
Rewriting using homogeneous coordinates:
![[Pasted image 20240809111222.png]]
![[Pasted image 20240809111235.png]] #formula #extrinsic-matrix

![[Pasted image 20240810105743.png]]
# Projection Matrix P
Combining #calibration-matrix rinsic and #extrinsic-matrix .
![[Pasted image 20240810105928.png]] #projection-matrix #formula 
