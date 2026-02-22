Reasoning Models 2.0, combine Reasoning with Tool Use! ✨ START teaches LLMs to use tools, such as code interpreter to improve reasoning and problem-solving. Self-taught Reasoner with Tools (START) integrates tool usage with chain-of-thought reasoning by enabling tool calls, self-check, exploration, and self-debug while reasoning using a self-learning framework. 👀
 
Implementation  
1️⃣ Collect math problems (AIME, MATH) and coding tasks (Codeforces, LiveCodeBench)  
2️⃣ Create context-specific hints like "Maybe using Python here is a good idea"  
3️⃣ Generate tool-assisted reasoning data (insert hints after conjunctions like "Wait" and before stop tokens)  
6️⃣ Score trajectories, remove repetitive patterns, and create a seed dataset with successful tool-assisted reasoning examples.  
7️⃣ Fine-tune model on seed dataset, then self self-Distill to generate more diverse reasoning trajectories  
6️⃣ Fine-tune the base model using rejection sampling (RFT) on the extended dataset
 
Insights  
💡 Improves math accuracy by +15% (AMC23: 95.0%) and coding by +38.6% on medium problems.  
📈 Test-time scaling via sequential hints boosts AIME24 performance by 12%.  
🐞 Code template modification reduces debug errors by 41% in training data.  
💡 Adding tools (Python interpreter) improves performance more than adding more training data.  
🧠 Large models already possess latent tool-using abilities that can be activated through hints.  
🛠️ Two-phase training (Hint-RFT then RFT) allows the model to learn effective tool usage.  
📍 Hint place selection is important. After conjunction Token and before stop token.
 
Paper: [https://lnkd.in/emF_m8Qz](https://lnkd.in/emF_m8Qz)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>