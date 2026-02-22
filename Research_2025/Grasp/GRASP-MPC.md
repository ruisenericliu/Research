[https://grasp-mpc.github.io/](https://grasp-mpc.github.io/)
 
How can robots safely and robustly grasp novel objects in cluttered environments?  
We introduce Grasp-MPC, a hybrid of model-based control and data-driven approaches for generalisable and safe 6DoF closed-loop grasping.
 
🔹 Background  
Open-loop grasping methods (e.g., M2T2 combined with motion planning) can generalise to novel objects, but they are brittle to prediction noise.  
Closed-loop RL/IL methods leverage feedback for control, but their performance is typically limited to simplified, clean environments.
 
🔹 Our idea  
Grasp-MPC combines the best of both worlds:  
- Model-based MPC for safety and constraint handling  
- Data-driven value function (as a cost function) for generalisable grasping  
Together → generalisable and safe 6DoF grasping.
 
🔹 Method  
1. Generate large-scale synthetic grasp trajectories in simulation using motion planning  
2. Train a value function with TD learning (labelling success = 0 cost, failure = 1)  
3. Integrate the learned value into GPU-accelerated MPC (CuRobo)
 
🔹Deployment  
1. Use an off-the-shelf grasp pose predictor (e.g., M2T2) to generate pre-grasp poses  
2. Plan motion to one of these poses with CuRobo goal-set planning  
3. Execute Grasp-MPC for closed-loop grasping
 
🔹 Results  
Simulation: Grasp-MPC significantly outperforms both open-loop and closed-loop baselines, especially under noisy grasp poses or when using an off-the-shelf grasp predictor.
 
Real world: In experiments including (1) clean tabletop, (2) cluttered tabletop, and (3) cluttered shelf scenes, Grasp-MPC achieves substantially better performance than the open-loop approach, safely grasping novel objects.  
Since it is closed-loop, Grasp-MPC can even grasp moving objects.
 
For further details, please refer to the paper and website!  
📄 Paper: [https://lnkd.in/eWTxsNx9](https://lnkd.in/eWTxsNx9)  
🌐 Project page: [https://lnkd.in/eaJGqB9n](https://lnkd.in/eaJGqB9n)
 
This work began during my internship at [NVIDIA Robotics](https://www.linkedin.com/company/nvidiarobotics/) and was further developed at [Oxford Robotics Institute](https://www.linkedin.com/company/oxford-robotics-institute/).  
Huge thanks to my collaborators: [Adithya Murali](https://www.linkedin.com/in/adithyamurali/), Ajay Mandlekar, Clemens Eppner, [Ingmar Posner](https://www.linkedin.com/in/ingmar-posner-20b49a/), and [Balakumar Sundaralingam](https://www.linkedin.com/in/balakumar-s/).
 \> From \<[https://www.linkedin.com/preload/](https://www.linkedin.com/preload/)\>