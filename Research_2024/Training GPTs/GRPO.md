What is Group Relative Policy Optimization (GRPO)? Deepseek Coder v2 is the best open Code LLM rivaling GPT-4 on coding tasks. As part of the technical report, GRPO is mentioned as RLHF method, but what is it? 🤔
 
GRPO was introduced in the DeepSeekMath Paper earlier this year and is method in designed to improve improve mathematical reasoning capabilities with less memory consumption.
 
Implementation  
1️⃣ Generate multiple outputs for each input question using the current Policy  
2️⃣ Score these outputs using a reward model  
3️⃣ Average the rewards and use it as a baseline to compute the advantages  
4️⃣ Update the Policy to maximize the GRPO objective, which includes the advantages and a KL term
 
Insights  
💡 GRPO doesn't need value function model, reducing memory and complexity  
🔗 GPRO adds the KL term directly to the loss rather than in the reward  
📈 GPRO improved GSM8K and MATH ~5%  
👉 GPRO looks similar to RLOO method (available in TRL)  
🔁 Used Iterative Approach to train new Reward Models  
📊 RL data consisted of 144k CoT prompts from SFT dataset  
🧠 Reward Model was trained using “Math-Shepherd” process
 
RL is “boosting the correct response from TopK rather than the enhancement of fundamental capabilities.”
 
DeepSeekMath: [https://lnkd.in/eGAk_vbG](https://lnkd.in/eGAk_vbG)  
Math-Shepherd: [https://lnkd.in/etUVyBgm](https://lnkd.in/etUVyBgm)
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>