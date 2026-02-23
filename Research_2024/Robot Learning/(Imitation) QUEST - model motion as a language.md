Ever wondered if we can model motion as a language?  
can we tokenize this new language?  
And notably, is it useful? Turns out tremendously!
 
In out latest [hashtag#NeurIPS2024](https://www.linkedin.com/feed/hashtag/?keywords=neurips2024&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7248513306842271744) paper on QueST: Self-Supervised Skill Abstractions for Learning Continuous Control, we find that action tokenization matters a lot!
 
We can learn skill encodings by representing temporal action abstractions with a discrete codebook. This enables 2 things  
1. Better Behaviour Cloning: we can better assimilate multi-task data (\>9%) over best paper. This is currently best in class BC method!  
2. Generalization of this language to represent new tasks in 5-shot transfer to longer horizon tasks!
 
QueST is a multitask latent-variable model that learns sharable low-level skills and outperforms Diffusion Policy, ACT and VQ-BeT by \>13% in 5-shot transfer  
💡 The key insight is to learn shareable state-independent low-level skill encodings by representing temporal action abstractions (1-2 secs motion) with a sequence of discrete codebook entries (skill-tokens)
 
We achieve this through our unique autoencoder architecture, specifically designed to impart causal inductive bias from action sequence data into the latent space. Then, we learn an autoregressive prior over the skill-tokens conditioned on observation and task encodings
 
🥇 QueST achieves SOTA performance, surpassing all other baselines by an absolute margin of 13% in 5-shot transfer, and by at least 9% in multitask setting on LIBERO.  
We compare against VQ-BeT, Diffusion Policy, ACT, PRISE etc. on LIBERO and MetaWorld benchmarks.
 
Interestingly, QueST's autoencoder does not need finetuning for solving downstream tasks, suggesting it can effectively extrapolate in learned skill space and combine the skill tokens to generalize to unseen action sequences.
 
Once trained on a large enough dataset like OpenX Embodiment, QueST’s semantically-sound, temporally abstracted tokenization might better facilitate the learning of large behavior models like RT2 and OpenVLA as compared to their currently used freq-based discretization schemes.
 
🌐 And check out more details at: [https://lnkd.in/edzxqgqw](https://lnkd.in/edzxqgqw)  
🖥️ Code: [https://lnkd.in/eYppqTSi](https://lnkd.in/eYppqTSi)  
Paper: [https://lnkd.in/ej7nwn97](https://lnkd.in/ej7nwn97)
 
Joint work with [Atharva Mete](https://www.linkedin.com/in/atharva-mete/), [Albert Wilcox](https://www.linkedin.com/in/albert-wilcox-314898184/), [Haotian Xue](https://www.linkedin.com/in/haotian-xue-gatech/), [Yongxin Chen](https://www.linkedin.com/in/yongxin-chen-31818144/)  
[College of Computing at Georgia Tech](https://www.linkedin.com/company/college-of-computing-at-georgia-tech/), [NVIDIA AI](https://www.linkedin.com/company/nvidia-ai/), [NVIDIA](https://www.linkedin.com/company/nvidia/)
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>