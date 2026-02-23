Can my robot cook my food, tidy my messy table, rearrange my dresser and do much much more without ANY demos or real-world training data?
 
Introducing ManipGen: A generalist agent for manipulation that can solve long-horizon robotics tasks entirely zero shot, from text input!
 
Key idea: for many manipulation tasks of interest, they can be decomposed into two phases, contact-free reaching (aka motion planning!) and contact-rich local interaction. The latter is hard to learn, and we take a sim2real transfer approach!
 
We define local policies, which operate in a local region around an object of interest. They are uniquely well-suited to generalization (see below!) and sim2real transfer.  
This is because they are invariant to:  
1) Absolute pose  
2) Skill orders  
3) Environment configurations
 
As an overview, our approach 1) acquires generalist behaviors for local skills at scale using RL 2) distills these behaviors into visuomotor policies using multitask DAgger and 3) deploys local policies in the real-world using VLMs and motion planning.
 
Phase 1: Train state-based, single-object policies to acquire skills such as picking, placing, opening and closing. We train policies using PPO across thousands of objects, designing reward and observation spaces for efficient learning and effective sim2real transfer.
 
Phase 2: We need visuomotor policies to deploy on robots! We distill single-object experts into multi-task policies using online imitation learning (aka DAgger) that observe local visual (wrist cam) input with edge and hole augmentation to match real-world depth noise.
 
To deploy local policies in the real-world, we decompose the task into components (GPT-4o), estimate where to go using Grounded SAM, and motion plan using Neural MP. For control, we use Industreallib from NVIDIA, an excellent library for sim2real transfer!
 
ManipGen can solve long-horizon tasks in the real-world entirely zero-shot generalizing across objects, poses, environments and scene configurations! We outperform SOTA approaches such as SayCan, OpenVLA, LLMTrajGen and VoxPoser across 50 tasks by 36%, 76%, 62% and 60%!
 
ManipGen exhibits exciting capabilities such as performing manipulation in tight spaces and with clutter, entirely zero-shot! From putting items on the shelf, carefully extracting the red pepper from clutter and putting large items in drawers, ManipGen is quite capable.
 
By training local policies at scale on thousands of objects, ManipGen generalizes to some pretty challenging out of distribution objects that don’t look anything like what was in training, such as pliers and the clamps as well as deformable objects such as the wire.
 
This work was done at [Carnegie Mellon University Robotics Institute](https://www.linkedin.com/company/cmu-ri/), with co-lead [Min Liu](https://www.linkedin.com/in/min-liu-16164321b/), as well as [Deepak Pathak](https://www.linkedin.com/in/pathak22/) and [Russ Salakhutdinov](https://www.linkedin.com/in/russ-salakhutdinov-53a0b610/) and in collaboration with [Walter Talbott](https://www.linkedin.com/in/walter-talbott-678b8aa8/), [Chen Chen, Ph.D.](https://www.linkedin.com/in/chen90/), and [Jian Zhang](https://www.linkedin.com/in/jianzhangpurdue/) from [Apple](https://www.linkedin.com/company/apple/).  
Paper, videos and code (coming soon!) at [https://lnkd.in/ekjWPXHM](https://lnkd.in/ekjWPXHM)
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>     

Neural MP:
 
[https://arxiv.org/pdf/2409.05864](https://arxiv.org/pdf/2409.05864)
   

Industrial REALLib : [https://github.com/NVlabs/industreallib](https://github.com/NVlabs/industreallib)