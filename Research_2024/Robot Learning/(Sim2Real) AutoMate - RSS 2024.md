AutoMate: [https://developer.nvidia.com/blog/training-sim-to-real-transferable-robotic-assembly-skills-over-diverse-geometries/?linkId=100000272950370](https://developer.nvidia.com/blog/training-sim-to-real-transferable-robotic-assembly-skills-over-diverse-geometries/?linkId=100000272950370)  
The real-world setup includes a Franka Panda robot arm, a wrist-mounted Intel RealSense D435 camera, a 3D-printed plug and socket, and a Schunk EGK40 gripper used to hold the socket. In the perception-initialized workflow: 

- The plug is placed haphazardly on a foam block and the socket is placed haphazardly within the Schunk gripper.
- An RGB-D image is captured through the wrist-mounted camera, followed by 6D pose estimation ([FoundationPose](https://nvlabs.github.io/FoundationPose/)) of the parts.
- The robot grasps the plug, transports it to the socket, and deploys a simulation-trained assembly skill.

![A sequence of images demonstrating the robotic ass...](Exported%20image%2020260222203017-0.png)

_Figure 10. Real-world setup and perception-initialized workflow_  
The specialists and the generalists are evaluated in the perception-initialized workflow. For specialists, the mean success rate is 90.0%. For generalists, the success rate is 86.0%. These results indicate that 6-DOF pose estimation, grasp optimization, and the proposed methods for learning specialist and generalist policies can be effectively combined to achieve reliable assembly under realistic conditions using research-grade hardware
 \> From \<[https://developer.nvidia.com/blog/training-sim-to-real-transferable-robotic-assembly-skills-over-diverse-geometries/?linkId=100000272950370](https://developer.nvidia.com/blog/training-sim-to-real-transferable-robotic-assembly-skills-over-diverse-geometries/?linkId=100000272950370)\>     

To get up to speed on the preceding NVIDIA work, read the papers for [Factory](https://arxiv.org/pdf/2205.03532) and [IndustReal](https://arxiv.org/pdf/2305.17110). Visit the [AutoMate](https://bingjietang718.github.io/automate/) project page to read the paper and view ‌summary videos. Stay tuned for the upcoming integration of AutoMate into the newly released [NVIDIA Isaac Lab](https://github.com/isaac-sim/IsaacLab).
 \> From \<[https://developer.nvidia.com/blog/training-sim-to-real-transferable-robotic-assembly-skills-over-diverse-geometries/?linkId=100000272950370](https://developer.nvidia.com/blog/training-sim-to-real-transferable-robotic-assembly-skills-over-diverse-geometries/?linkId=100000272950370)\>     

Join authors Bingjie Tang, Iretiayo Akinola, Jie Xu, Bowen Wen, Ankur Handa, Karl Van Wyk,  Dieter Fox, Gaurav S. Sukhatme, Fabio Ramos, and Yashraj Narang at the [Robotics: Science and Systems (RSS)](https://roboticsconference.org) conference in July 2024 for their presentation of the paper, AutoMate: Specialist and Generalist Assembly Policies over Diverse Geometries. 
 \> From \<[https://developer.nvidia.com/blog/training-sim-to-real-transferable-robotic-assembly-skills-over-diverse-geometries/?linkId=100000272950370](https://developer.nvidia.com/blog/training-sim-to-real-transferable-robotic-assembly-skills-over-diverse-geometries/?linkId=100000272950370)\>