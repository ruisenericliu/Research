**Announcing Mujoco-Warp and Newton: How Google DeepMind and NVIDIA are Supercharging Robotics Development [S72709]**
 \> From \<[https://register.nvidia.com/flow/nvidia/gtcs25/vap/page/vsessioncatalog/session/1727738299460001toka](https://register.nvidia.com/flow/nvidia/gtcs25/vap/page/vsessioncatalog/session/1727738299460001toka)\>   
Erik Frey, Google Deepmind
 
Newton - Open source Ecosystem for Physical Simulation  
MuJoCo Warp --\> MuJoCO XLA (MJX) ---\> JAX  
15 min for a humanoid locomotion policy
 ![Exported image](Exported%20image%2020260222122458-0.png)  

Broad phase geometry collision to accelerate sim6  
JAX declares tensor sizes ahead in advance - most matrices are sparse
 ![Exported image](Exported%20image%2020260222122501-1.png)  
![Exported image](Exported%20image%2020260222122507-2.png)  
![Exported image](Exported%20image%2020260222122511-3.png)