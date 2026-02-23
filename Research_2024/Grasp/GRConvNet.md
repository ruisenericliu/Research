Antipodal Robotic Grasping
   

Not a sampling based approach - generate 3 images instead for pixel estimates of:
 
1. Quality, Angle, and Width  
Shape the grasp pose as 4-DOF  
Position + rotation around Z axis, Width + Grasp Quality score  
Rotation is in camera reference frame hmmmmm
 
Assume for vertical grasping like a heron
 
antipodal grasp is uniform around ± π/2, we extract the angle in the form of two elements cos 2Θ and sin 2Θ
 
Very small network, suitable for closed loop up to 50 Hz
 
Loss function on Grasp generation error - Huber loss  
(Train on Cornell and Jacquard)
 ![Exported image](Exported%20image%2020260222202545-0.png)  

![Exported image](Exported%20image%2020260222202546-1.png)