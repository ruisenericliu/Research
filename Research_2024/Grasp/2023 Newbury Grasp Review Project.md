[https://rhys-newbury.github.io/projects/6dof/](https://rhys-newbury.github.io/projects/6dof/)
 
“There is currently no consensus on when to use direct regression based methods versus sampling-based methods, as both approaches focus on similar tasks with similar success rates”(Newbury et al., 2023, p. 13)
 
“RL approaches for grasping typically focus not only on grasp generation but also on the trajectory used by the system. However, RL approaches typically generate only one grasp per scene, making it difficult to incorporate additional constraints during execution.”(Newbury et al., 2023, p. 13)
 ![Grasping Stages](Exported%20image%2020260222202543-0.jpeg)  

Focus of this review is grasp synthesis
 
Duan et al. indicates pre 2020 is about sampling based methods; Newbury focuses on end-to-end methods (Direct Regression)  
4 - DOF - x,y,z, yaw  
6 - DOF - position and orientation  
Acceptable surface points for an object's pose
 
**An approach vector** defines the line along which the gripper or robotic hand approach the target object.
 
**The grasp center point** is the point in space somewhere along the approach vector where the coordinate frame fixed to  
the gripper must be positioned before starting to close the fingers.
 
**The hand orientation** defines how the robot hand is oriented around the approach vector when placed on the grasp center point.
 
“Antipodal points are pairs of points on the object surface whose normal vectors are collinear and pointing in the opposite direction [21].”(Newbury et al., 2023, p. 3)
       
Sampling approaches estimate the quality of each sampled grasp; whereas direct regression considers the data globally
  2. Sampling considers an optimization search for the grasp based on a (learned) value for grasp quality.
    1. Sample a grasp as init seed, refine via derivatives of quality estimation network
3. Direct regression attempts a single network for 6-DOF grasping
    1. Some approaches seek to target grasp depth after grasp position
    2. Could also handle in this in multiple stages
        1. e.g. predict grasp quality
        2. Estimate a grasp proposal
        3. Refine regressed grasps
4. Learning approaches
    1. Q Learning, DQN, PPO, TRPO, DDPG
    2. On policy more common than off-policy
        1. On policy looks like orientation, approach, and close
        2. Reward is pick + distance (sink)
5. Support methods
    1. Predict shape, predict grasp
    2. Predict affordance, assign 6-DOF grasp
 
Data:  
Point Cloud; Voxel Grid; RGB-D Image; and Depth Image  
Cornell, YCB, Armbench, GraspNet 1B
 
YCB Dataset?