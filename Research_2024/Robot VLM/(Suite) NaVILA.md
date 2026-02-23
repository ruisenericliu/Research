Collaborating between [NVIDIA](https://www.linkedin.com/company/nvidia/) and [UC San Diego](https://www.linkedin.com/company/ucsandiego/), we build NaVILA, the foundational navigation VLA for humanoids and quadrupeds. The robot takes a language instruction as input, and navigates in the environment following the sentence autonomously. It moves across any indoor/outdoor scenes without any map or prior knowledge about them.
 
This is enabled by a 2-level framework, a direction I am pushing a lot these days:  
1️⃣ A VLA that outputs mid-level actions, like "turn left 15 degrees", given vision and language instruction inputs.  
2️⃣ A robust RL locomotion controller with visual inputs.
 
This is completely different from the current main-stream VLA works, where the model outputs the low-level action end2end. Our proposed 2-level framework is beneficial for:  
✅ The data used to train the mid-level VLA can be agent agnostic, we use human videos;  
✅ Such VLA is not only trained for action, but also on regular VLM QA tasks, making it not forget about its reasoning capability;  
✅ VLA and RL policy and run in different frequencies. VLA: 1HZ, RL policy: 50HZ;  
✅ The same VLA can be plugged into any robot with just replacing the low-level policy.
 
Website: [https://lnkd.in/gYga9Zpf](https://lnkd.in/gYga9Zpf)  
arxiv: [arxiv.org/abs/2412.04453](http://arxiv.org/abs/2412.04453)
 
The project is led by [An-Chieh Cheng](https://www.linkedin.com/in/anchiehcheng/), [Yandong Ji](https://www.linkedin.com/in/yandong-ji-58a816160/), [Zhaojing Yang](https://www.linkedin.com/in/zhaojing-yang-4a54712a0/) as equal contributors.
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>