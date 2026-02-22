[![Image preview](Exported%20image%2020260222122624-0.jpeg)](https://www.linkedin.com/feed/update/urn:li:activity:7282783528847613952?updateEntityUrn=urn%3Ali%3Afs_updateV2%3A%28urn%3Ali%3Aactivity%3A7282783528847613952%2CFEED_DETAIL%2CEMPTY%2CDEFAULT%2Cfalse%29)

Robotics has a data scarcity problem - you simply can't scrape robot control data from webpages. Introducing GR00T-Mimic and GR00T-Gen: using both Graphics 1.0 & Graphics 2.0 to multiply your robot datasets by 1,000,000x.
 
We trade compute for synthetic data, so we are not capped by the fundamental physical limit of 24 hrs/robot/day.
 
Robotics is right in the thick of Moravec's paradox: things that are easy for humans turn out to be incredibly hard for machines. We are crushing the Moravec's paradox, one token at a time.
 
\> Graphics 1.0: Isaac simulators with manually written, GPU-accelerated physics and rendering equations.  
\> Graphics 2.0: big neural nets (Cosmos) that repaint the pixels from sim textures to real, given an open-ended prompt.
 
Robot data multiplier workflow:
 
1. GR00T-Teleop: use XR device like Apple Vision Pro to map human finger poses to humanoid hands.
 
2. GR00T-Mimic: given a human-collected task demonstration, we augment the actions in Isaac and filter out ones that fail the task.
 
3. GR00T-Gen: apply Graphics 1.0 and then Graphics 2.0 to produce tons of visual variations.
 
The above is an exponential pipeline, adding orders of magnitude at each step.
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>         
Exciting updates on Project GR00T! We discover a systematic way to scale up robot data, tackling the most painful pain point in robotics. The idea is simple: human collects demonstration on a real robot, and we multiply that data 1000x or more in simulation. Let’s break it down:
 
1. We use Apple Vision Pro (yes!!) to give the human operator first person control of the humanoid. Vision Pro parses human hand pose and retargets the motion to the robot hand, all in real time. From the human’s point of view, they are immersed in another body like the Avatar. Teleoperation is slow and time-consuming, but we can afford to collect a small amount of data.  
2. We use RoboCasa, a generative simulation framework, to multiply the demonstration data by varying the visual appearance and layout of the environment. In Jensen’s keynote video below, the humanoid is now placing the cup in hundreds of kitchens with a huge diversity of textures, furniture, and object placement. We only have 1 physical kitchen at the GEAR Lab in NVIDIA HQ, but we can conjure up infinite ones in simulation.  
3. Finally, we apply MimicGen, a technique to multiply the above data even more by varying the *motion* of the robot. MimicGen generates vast number of new action trajectories based on the original human data, and filters out failed ones (e.g. those that drop the cup) to form a much larger dataset.
 
To sum up, given 1 human trajectory with Vision Pro  
-\> RoboCasa produces N (varying visuals)  
-\> MimicGen further augments to NxM (varying motions).
 
This is the way to trade compute for expensive human data by GPU-accelerated simulation. A while ago, I mentioned that teleoperation is fundamentally not scalable, because we are always limited by 24 hrs/robot/day in the world of atoms. Our new GR00T synthetic data pipeline breaks this barrier in the world of bits.
 
Scaling has been so much fun for LLMs, and it's finally our turn to have fun in robotics! We are creating tools to enable everyone in the ecosystem to scale up with us:
 
- RoboCasa: our generative simulation framework (Yuke Zhu). It's fully open-source! Here you go: [http://robocasa.ai](http://robocasa.ai)  
- MimicGen: our generative action framework (Ajay Mandlekar). The code is open-source for robot arms, but we will have another version for humanoid and 5-finger hands: [https://lnkd.in/gsRArQXy](https://lnkd.in/gsRArQXy)  
- We are building a state-of-the-art Apple Vision Pro -\> humanoid robot "Avatar" stack. Xiaolong Wang group’s open-source libraries laid the foundation: [https://lnkd.in/gUYye7yt](https://lnkd.in/gUYye7yt)  
- Watch Jensen's keynote yesterday. He cannot hide his excitement about Project GR00T and robot foundation models! [https://lnkd.in/g3hZteCG](https://lnkd.in/g3hZteCG)
 
Finally, GEAR lab is hiring! We want the best roboticists in the world to join us on this moon-landing mission to solve physical AGI: [https://lnkd.in/gTancpNK](https://lnkd.in/gTancpNK)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>