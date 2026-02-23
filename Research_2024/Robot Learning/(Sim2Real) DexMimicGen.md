I don’t know if we live in a Matrix, but I know for sure that robots will spend most of their lives in simulation. Let machines train machines! I’m excited to introduce DexMimicGen, a massive-scale synthetic data generator that enables a humanoid robot to learn complex skills from only a handful of human demonstrations. Yes, as few as 5!
 
DexMimicGen addresses the biggest pain point in robotics: where do we get data? Unlike with LLMs, where vast amounts of texts are readily available, you cannot simply download motor control signals from the internet. So researchers teleoperate the robots to collect motion data via XR headsets. They have to repeat the same skill over and over and over again, because neural nets are data hungry. This is a very slow and uncomfortable process.
 
At NVIDIA, we believe the majority of high-quality tokens for robot foundation models will come from simulation.
 
What DexMimicGen does is to trade GPU compute time for human time. It takes one motion trajectory from human, and multiplies into 1000s of new trajectories. A robot brain trained on this augmented dataset will generalize far better in the real world.
 
Think of DexMimicGen as a learning signal amplifier. It maps a small dataset to a large (de facto infinite) dataset, using physics simulation in the loop. In this way, we free humans from babysitting the bots all day.
 
The future of robot data is generative.  
The future of the entire robot learning pipeline will also be generative.
 
DexMimicGen is a big team work from GEAR Lab and collaborators:  
Team: Zhenyu Jiang, Yuqi Xie, Kevin Lin, Zhenjia Xu, Weikang Wan  
Project leads: Ajay Mandlekar, Jim Fan, Yuke Zhu
 
Website: [https://lnkd.in/gEGeQ2u4](https://lnkd.in/gEGeQ2u4)  
Arxiv: [https://lnkd.in/gU9QmWsA](https://lnkd.in/gU9QmWsA)
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>