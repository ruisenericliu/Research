Can robots learn without training❓  
[𝗜𝘁'𝘀 𝗼𝗽𝗲𝗻 𝘀𝗼𝘂𝗿𝗰𝗲𝗱 ⬇ ]
 
Teaching robots to do complex tasks WITHOUT spending hours training them.
 
Sounds cool, right?
 
That's exactly what DIAL-MPC does!
 
The first training-free method for whole-body torque control using full-order dynamics:
 
✅ Instantly checks if a robot's moves are right or wrong  
✅ Adapts quickly to new tasks without needing extra training  
✅ Could work hand-in-hand with other robot learning methods
 
Robots are getting smarter AND faster without the need for long training sessions.
 
Website: [https://lnkd.in/de7Zuyd5](https://lnkd.in/de7Zuyd5)  
Paper: [https://lnkd.in/dTkBWHb2](https://lnkd.in/dTkBWHb2)  
Code: [https://lnkd.in/dbQtiHXd](https://lnkd.in/dbQtiHXd)
 
Saw this first at [Haoru Xue](https://www.linkedin.com/in/haoru-xue/)!
   

Sim2Real RL works by scaling up offline computation in training time. How about scaling up online computation using sampling-based MPC in test time?
 
DIAL-MPC is a training-free sampling-based MPC method that adopts the key idea from diffusion to gradually refine solutions via annealing. For the first time, as a training-free method, DIAL-MPC enables 50Hz, torque-level, precise locomotion control using full-order dynamics (no reduced-order modeling, no hierarchy, no linearization, directly output torques using full dynamics).
 
In various tasks requiring precision or zero-shot test-time adaptability (e.g., robots with payload), it even outperforms RL methods that require training.
 
The theoretical backbone of DIAL-MPC is the intriguing connection between sampling-based optimization/control and diffusion (more details in our NeurIPS'24 paper MBD [https://lnkd.in/emWcECQE](https://lnkd.in/emWcECQE)).
 
DIAL-MPC is fully open-sourced! [https://lnkd.in/eHT_VEnZ](https://lnkd.in/eHT_VEnZ) Implementing it is actually simpler than many Sim2Real RL pipelines: No waiting time, real-time large-scale sampling in simulation + few reward terms = real-world locomotion!