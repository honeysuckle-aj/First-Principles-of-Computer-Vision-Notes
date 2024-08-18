# Uncalibrated Stereo
The #extrinsic-matrix is **unknown**
![[Pasted image 20240811162547.png]]
## get intrinsics
- calibrate the camera
- mera tag information embedded to the image itself
## get extrinsics
1. Assume #camera-matrix $K$ is known for each camera.
2. Find a few reliable corresponding points![[Pasted image 20240811163258.png]]
3. Find *ralative* camera position $t$ and Orientation $R$.
4. Find Dense Correspondences.