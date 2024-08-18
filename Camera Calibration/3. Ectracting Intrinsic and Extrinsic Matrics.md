#projection-matrix can be decomposed into the #intrinsic-matrix and the #extrinsic-matrix .
![[Pasted image 20240810152206.png]]
![[Pasted image 20240810152233.png]]
$K$ is an *Upper Right Triangular matrix* and $R$ is an [[Orthonormal Matrix]]. 
It is possible to uniquely *decouple* $K$ and $R$ using [[QR factorization]]
![[Pasted image 20240810152723.png]]
![[Pasted image 20240810152743.png]]
 
# Other Intrinsic Parameters
 Pinholes do not exhibit image distortions. *But lenses do.*
 ![[Pasted image 20240810154640.png]] #radial-distortion #tengential-distortion
 These two distortion make camera calibration non-linear. There are two methods:
 1. add more parameters to projection matrix -> makes matrx ==non-linear==
 2. calibrate these kinds of distortions in advance, then we have a linearised camera model.