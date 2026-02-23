[https://cohere.com/research/papers/back-to-basics-revisiting-reinforce-style-optimization-for-learning-from-human-feedback-in-llms-2024-02-23](https://cohere.com/research/papers/back-to-basics-revisiting-reinforce-style-optimization-for-learning-from-human-feedback-in-llms-2024-02-23)
 
Reinforcement Learning from Human Feedback (RLHF) has established itself as a cornerstone in improving LLMs after fine-tuning (SFT). 🧬 I am excited to share my “RLHF in 2024 with DPO & Hugging Face” guide teaching you how to apply RLHF on open LLMs using DPO, including Flash Attention & Q-LoRA, all built with [Hugging Face](https://www.linkedin.com/company/huggingface/) TRL. 🚀
 
The guide covers full end-to-end DPO example with:  
🧑🏻‍💻 Setup of the development environment  
🧮 Create and prepare the preference dataset  
🏋️‍♀️ Align LLM with TRL and the DPOTrainer  
😎 Test LLM (vibe-check)  
🥇 Evaluate open LLMs on MT-Bench
 
👉  [https://lnkd.in/eWfTtiVP](https://lnkd.in/eWfTtiVP)
 
RLHF in 2024 with DPO & Hugging Face is the continuation of my “How to Fine-Tune LLMs in 2024 with Hugging Face” Blog post. Coming next: Scaling SFT and DPO in multi-GPU/multi-Node environments.🔜
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>      
[https://github.com/huggingface/alignment-handbook](https://github.com/huggingface/alignment-handbook)
 
Aligning LLMs with Human Preferences is one of the most active research areas. 🧪 RLHF, DPO, and SLiC are all techniques for aligning LLMs, but they come with limitations and challenges. 🥷 DeepMind proposed a new method, “Statistical Rejection Sampling Optimization (RSO)” to align and learn from Human Preferences.
 
𝗣𝗿𝗲𝗿𝗲𝗾𝘂𝗶𝘀𝗶𝘁𝗲𝘀:  
📝 Collect pairwise human preferences data, with each example containing a prompt, an accepted response, and a rejected response.  
🧠 Train a pairwise Reward Model on the preference dataset to predict which response is “accepted” for a given prompt.  
🤖 Train an SFT Model on a different instruction dataset
 
𝗥𝗦𝗢 𝗶𝗺𝗽𝗹𝗲𝗺𝗲𝗻𝘁𝗮𝘁𝗶𝗼𝗻:  
𝗦̲𝘁̲𝗲̲𝗽̲ ̲𝟭̲:̲ Sample responses using the SFT Model and rank each response with the Reward Model  
𝗦̲𝘁̲𝗲̲𝗽̲ ̲𝟮̲:̲ Use Statistical rejection sampling to conduct samples favoring higher rewards. Label the selected responses as preference pairs based on the relative reward.  
𝗦̲𝘁̲𝗲̲𝗽̲ ̲𝟯̲:̲ Iteratively train the SFT Model using the new labeled preference pairs with logistic or hinge loss.
 
𝗣𝗮𝗽𝗲𝗿 𝗜𝗻𝘀𝗶𝗴𝗵𝘁𝘀:  
🥇 A good Reward Model is the most important and crucial component of RSO  
🏆 RSO outperforms other methods like SLiC and DPO across diverse tasks.  
✅ Easier to implement than RLHF to learn from human preference  
🔢 Rejection sampling unifies top-k selection and statistical sampling.  
👩‍🔧 Used Amazon Mechanical Turk for human evaluation.  
⚖️ Shows Hinge (SLiC) and logistic Loss (DPO) perform equally well.  
🤖 Used T5 models
 
Check out the full paper: [https://lnkd.in/eDK-PXxs](https://lnkd.in/eDK-PXxs)
 
Remember that these are just my personal findings. Make sure always to conduct your own research and analysis. 🤗
 ![diagram](Exported%20image%2020260222203119-0.jpeg)

_It is only rarely that, after reading a research paper, I feel like giving the authors a standing ovation. But I felt that way after finishing_ _Direct Preference Optimization_ _(DPO) by Rafael Rafailov, Archit Sharma, Eric Mitchell, Stefano Ermon, Chris Manning, and Chelsea Finn._
 
_RLHF became a key algorithm for LLM training thanks to the_ _InstructGPT_ _paper, which adapted the technique to that purpose. A typical implementation of the algorithm works as follows:_ 

- _Get humans to compare pairs of LLM outputs, generated in response to the same prompt, to specify which one they prefer. For example, humans typically prefer the more helpful, less toxic output._
- _Use the human preferences to learn a reward function. The reward function, typically represented using a transformer network, is trained to give a higher reward (or score) to the outputs that the humans preferred._
- _Finally, using the learned reward, run a reinforcement learning algorithm to tune the LLM to (i) maximize the reward of the answers generated, while (ii) not letting the LLM change too much (as a form of regularization)._

_This is a relatively complex algorithm. It needs to separately represent a reward function and an LLM. Also, the final, reinforcement learning step is well known to be finicky to the choice of hyperparameters._
 
_DPO dramatically simplifies the whole thing. Rather than needing separate transformer networks to represent a reward function and an LLM, the authors show how, given an LLM, you can figure out the reward function (plus regularization term) that that LLM is best at maximizing. This collapses the two transformer networks into one. Thus, you now need to train only the LLM and no longer have to deal with a separately trained reward function. The DPO algorithm trains the LLM directly, so as to make the reward function (which is implicitly defined by the LLM) consistent with the human preferences. Further, the authors show that DPO is better at achieving RLHF's optimization objective (that is, (i) and (ii) above) than most implementations of RLHF_
 
_RLHF is a key building block of the most advanced LLMs. It’s fantastic that these Stanford authors — through clever thinking and mathematical insight — seem to have replaced it with something simpler and more elegant. While it's easy to get excited about a piece of research before it has stood the test of time, I am cautiously optimistic that DPO will have a huge impact on LLMs and beyond in the next few years. Indeed, it is already making its way into some top-performing models, such as Mistral’s_ _Mixtral__._  
 \> From \<[https://mail.google.com/mail/u/0/#inbox/FMfcgzGwJckFzvwxdxCDkVDBLTWlWTMT](https://mail.google.com/mail/u/0/#inbox/FMfcgzGwJckFzvwxdxCDkVDBLTWlWTMT)\>