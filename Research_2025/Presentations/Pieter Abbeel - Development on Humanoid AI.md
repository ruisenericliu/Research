[https://www.nvidia.com/en-us/on-demand/session/gtc25-s73182/](https://www.nvidia.com/en-us/on-demand/session/gtc25-s73182/)
 
Revolution in hardware for humanoids and haptics
 
Data for robotics --- biggest opportunity

1. Tele-operation (time consuming)
2. Human Hand Videos (ego4d)
3. Simulation (at scale)
4. Real Robot RL
5. Internet Videos/ text
 
Predicts continued drop in hardware price
 
In some sense, we have a mess - it's exciting from a research standpoint ( need an interactive context)
 
No convergence yet on high-signal data  
No convergence to combine data sources
 
However, exciting time for this field ( and can jump in from home (start from sim - HumanoidBench)
 
Some highlights:

1. Mobile Aloha -- capture tokens for teleop
2. Pi0 builds on top of mobile aloha - shows better results - shows error correction behavior of robots
3. Apple vision pro - telop via hand motion (MIT UCSD)
4. UCSD (Wang Xiaolong - robot dog with arm, 4x speed)
5. Affordance from human videos - Deepak Pathak (CVPR 2023) - instill a prior of interest
6. Dataset of Walking Trajectories (Berkeley Mocap capture (Radosavovic, Malik, 2024) -- some data with action ignored + Fine Tune RL - 4 miles of real hikes, no camera feed
7. Li, Abbeel - lower body running - 27S to run 100M
8. Unitree was probably trained on MoCap + SimRL
9. VideoMimic - how to get more video data into the simulator
10. BodyTransformer - locality of body matters
    1. A spatially modular architecture - in place of a monolthy - high-diemnsional setting - localized credit assignment!
    2. Better inductive bias - thus needs fewer demonstrations!
11. HumanoidBench - keep weaker robots; maximize usage at physical boundaries - 3/27 tasks solved thus far
12. MuJoCo Playground
    1. ![Exported image](Exported%20image%2020260222122421-0.png)
    2. Erik Frey solving this   

![Exported image](Exported%20image%2020260222122422-1.png)      ![Exported image](Exported%20image%2020260222122423-2.png)   ![Exported image](Exported%20image%2020260222122428-3.png)