We’ve entered a new phase in robotics—moving beyond rigid-link systems with embedded sensors, toward soft, biologically inspired robots that can adapt to the world around them. But these new morphologies bring a big challenge: control.
 
In our latest paper, published in Nature Magazine, my collaborators and I introduce Neural Jacobian Fields (NJF) — a vision-based control method that allows robots to learn how their bodies move, using only video. No sensors. No digital twin. Just observation and self-supervised learning.
 
With Neural Jacobian Fields, our soft robotic hands were able to learn to grasp objects entirely through visual observation — no sensors, no prior model, and no manual programming. By watching its own movements through a camera and performing random actions, the robot built an internal model of how its body responds to motor commands. NJF mapped these visual inputs to a dense visuomotor Jacobian field, enabling the robot to control its motion in real time based solely on what it sees.
 
This reframing of control has major implications. Traditional methods require detailed models or embedded sensors. NJF lifts those constraints, enabling control of unconventional, deformable, or sensor-less robots in real time, using only a single monocular camera.
 
We tested NJF across soft grippers, rigid hands, 3D-printed arms, and even a rotating platform — all learned their internal models autonomously, from vision alone. That means more freedom for robot designers and new opportunities for automation in agriculture, construction, and home environments.  
Huge thanks to my collaborators S. Lester Li, Vincent Sitzmann, Annan Zhang, Boyuan Chen, Hanna Matusik, and Chao Liu. It was a privilege to combine our work in soft robotics, computer vision, and learning to explore this new frontier.
 
You can read our paper in Nature and learn more about our work in  
MIT Computer Science and Artificial Intelligence Laboratory (CSAIL)'s Robot Report  
[https://lnkd.in/eBVJF-V5](https://lnkd.in/eBVJF-V5)  
[https://lnkd.in/eWRcWUii](https://lnkd.in/eWRcWUii)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>