eepSeek R1 moment has come for GUI agents: Rule-based Reinforcement Learning gives better results than SFT with 500x smaller datasets!
 
First, WTF is a GUI agent?  
➡️ It's an agent (i.e. a LLM-powered bot that can use tools) that reads a recording from your screen, and decides based on it what action to do next: click, type text?  
🏆 Once we get these to work well, they will become extremely general and useful assistants. This problem is very exciting: it's far from being cracked, and undergoing fast progress.
 
Traditionally (by which I mean "in the last few months"), GUI agents have been trained with supervised fine-tuning (SFT). This meant, collecting huge datasets of screen captures from people using computers, and using these to fine-tune your model. 📚
 
👉 But last week, a new paper introduced UI-R1, applying DeepSeek's R1-style rule-based reinforcement learning (RL) specifically to GUI action prediction tasks.  
This is big news: with RL, maybe we could build good agents without the need for huge datasets.
 
UI-R1 uses a unified reward function that evaluates multiple responses from models, optimizing via policy algorithms like Group Relative Policy Optimization (GRPO).
 
Specifically, the reward function assesses:  
🎯 Action type accuracy: Does the predicted action match the ground truth?  
📍 Coordinate accuracy (specifically for clicks): Is the predicted click within the correct bounding box?  
📑 Output format: Does the model clearly articulate both its reasoning and final action?
 
Using just 136 carefully selected mobile tasks—compared to 76,000 tasks for larger models like OS-Atlas—UI-R1 shows significant efficiency and improved performance:  
📈 Boosted action prediction accuracy from 76% to 89% on AndroidControl.  
🌐 Outperformed larger, SFT-trained models (e.g., OS-Atlas-7B), demonstrating superior results with vastly fewer data points (136 tasks vs. 76K).  
🔍 Enhanced adaptability and generalization, excelling even in out-of-domain scenarios.
 
The paper tests this RL-based method only in low-level GUI tasks. Could it generalize to more complex interactions? 🧐
 
Read the full paper here : [https://huggingface.co/papers/2503.21620](https://huggingface.co/papers/2503.21620)