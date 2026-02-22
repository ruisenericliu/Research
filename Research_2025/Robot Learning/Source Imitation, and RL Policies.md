**Summary Points:**  
**On Robot Learning:** [https://www.linkedin.com/pulse/robot-learning-julien-perez-0p5ce](https://www.linkedin.com/pulse/robot-learning-julien-perez-0p5ce)  
PPO and SAC are RL --- ACT, diffusion policy, VQ-BET are imitation learning  
TD-MPC is a model based planner with an RL trained policy. It's similar to PlaNet, Dreamer, MuZero in how it works. So of those the only one worth comparing, since the others aren't RL, is TD-MPC. That is designed to more sample efficient than SAC and should work well in high dimensional environments. (edited)  
And compared to dreamer TD-MPC and especially TD-MPC2 is meant to be better (according to TDMPC2) (edited)
 
Uncategorized:  
URMAv2: [https://arxiv.org/abs/2509.02815](https://arxiv.org/abs/2509.02815)  
Efficient RL needs no Online Data: [https://arxiv.org/abs/2412.07762](https://arxiv.org/abs/2412.07762)  
[https://generalist-distillation.github.io/](https://generalist-distillation.github.io/)  
Ex-body: [https://exbody2.github.io/resources/exbody2.pdf](https://exbody2.github.io/resources/exbody2.pdf)  
[https://zhouzypaul.github.io/wsrl/](https://zhouzypaul.github.io/wsrl/)  
[https://generalistai.com/blog.html](https://generalistai.com/blog.html)  
[https://github.com/google-deepmind/gemini-robotics-sdk](https://github.com/google-deepmind/gemini-robotics-sdk)  
[https://vision-in-action.github.io/](https://vision-in-action.github.io/)  
[https://bridgevla.github.io/home_page.html](https://bridgevla.github.io/home_page.html)  
[https://ember-lab-berkeley.github.io/LeVERB-Website/](https://ember-lab-berkeley.github.io/LeVERB-Website/)  
[https://diffusion-steering.github.io/](https://diffusion-steering.github.io/)  
[https://www.physicalintelligence.company/research/knowledge_insulation](https://www.physicalintelligence.company/research/knowledge_insulation)  
[https://ut-austin-rpl.github.io/SCIZOR/](https://ut-austin-rpl.github.io/SCIZOR/)  
DreamGen(https://arxiv.org/pdf/2505.12705) this paper is wild  
[https://pd-perry.github.io/expo-site/](https://pd-perry.github.io/expo-site/)
 
**Core Papers: RL + Imitation**  
**CoT-VLA:** [https://cot-vla.github.io](https://cot-vla.github.io)  
**Demo3:** **https://adrialopezescoriza.github.io/demo3**  
**OtterVLA:** [https://ottervla.github.io/](https://ottervla.github.io/)  
**CASPER:** [https://arxiv.org/abs/2506.14727](https://arxiv.org/abs/2506.14727)  
**VLA-RL:** [https://arxiv.org/pdf/2505.18719v1](https://arxiv.org/pdf/2505.18719v1) | [https://github.com/PRIME-RL/SimpleVLA-RL](https://github.com/PRIME-RL/SimpleVLA-RL)  
**Motion Tracks: sample efficiency from demonstrations** **https://arxiv.org/pdf/2501.06994**  
OpenTeach: [https://open-teach.github.io/](https://open-teach.github.io/)  
Policy Agnostic RL: [https://policyagnosticrl.github.io/](https://policyagnosticrl.github.io/)  
Summary of ACT|Diffusion: [https://bimanual-imitation.github.io/](https://bimanual-imitation.github.io/)  
Starting point: [https://supervised-robot-learning.github.io/](https://supervised-robot-learning.github.io/)  
Mobile Aloha: [https://aloha-2.github.io/](https://aloha-2.github.io/) | [https://aloha-unleashed.github.io/](https://aloha-unleashed.github.io/)  
UMI-Gripper: [https://umi-gripper.github.io/](https://umi-gripper.github.io/)  
OpenVLA: [https://openvla.github.io/](https://openvla.github.io/)  
Pi0: [https://www.physicalintelligence.company/blog/pi0](https://www.physicalintelligence.company/blog/pi0)  
[https://www.physicalintelligence.company/download/pi0.pdf](https://www.physicalintelligence.company/download/pi0.pdf)  
FAST data tokenizer [https://www.pi.website/research/fast](https://www.pi.website/research/fast)  
PI opensource: [https://github.com/allenzren/open-pi-zero](https://github.com/allenzren/open-pi-zero)  
CONRFT: [https://github.com/cccedric/conrft](https://github.com/cccedric/conrft)  
HIL SERL | SERL: [https://hil-serl.github.io/](https://hil-serl.github.io/) | [https://serl-robot.github.io/](https://serl-robot.github.io/)  
[https://github.com/Ke-Wang1017/hil-serl/tree/franka_sim](https://github.com/Ke-Wang1017/hil-serl/tree/franka_sim)  
HIL-SERL provides a set of common libraries for users to train RL policies for robotic manipulation tasks. The main structure of running the RL experiments involves having an actor node and a learner node, both of which interact with the robot gym environment
 
Hi guys, i know it is always exciting to see real robots working. But for me who doesn't have a real robot at home and want to try out quickly the simulation is a good first-to-go. Therefore I integrated franka sim environment into hil-serl and managed to record demos and datasets for reward classifier with just a Xbox gamepad
 
Generative Value Learning: [https://generative-value-learning.github.io/](https://generative-value-learning.github.io/)  
Instant Policy - InContext Imitation Learning via Graph Diffusion: [https://www.robot-learning.uk/instant-policy](https://www.robot-learning.uk/instant-policy)
    
**Action Chunking Variants:**  
ACT: [https://www.linkedin.com/pulse/action-chunking-transformer-act-practical-details-dmitriy-shingarey-2ogmf/?trackingId=gWW4dSaESte685iS0%2FE3WA%3D%3D](https://www.linkedin.com/pulse/action-chunking-transformer-act-practical-details-dmitriy-shingarey-2ogmf/?trackingId=gWW4dSaESte685iS0%2FE3WA%3D%3D)  
Act AIM2 [https://generative-value-learning.github.io/](https://generative-value-learning.github.io/)  
Bidrectional decoding [https://bid-robot.github.io/](https://bid-robot.github.io/)  
Dinobot: [https://arxiv.org/html/2402.13181v1](https://arxiv.org/html/2402.13181v1)  
BAKU: An Efficient Transformer for Multi-Task Policy Learning: [https://baku-robot.github.io/](https://baku-robot.github.io/)
 
**Diffusion Variants:**  
[https://github.com/mbreuss/diffusion-literature-for-robotics](https://github.com/mbreuss/diffusion-literature-for-robotics)  
See bottom for summary  
Diffueraser
 
Faster diffusion - Noise search: [https://arxiv.org/abs/2501.09732](https://arxiv.org/abs/2501.09732)
 
Instant Policy: In-Context Imitation Learning via Graph Diffusion [https://www.robot-learning.uk/instant-policy](https://www.robot-learning.uk/instant-policy)  
Diffusion --\> Conditional Flow Matching: [http://pointflowmatch.cs.uni-freiburg.de/](http://pointflowmatch.cs.uni-freiburg.de/)  
Shortcut (Diffusion) Models: [https://arxiv.org/pdf/2410.12557](https://arxiv.org/pdf/2410.12557)  
[OpenAI introduces sCM: Two-Step Consistency Models](https://link.alphasignal.ai/ltsfhM) Match Diffusion Quality with 50x Faster Generation.  
Stateful Diffusion Policies: [https://diff-control.github.io/](https://diff-control.github.io/)  
Diffusion PPO: [https://diffusion-ppo.github.io/](https://diffusion-ppo.github.io/)  
Equivariant Diffusion Policy: [https://arxiv.org/pdf/2407.01812](https://arxiv.org/pdf/2407.01812)  
Clean Defuser: [https://github.com/CleanDiffuserTeam/CleanDiffuser](https://github.com/CleanDiffuserTeam/CleanDiffuser)  
More diffusers [https://arxiv.org/abs/2407.05530](https://arxiv.org/abs/2407.05530)  
Stable diffusion for joint-actions: [https://genima-robot.github.io/](https://genima-robot.github.io/)  
Diffusion Forcing: [https://boyuan.space/diffusion-forcing/](https://boyuan.space/diffusion-forcing/)
 
**MPCS:**

You can look into the TD-MPC family:

- TD-MPC: [https://arxiv.org/abs/2203.04955](https://arxiv.org/abs/2203.04955)
- FOWM: [https://www.yunhaifeng.com/FOWM/](https://www.yunhaifeng.com/FOWM/)
- TD-MPC2: [https://www.tdmpc2.com/](https://www.tdmpc2.com/)

LeRobot Tech Talk by Nicklas Hansen (first author TD-MPC): [https://www.youtube.com/watch?v=5d9W0I2mpNg](https://www.youtube.com/watch?v=5d9W0I2mpNg)  
RL MPC for Locomotion: [https://arxiv.org/abs/2407.17683](https://arxiv.org/abs/2407.17683)

\> From \<[https://discord.com/channels/1216765309076115607/1216765309558722622](https://discord.com/channels/1216765309076115607/1216765309558722622)\>     

\> From \<[https://discord.com/channels/1216765309076115607/1216765309558722622](https://discord.com/channels/1216765309076115607/1216765309558722622)\>     

**RL Adjustment:**  
Many Quadrupeds, Policy Aggregation: [https://arxiv.org/pdf/2310.10486.pdf](https://arxiv.org/pdf/2310.10486.pdf)  
Sprint (downstream RL adjustment): [https://rasc.usc.edu/blog/llms-adapt-robots/](https://rasc.usc.edu/blog/llms-adapt-robots/)  
Policy Adaptation via Language Optimization: Decomposing Tasks for Few-Shot Imitation [https://arxiv.org/abs/2408.16228](https://arxiv.org/abs/2408.16228)  
Adaptive cloning + downstream adjustment: [https://open-world-mobilemanip.github.io/](https://open-world-mobilemanip.github.io/)  
Affrodance based policy adjustment: [https://policy-decomposition.github.io/Images/paper.pdf](https://policy-decomposition.github.io/Images/paper.pdf)  
Consistency distillation for action policy: [https://arxiv.org/abs/2405.07503](https://arxiv.org/abs/2405.07503)