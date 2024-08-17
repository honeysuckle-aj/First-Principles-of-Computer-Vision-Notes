find relative position
# Epipoles
![[Pasted image 20240817145717.png]]
we are going to find $R$ and $t$.
**$e_l, e_r$ are the epipoles
$e_l, e_r$ are unique for a given stereo pair.**
# Epipolar plane
![[Pasted image 20240817145849.png]]
**Every scene point lies on a unique epipolar plane**
# Epipolar conatraint
## What is an essential matrix
![[Pasted image 20240817150005.png]]
![[Pasted image 20240817150032.png]] #epipolar-constraint
![[Pasted image 20240817150211.png]]
![[Pasted image 20240817150234.png]]
![[Pasted image 20240817150408.png]] #essential-matrix #formula 
![[Pasted image 20240817150441.png]]
#skew-symmetric [[singular value decomposition]]
If $E$ is known, we can calculate $t$ and $R$.
## Find the essential matrix
![[Pasted image 20240817150817.png]]
Unfortunately, *we don't have $x_l$ and $x_r$.*
*we only have $u_l,u_r$ which is the projection of $x$ on the image*
### incorporate the Image Coondinates
![[Pasted image 20240817151026.png]]
#camera-matrix 
we have left and right camera equations
![[Pasted image 20240817151443.png]]
![[Pasted image 20240817151235.png]]
Axis $z$ represents the depth of the point.
So $z_l$ and $z_r$ can't be $0$, or they will lie on the center of projection instead of being **infront of the camera.**
![[Pasted image 20240817151821.png]]
![[Pasted image 20240817151829.png]]
![[Pasted image 20240817151914.png]] #fundamental-matrix
$$F = K_{l}^{-1^T}E K_r^{-1}$$
$$E=K^T_lFK_r$$

