Are autonomous vehicles with end-to-end planners safe?  
(end-to-end planners are neural networks that take as input images and output a driving trajectory)
 
This is an important question as Tesla's FSD v12 is apparently end-to-end. Furthermore, papers like UniAD and VAD are slowly taking over in a diverse set of benchmarks from tracking and mapping to prediction and planning.
 
So how do we test such methods?   
- Test-track? Not the right environment!   
- Classical simulation? Not photorealistic!  
- Learned simulation? Yes, using Zenseact's NeuRAD (NeRF-based)
 
We create three "NeuroNCAP" scenarios from urban scenes in nuScenes. We modify the placement of the agents and render three crash test scenarios: frontal collisions, collisions with static vehicles and side collisions. Then we run end-to-end planners in closed-loop to evaluate their performance. If they crash into the vehicle, we measure the impact velocity, similar to traditional NCAP tests.
 
How do leading end-to-end methods perform? Shockingly, they fail in more than half of all scenarios. 😱😱😱  
Why? Because regular autonomous vehicle datasets do not include such (near-)crash scenarios.
 
What does this mean for Tesla? Hard to say. Unfortunately, they do probably have data of (near-)accident scenarios, but even then these will be a needle in a haystack and it will be hard to train a planner to deal with such scenarios. Training in a learned simulation environment could help here.
 
We make our benchmark available to the public, in the hopes that the community will be able to overcome these limitations.
 
This great work was done by the talented PhD students at Zenseact, [William Ljungbergh](https://www.linkedin.com/in/ACoAACAhPp0Bl_i5sHKNNtgOjfZ3KO2cI9WiW_k) [Adam Tonderski](https://www.linkedin.com/in/ACoAABqhjjkB86WVWlPHz9Z2lL8oTJzZhG2xT3U) [Joakim Johnander](https://www.linkedin.com/in/ACoAACIzxycBUIBCYXx6nBlkI2K6jfebMhQ4190), as well as myself, [Kalle Åström](https://www.linkedin.com/in/ACoAAADbHJUBXPjKML8Gby6oIQ3RoriFINMudyk), [Michael Felsberg](https://www.linkedin.com/in/ACoAAACBvbABICQTftSOVSG4z_NPyWE_qMTfknk) and Christoffer Peterssen.
 
Project Page: [https://lnkd.in/dSv7HFYQ](https://lnkd.in/dSv7HFYQ)  
Code: [https://lnkd.in/d73HcWrb](https://lnkd.in/d73HcWrb)  
Paper: [https://lnkd.in/dTQfg__9](https://lnkd.in/dTQfg__9)
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>