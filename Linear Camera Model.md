# [[Forward Imaging Model]]

3D to 2D
![[Pasted image 20240808235709.png]]

the **Z axis** of the **camera coordinate frame** is aligned with the **optical axis** of the camera

- $f$: focal length
- $x_w$: x in the World coodinates
- $x_c$: x in the Camera coodinates
- $x_i$: x in the Image coodinates

## [[Perspective Projection]]

Camera to Image

![[Pasted image 20240808235743.png]]

### Image plane to Image sensor plane

Image plane(milimeter)

Image sensor(pixel)
![[Pasted image 20240808235806.png]]

- Pixels may be recrangular
- $（o_x,o_y)$: Principle Point. We always treat the top-left corner as the beginning of the Image Sensor which is easier to indexing. Principle Point is where the **optical axis** pierces the sensor.
- **$m_x,m_y$ : Pixel Density(pixel/mm) of axis x and y
- **$u=m_x x_i=m_x f\frac{x_c}{z_c}+o_x$**
- **$v=m_yy_i=m_yf\frac{y_c}{z_c}+o_y$**

Let $(f_x,f_y)=(fm_x,fm_y)$ be the focal lengthof the pixels of the x and y directions.

Typically one camera only has one exffective focal length. But considering ==there might be different pixel densities in x and y directions,== we use $（f_x, f_y)$ to represent these two focal length of pixels.