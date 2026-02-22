New RL Method thats better than GRPO! 🤯 ByteDance released a new open source RL method that outperforms GRPO 👀 DAPO or Decoupled Clip and Dynamic sAmpling Policy Optimization (DAPO) achieves 50 points on the AIME 2024 with 50% fewer training steps.
 
TL;DR:  
🏆 50% AIME 2024 accuracy (Qwen2.5-32B), surpassing DeepSeek-R1 with 50% fewer steps.  
🤗 Fully open-source: code (based on verl), training dataset (DAPO-Math-17k), and model weights (soon)  
💡 Clip-Higher: Asymmetric clipping bounds with higher upper bound to prevent entropy collapse  
🔄 Dynamic Sampling: Filters out prompts with 0% or 100% accuracy  
🔍 Token-level Policy Gradient Loss: Prevents excessive response lengths and maintains reasoning quality  
📏 Length-aware penalty: Reduce reward noise for truncated, but potentially valid, long responses.  
✅ Uses simple, robust rule-based verifier based on string normalization and matching  
🛠️ Compared to GRPO: No KL divergence penalty, token-level loss (vs sample-level), asymmetric clip ranges and filtering.  
🥇Qwen2.5-32B DAPO achieves 50 points on AIME vs. GRPO's 30 points  
⚠️ Release excludes Dynamic Sampling in scripts (44% AIME)
 
project page: [https://lnkd.in/ddjyQ3ae](https://lnkd.in/ddjyQ3ae)  
code: [https://lnkd.in/dxTAYy5M](https://lnkd.in/dxTAYy5M)  
paper: [https://lnkd.in/dTihcBNW](https://lnkd.in/dTihcBNW)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>