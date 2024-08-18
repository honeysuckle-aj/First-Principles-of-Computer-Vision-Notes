Given a calibrated camera
![[Pasted image 20240811154257.png]]
# Triangulation using Two Cameras
**Attention: here the two camera plains are horizontal**
![[Pasted image 20240811154530.png]] #formula #stereo-system
- for a point $(u_l,v_l)$ in the left image, we can find a *corresponding point* $(u_r,v_r)$ in the right image.
- $b$ is the [[horizontal baseline]] representing the distance between the two cameras' central points.
- Solving for $(x,y,z)$:![[Pasted image 20240811154930.png]] ![[Pasted image 20240811154941.png]] 
- $u_l - u_r$ is called [[disparity]]
- depth $z$ is inversely proportional to [[disparity]]
- [[disparity]] is proportional to [[horizontal baseline]]
# A Simple Stereo Camera
![[Pasted image 20240811155306.png]]
# Stereo Matching: Finding Disparities
determine disparity using template window
![[Pasted image 20240811155600.png]]
# Similarity Metrics for Template Matching
![[Pasted image 20240811155702.png]]
# Issues with Stereo Matching
- Surface must have (non-repetitive) texture.![[Pasted image 20240811155829.png]] the window will be identical to others
- Foreshortening effect maked matching challenging![[Pasted image 20240811155944.png]] the same size of window might catch different pixels. The left camera is *further* from the plain compared to the right camera which cause the window areas from the left image cover more *real world* points.
# How Large should the Window be?
## Big or Small
- small windows: *good localization* but **high sensitivity noise**
- big windows: *more robust matching* but **more blurred especially at boundaries**
- ![[Pasted image 20240811160856.png]]
## Adaptive Window Sizes
![[Pasted image 20240811160930.png]]
![[Pasted image 20240811161023.png]]