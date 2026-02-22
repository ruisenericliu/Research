Why RL Can’t Teach Thinking: Lessons from Self-Improving LLMs
 
After reading Cognitive Behaviors that Enable Self-Improving Reasoners, I realized a key insight: Reinforcement Learning only amplifies what a model already knows how to do. If your LLM lacks reasoning primitives like backtracking or verification, RL won't magically teach them. Before any RL training, we must check for these cognitive behaviors—if missing, we inject them through SFT. This paper changed how I plan model training: reason first, reinforce later. No more blind RL. Smart thinking starts with smart scaffolding.
 
[https://arxiv.org/abs/2503.01307](https://arxiv.org/abs/2503.01307)
 
Cognitive Behaviors that Enable Self-Improving Reasoners, or, Four Habits of Highly Effective STaRs
 
Test-time inference has emerged as a powerful paradigm for enabling language models to ``think'' longer and more carefully about complex challenges, much like skilled human experts. While reinforcement learning (RL) can drive self-improvement in language models on verifiable tasks, **some models exhibit substantial gains while others quickly plateau**. For instance, we find that Qwen-2.5-3B far exceeds Llama-3.2-3B under identical RL training for the game of Countdown. This discrepancy raises a critical question: what intrinsic properties enable effective self-improvement? We introduce a framework to investigate this question by analyzing four key cognitive behaviors -- **verification, backtracking, subgoal setting, and backward chaining** -- that both expert human problem solvers and successful language models employ. Our study reveals that Qwen naturally exhibits these reasoning behaviors, whereas Llama initially lacks them. In systematic experimentation with controlled behavioral datasets, we find that priming Llama with examples containing these reasoning behaviors enables substantial improvements during RL, matching or exceeding Qwen's performance. Importantly, the presence of reasoning behaviors, rather than correctness of answers, proves to be the critical factor -- models primed with incorrect solutions containing proper reasoning patterns achieve comparable performance to those trained on correct solutions. Finally, leveraging continued pretraining with OpenWebMath data, filtered to amplify reasoning behaviors, enables the Llama model to match Qwen's self-improvement trajectory. Our findings establish a fundamental relationship between initial reasoning behaviors and the capacity for improvement, explaining why some language models effectively utilize additional computation while others plateau.
 \> From \<[https://arxiv.org/abs/2503.01307](https://arxiv.org/abs/2503.01307)\>  

SFT Memorizes, RL Generalizes. New Paper from Google DeepMind shows that Reinforcement Learning generalizes at cross-domain, while SFT primarily memorizes. 👀
 
Experiments  
1️⃣ Model & Tasks: Llama-3.2-Vision-11B; GeneralPoints (text/visual arithmetic game); V-IRL (real-world robot navigation)  
2️⃣ Setup: SFT-only vs RL-only vs hybrid (SFT→RL) pipelines + RL variants: 1/3/5/10 verification iterations (”Reject Sampling”)  
3️⃣ Metrics: In-distribution (ID) vs out-of-distribution (OOD) performance  
4️⃣ Ablations: Applied RL directly to base Llama-3.2 without SFT initialization; Tested extreme SFT overfitting scenarios; Compared computational costs versus performance gains
 
Insights  
💡 Outcome-based rewards are key for effective RL training  
🎯 SFT is necessary for RL training when the backbone model does not follow instructions  
🔢 Multiple verification/Reject Sampling help improve generalization up to ~6%  
🧮 Used Outcome-based/rule-based reward focusing on correctness  
🧠 RL generalizes in rule-based tasks (text & visual), learning transferable principles.  
📈 SFT leads to memorization and struggles with out-of-distribution scenarios.
 
Paper: [https://lnkd.in/eTa4pZpg](https://lnkd.in/eTa4pZpg)  
Github: [https://lnkd.in/eE7BmgzV](https://lnkd.in/eE7BmgzV)  
Model & Data: [https://lnkd.in/eH3394tc](https://lnkd.in/eH3394tc)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>