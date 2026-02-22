**Andrew Ng (Stanford)**
 
Dear friends,  
   
The buzz over DeepSeek this week crystallized, for many people, a few important trends that have been happening in plain sight: (i) China is catching up to the U.S. in generative AI, with implications for the AI supply chain. (ii) Open weight models are commoditizing the foundation-model layer, which creates opportunities for application builders. (iii) Scaling up isn’t the only path to AI progress. Despite the massive focus on and hype around processing power, algorithmic innovations are rapidly pushing down training costs. 
 
About a week ago, DeepSeek, a company based in China, released DeepSeek-R1, a remarkable model whose performance on benchmarks is comparable to OpenAI’s o1. Further, it was released as an open weight model with a permissive MIT license. At Davos last week, I got a lot of questions about it from non-technical business leaders. And on Monday, the stock market saw a “DeepSeek selloff”: The share prices of Nvidia and a number of other U.S. tech companies plunged. (As of the time of writing, they have recovered somewhat.) 
 
Here’s what I think DeepSeek has caused many people to realize: 
 
China is catching up to the U.S. in generative AI. When ChatGPT was launched in November 2022, the U.S. was significantly ahead of China in generative AI. Impressions change slowly, and so even recently I heard friends in both the U.S. and China say they thought China was behind. But in reality, this gap has rapidly eroded over the past two years. With models from China such as Qwen (which my teams have used for months), Kimi, InternVL, and DeepSeek, China had clearly been closing the gap, and in areas such as video generation there were already moments where China seemed to be in the lead. 
 
I’m thrilled that DeepSeek-R1 was released as an open weight model, with a technical report that shares many details. In contrast, a number of U.S. companies have pushed for regulation to stifle open source by hyping up hypothetical AI dangers such as human extinction. It is now clear that open source/open weight models are a key part of the AI supply chain: Many companies will use them. If the U.S. continues to stymie open source, China will come to dominate this part of the supply chain and many businesses will end up using models that reflect China’s values much more than America’s.
 
Open weight models are commoditizing the foundation-model layer. As I wrote previously, LLM token prices have been falling rapidly, and open weights have contributed to this trend and given developers more choice. OpenAI’s o1 costs $60 per million output tokens; DeepSeek R1 costs $2.19. This nearly 30x difference brought the trend of falling prices to the attention of many people. 
 
The business of training foundation models and selling API access is tough. Many companies in this area are still looking for a path to recouping the massive cost of model training. The article “AI’s $600B Question” lays out the challenge well (but, to be clear, I think the foundation model companies are doing great work, and I hope they succeed). In contrast, building applications on top of foundation models presents many great business opportunities. Now that others have spent billions training such models, you can access these models for mere dollars to build customer service chatbots, email summarizers, AI doctors, legal document assistants, and much more.  
   
Scaling up isn’t the only path to AI progress. There’s been a lot of hype around scaling up models as a way to drive progress. To be fair, I was an early proponent of scaling up models. A number of companies raised billions of dollars by generating buzz around the narrative that, with more capital, they could (i) scale up and (ii) predictably drive improvements. Consequently, there has been a huge focus on scaling up, as opposed to a more nuanced view that gives due attention to the many different ways we can make progress. Driven in part by the U.S. AI chip embargo, the DeepSeek team had to innovate on many optimizations to run on less-capable H800 GPUs rather than H100s, leading ultimately to a model trained (omitting research costs) for under $6M of compute.  
   
It remains to be seen if this will actually reduce demand for compute. Sometimes making each unit of a good cheaper can result in more dollars in total going to buy that good. I think the demand for intelligence and compute has practically no ceiling over the long term, so I remain bullish that humanity will use more intelligence even as it gets cheaper.
 
I saw many different interpretations of DeepSeek’s progress on social media, as if it was a Rorschach test that allowed many people to project their own meaning onto it. I think DeepSeek-R1 has geopolitical implications that are yet to be worked out. And it’s also great for AI application builders. My team is already brainstorming ideas that are newly possible only because we have easy access to an open advanced reasoning model. This continues to be a great time to build!  
   
Keep learning,  
Andrew 
 
--------------------------
 
Reinforcement learning is emerging as an avenue for building large language models with advanced reasoning capabilities.  
**What’s new:** Two recent high-performance models, [DeepSeek-R1](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VVW4RH2KjlBxW7Sx_Yd2C-tvKW3GjFly5rpF8nN3rtP743qgyTW7lCdLW6lZ3mGW21hsBh7LnZ9cW542ZQC69bhz8W859tDN3qYZqtW520Lwr18NWFcW7YcLgK6M_MC2N8rYTXD2_0PsW8LnkC-5T0S0bW12tSsc8pPjfPW6l0Zyf9bNJZzW4ktNz979BCH7W8ycc3j6zc8ByW6hh_Vx88DtbCW21HsHX3clNbSW5C6DKg3wkjmwVPrmbT1Wk5_fW1x0qyF4wGF2SW6tSDMf8z3J2jW59TLFG49lWqRW8kHZgH8Z6Z2-W95Spw428P6HwV9B1RN7x7q8vW30pGZ674wPpcW4Jtpn29lL8TTW6DRc9Y5TW3lTf7HDx5b04) (and its variants including DeepSeek-R1-Zero) and [Kimi k1.5](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VVW4RH2KjlBxW7Sx_Yd2C-tvKW3GjFly5rpF8nN3rtP6P3qgyTW6N1vHY6lZ3p1W53XK722ChbGsW6yypvV13wlDSW8XdTPN2TXdrvN3L6-B_MFGR3W3M35h03D8dP5W4bQHhY5bRB98VGHwf74sxVMQW3zK5T03ts3TJMcPhxyqbKhHW6lGf0n2hJ7Z8W27zzX68tJq4xW5WSPSx20j4WYW7YFKHq4SfRqxW4l6DRW39mryFW7773Gl4CqrvyW5xr2zQ3RwpJyW4h7f7c6JKqkWW7X5mSY4j2nNMW82BM5L7LzX2RW6Y5Mdb1wVQFfW6Q-KnF26z2kdW2NPWNh1_ykgrf8C54lR04), learned to improve their generated lines of reasoning via reinforcement learning. [o1](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VVW4RH2KjlBxW7Sx_Yd2C-tvKW3GjFly5rpF8nN3rtP743qgyTW7lCdLW6lZ3n3N7XQl5KxY74SW9cfpWD5my7hlVvMr9p59X85yCPXk4gf9RW5JMmBf1dsBYvW8SsXRD6zXZQtN8zDV4FDS3w3W4GhG3Y5B1mjmW6Ss54x96M6PjW475v6R3Bq9lgW31kTH530YRCpW3g2slp5Lj1wXW4Zjhfl4XknZ1W4NJbW73s_S_YW3b0BBV8PM8B2W4nMKbF3KlqNzW2-Xr2s9hshdjVqjhJQ2p_yWdN87lPKRHYxZ9W4Vjkct7k9qbZW2-JmMq944Mv1W2rkDG66GZFTFV-BdnV7fhVn5W1cxvPT6rv9Kbf4vZqcT04) pioneered this approach last year.  
**Reinforcement learning (RL) basics:** RL rewards or punishes a model for performing particular actions or achieving certain objectives. Unlike supervised and unsupervised learning, which compare the model's output to a known ground truth, RL doesn’t explicitly tell a model what it should output. Instead, the model starts out behaving randomly and discovers desired behaviors by earning rewards for its actions. This makes RL especially popular for training machine learning models that play games or control robots.   
**How it works:** To improve the [chain of thought](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VVW4RH2KjlBxW7Sx_Yd2C-tvKW3GjFly5rpF8nN3rtP6P3qgyTW6N1vHY6lZ3mCW6_BZtG1m5tcTN22k99FrZDKBW1SLRkV3JY2zRW1CCC-r18m5PXW3L5rbl5DTcKwV2vGwv53jb-XW8C620X5gPCXJV4vhZq57ZVc4N8fBgXhTGQbXW10BQ7f4d7snjW6pzwVR45M0vVW5b00yX6qnd4vW3T6Hxy7fqvcSN7kdMltw036lW5xyLMm6JHd4xW8PGyHG8s06B4W6mylcp1xgzPyW2JWD646NyGKXN4bmlCRt4f-9W4DLvnJ6rM0mWVWdzcY7N_6VvW7ltX363kNY0Pf5Z2P6n04) (CoT) generated by a large language model (LLM), reinforcement learning encourages the model to generate correct solutions to math, coding, science, and other problems that have known solutions. Unlike typical LLM training, in which the model simply generates the next token of its output and receives feedback token by token, this method rewards the model for generating a sequence of reasoning steps that lead to an accurate conclusion, even if doing so requires generating many intermediate tokens between the prompt and the response — to plan an outline, check the conclusion, or reflect on the approach — without explicit training on the reasoning steps to take.

- The DeepSeek team found that fine-tuning via reinforcement learning alone (after pretraining) was sufficient for DeepSeek-R1-Zero to learn problem-solving strategies like double checking its answer. However, the model also showed quirky behaviors such as mixing different languages in its output. The team overcame these issues in DeepSeek-R1 by supervised fine-tuning on a small number of long CoT examples prior to reinforcement learning.
- Similarly, the Kimi k1.5 team found that fine-tuning the model on long CoTs prior to reinforcement learning enabled it to devise its own problem-solving strategies. The resulting long responses proved to be more accurate but also more expensive to generate, so the team added a second round of reinforcement learning that encouraged the model to produce shorter responses. On the [AIME 2024](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VVW4RH2KjlBxW7Sx_Yd2C-tvKW3GjFly5rpF8nN3rtP7n3qgyTW7Y8-PT6lZ3mvW8w6jjG6JrBp1W9713Fb517j7LW7Gjc1B1XwqtRW95gFL_1G4SfqW5nfh284QKp8gW2W9Pfj5tRXlQW7nyXB33YzKxsW97Xw3T6C9bhZMZyhP2mppYpW65gxcn8BWd96V-04y389VpKlW2-VSQV2CDKvfN6ssYDNZXmMZW6mFTt-5qNGPwVw8SYh6Sj42rVXXjYz2ng-xYN7lH8LtG2lXWW3F3Z1b8Wy4gmW6x74wC2PgfSqVp-qLV32qgLsW3GypHt7bv1QBW58hx3_2jWBgpW6F-4YB576BW-W8Z7ZPm57HxHZW5D9pSh1mVj78W5ynkLK41SGwCf7DzC0004) benchmark of advanced math problems, this process reduced the average number of tokens in the response by around 20 percent, and on [MATH-500](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VVW4RH2KjlBxW7Sx_Yd2C-tvKW3GjFly5rpF8nN3rtP743qgyTW7lCdLW6lZ3n_W8z98Vx3XPN-NVp9V_y53RHCHW17JCF53qQT4mW6RKycg26Z312W2MSfT_6qknVZW6Dh2GT7RzpMkW8dQYV22T0ND4W4MKmlG4ChYsjW6zmcqK4TrqcWN7ffqf9Ny-cMW5mNMR86jMfrNVBkB9F4GM4pjW6m_Qrf1mSHCdW7sJCCy1DR7Q6W38Frfm7vsm1pW6zGXlx6b8TTPW556Chw7SJvnSW1pPs1896FFPnW39XxNG6BVxPRW1cnBc88-7XcsW3y8TkS5mYSDnW19kggt9bF2yQW5RqHWj8zrftRV4z7LM1dRQ_Jf1jxBP804), it cut the average number of output tokens by roughly 10 percent.
- OpenAI has [disclosed](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VVW4RH2KjlBxW7Sx_Yd2C-tvKW3GjFly5rpF8nN3rtP743qgyTW7lCdLW6lZ3l4W47PsHQ4DDL9MW5X-7Zn19d7hwW4fjFLs6yPm-zW6RQxtM68VPQpW2nCnCB4BnL51W6TGdSF5b4fNjW3TV_MT4FCgk4W27lQGh1D__F3W5CW_9f1B1M5lW2T7vN81FGf-NN4BQw7_LwgtvW7xrz6537snKRW2btRnF6xXB4pVlzRs18ykcDhW8pWgJW48N39lW8lGpTy3Xkd6qW3D4WmQ3FNmPwW7_T1qc3cmrl8W5jZnHX8ShcNFW47TZ7M79x6WnW7xj4w87ZsKS9W2mGqdR1bvKR1W8NFCGk5Hr2DkW1HT_1k5jj2k8f5_QtK004) limited information about how it trained o1, but team members have said they used reinforcement learning to improve the model’s chain of thought.

**Behind the news:** While RL has been a staple technique for training models to [play games](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VVW4RH2KjlBxW7Sx_Yd2C-tvKW3GjFly5rpF8nN3rtP743qgyTW7lCdLW6lZ3kXW8zc_pw85yTFNW2Pp-K39knlpnN1778W-Y18HYN7MSPxgh-l-lW3y9X9W7hTzgMVRHZTt15DLrHW7fxqB66kPjp-N3GrQ7tyC-DYN5BhRzNg-QBZW3YfT1r328JQbW8_2Bzp7TYZdVW31pprC5WkyL6W1dPQTm13bvc1W163qvV38VdM5W8zt09V1gpPZcW7HlSc42k_9nWMQV10YJ_PxgW284Ccv632jrTW5BhKcm7ggLVfW1v1gpB40kZdmW1gvlzX291l8fW4rzW3v51Br9JN77lq9PlV28jW2Hpl057xkW6Gf7ZZBnn04) and [control robots](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VVW4RH2KjlBxW7Sx_Yd2C-tvKW3GjFly5rpF8nN3rtP743qgyTW7lCdLW6lZ3lpW6wDvDv3FFhC1W7pTz_s6HVPs9W5pppNh4NnlCTW4s9xqq7PFDhDVcGLfb1Vv6KgW6WJb5F2yyztcN8KwBQRpYsW-N2m2lhW-16ycW73cb-K3RYkc8W3n11d-8Tjb9MVGJRWL4R4PvsW50r24l28Sm7MW4KSpxP10mKpfW79hTkR5v47lfW3XPx9J6ZMP5kW35xhG65BmCrjW75Xb0l90_hqsW7qwbSw90RZngVl7Jbl3ckRJrW4LGhP59jyxBfVkxdPr14XVW3W2rWxnj3YFz4fW8FM75N3WtBf2W1_JDtg100Gwxf6Kq3gW04), its role in developing LLMs has been confined to alignment with human preferences. Reinforcement learning to match judgements of humans ([reinforcement learning from human feedback](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VVW4RH2KjlBxW7Sx_Yd2C-tvKW3GjFly5rpF8nN3rtP6P3qgyTW6N1vHY6lZ3m7W1fzyCT6KK_B3W8Y1rcV6XyC3DW7TRGj859-0dtW4PWC6C54Zy4nW5n7PNH1GbG_XN4NTXVpwxbw7W5xkgPZ1lDZxdW1mp1zQ3YzHj6N313j1HxGbnMN4VsSS88H47LW7M2xLf4rQv2RW2znWdk85QbpSN4sdDmNsDhRGW5txx9S3wgltlW48yJ6V73fZ00W8XFPm43yJJzVW5lDKMs1mqcWyW8CqZy92l286BW48Rjxm5rwyPDW5rjKy79hw14pW6RBgVc1M4MB9W9684zN6T4ZnVf9cmdjs04), or RLHF) or AI ([Constitutional AI](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VVW4RH2KjlBxW7Sx_Yd2C-tvKW3GjFly5rpF8nN3rtP6P3qgyTW6N1vHY6lZ3m4VVRf8H4GZMTCW2QWXVM8XgNLLW555KbT3ggF21W43F0Qn1Lx_0TW2KL4Rm8d5tR9W5Gyyr1866F46W94KT5f8pskFcV8WyG_8BCb2jW6fNmy52sYflkW5Z05mF4Cd2PKW8rjGGl8xwvq9W887-pP2l3htrN1Cxc-WQhpLfW3bgCZz4pqLv7W3svt6C3Yldw7W3X1zKd60xrssW8FNSYp49kxGtW7l1sX83GSx44MlWD_ck16rnW8RcTcx1l83ZwW5VDlkx5Tmxm7W6Y8d757z_MXBf5yNyQl04), which uses reinforcement learning from AI feedback or RLAIF) were the primary methods for encouraging LLMs to align with human preferences prior to the development of [direct preference optimization](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VVW4RH2KjlBxW7Sx_Yd2C-tvKW3GjFly5rpF8nN3rtP7H3qgyTW8wLKSR6lZ3m_W1Rxd8N1tz97MW4cSjsV1-xY5ZW2z3f-Q4Qpp8DW81TcwT81V30fW8ssVFy7Dz4jsW4LD3YB7r2w7JN7MQklLnry9HN3ZpT3KQQWwBW1fnmyM7-lsyBW3WHZFs4TJv9cW5rB5-n2d2dPMW5msdtw8Nz-_fW63ymZ_4bV7-1W3F4bV54SQTV5W2xwq1j5tvf5ZN5ff7WGXfkD1W8K1mgv3gBsd7W3sKfNg4C871sVxtgBl5528DnW5G7hmH358KsDVT8wVh4wN_FXW125P5w9fx_9pW8rlX947PtCW9N77CjfhZwFH1W7DSDNc11swD-W9dr4kg2S3QkZW1KTKTH59DyC9W908ShK23wJZkf4zwQt604).  
**Why it matters:** Reinforcement learning has surprising utility in training large language models to reason. As researchers press models into service in more complex tasks — math, coding, animated graphics, and beyond — reinforcement learning is emerging as an important path to progress.  
**We’re thinking:** Less than three years ago, reinforcement learning looked too [finicky](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VVW4RH2KjlBxW7Sx_Yd2C-tvKW3GjFly5rpF8nN3rtP7H3qgyTW8wLKSR6lZ3pHVK5-0g3cDJ66W3LWryg97vbf6W40JQXV2NyBFSW7GNkmk7Cb4f3W5C_nbx6-DnBkVjKn0L17K9xpW3705sB1KrmvzN7tr0ZHd8qhVW1TRl6P7G1CCtW5vT29d1p6p9BW3RJjdp8bm1l4M77qXMHQkLfW61Mc8J91v7hzVt4kKj2jxWddW8t7W_C7XxwbYW1qytSL8ZbcD9W7ML2C878J9fhW5DlSFS6DzN9zW3kJHCQ5wLpwmW1CHGmR1W6dqnW8k5gCB20DbxrN3WbTqy6CB3WW85sfhY7zb7F2W8v9pyf8tTnZNW5_Rxf02rlvy6W6ndy8r7wn8ZrW7XBh9z6Q2VHmW7pH8_y7c1YKhf7Y_Rs804) to be worth the trouble. Now it’s a key direction in language modeling. Machine learning continues to be full of surprising twists!
      

**Phil Schmidt (Hugging Face)**
 
Don’t fall for false DeepSeek R1 news! Deepseek R1 made it to mainstream, but there are so many wrong takes and false information. ℹ️
 
\> No, the training didn’t cost only ~$6M dollars; the compute for the base model (no RL) was equivalent to GPU hours worth $5.5M, excluding ablations, smaller runs, data generation, and any of DeepSeek R1 training.
 
\> No, it's not a side project (maybe started as one). DeepSeek is backed and owned by High-Flyer, a Chinese hedge fund; in 2020, they managed assets of over 7 billion dollars, and their talent includes Olympic medalists in mathematics, physics, and informatics.
 
\> No, they don’t just have a few GPUs. They have ~50k GPUs.
 
\> The real Deepseek R1 is 671B MoE model that needs \> 16x 80GB Memory (16x H100s).
 
\> Yes, the Deepseek R1 671B is really good! And they do great open source and science work \> 2 years already
 
\> There are 6 “distilled” versions. They are fine-tuned Qwen and Llama on 800k samples, (NO RL). Thats not “r1”. The smallest one with 1.5B (Yes, you can run locally, but it’s not near R1).
 
\> Yes, the hosted version on chat(.)deepseek(.)com might use your data to train new models (as per ToS of DS).
 
\> Yes, Open Science and Source will benefit everyone in the long term! Hugging Face is working on a fully open reproduction pipeline
 
If you are curious how Deepseek R1 trained, I wrote a blog: [https://lnkd.in/eKnT7bHC](https://lnkd.in/eKnT7bHC)
 
-------------------------------   Does Deepseek impact how the next iteration of models are built as Llama did? Deepseek shocked the world with its performance, is it because of architectural changes? 🤔 Deepseek V3/R1 includes multiple innovations compared to traditional LLM architecture we know from Llama or other open Models. Here are the main differences and what they mean:
 
Main Architectural Differences:  
1️⃣ Mixture of Experts (MoE): Uses only selected parameters per token, reducing computation while maintaining model quality. Implemented special load balancing loss to ensure even expert utilization of distributed Hardware.  
2️⃣ Multihead Latent Attention (MLA): Reduces memory and computational costs by projecting KQV matrices into a lower-dimensional space.  
3️⃣ Multi-Token Prediction (MTP): Allows parallel token generation, improving throughput by 2-3x.  
4️⃣ FP8 Quantization: Provides up to 75% memory reduction compared to FP32 while maintaining stability through adaptive bit-width scaling and loss-aware quantization techniques.
 
DeepSeek's architectural innovations (MoE, MLA, MTP, and FP8 Quantization) focus on optimizing large-scale training and deployment and serving efficiency. Not single-user or local runtime performance, e.g., MoE requires the same memory footprint as the Dense model despite using fewer parameters per inference, MTP's parallel token generation mainly benefits high-throughput scenarios.
 
The real innovation comes from its training methodology. The team managed to independently find some of the core ideas from OpenAI o1. (Confirmed by [Mark Chen](https://www.linkedin.com/in/markchen90/) Chief Research Officer at @OpenAI). Deepseek used Group Relative Policy Optimization (GRPO) - A more efficient alternative to PPO/DPO for reinforcement learning in a multi-stage training approach combining SFT and RL. The reasoning capabilities emerge through reinforcement learning. Read more here:  
[https://lnkd.in/eKnT7bHC](https://lnkd.in/eKnT7bHC)
 
I am working on blog post to replicate a “mini” R1 and teach a model to “reason” using GRPO. Stay tuned for that. 🚀
   
![Image preview](Exported%20image%2020260222122121-0.jpeg)   
-------------------------------
   

Reinforcement Learning is all you need! Deepseek R1 an open model that rivals [OpenAI](https://www.linkedin.com/company/openai/) o1 and other models on complex reasoning tasks just got released. But how is it trained? 👀 DeepSeek combines reinforcement learning with multi-stage training to achieve reasoning abilities that rival leading closed-source: Base → RL → SFT → RL → SFT → RL
 
0/4 Base → RL: Uses GRPO on ended reasoning text-completions with rule-based Reward Models, e.g. Format, Math, Coding. Leading to coherent long reasoning/reflection CoT but with readability issues.
 
1/4 RL → SFT: Collect up to 10k token long CoT using the previous model and few-shot prompting, then supervise fine-tune it. Leading readable thoughts and structured outputs (\<think\>, \<summary\>).
 
2/4 SFT → RL: Same pipeline as on 0/4 with GRPO focusing on reasoning-intensive tasks (coding, mathematics, science, still rule-based) with additional “language consistency” reward. Leading coherent, readable performance on reasoning tasks
 
3/4 RL → SFT: Collect 600k synthetic samples using Reject Sampling with the model (2/4) focusing on writing, role-playing, and other general-purpose tasks using DS v3 as LLM Judge. Adding additionally 200k samples for factual QA and translation from DS 3 training.
 
4/4 SFT → RL: Use GRPO to improve helpfulness and harmlessness for reasoning tasks. Use rule-based RM for general tasks and use outcome RMs. Leading to DS R1 model
 
Insights  
❌ No, MCTS for search and synthetic data or Process Reward Models (PRM) used  
🧠 RL on Base model lead to “aha moment”, where models learns to coherent “reasoning” longer outputs  
🧠 Pure Reinforcement Learning can lead to strong reasoning abilities in LLMs.  
🚀 SFT before RL can accelerate and stabilize training.  
6️⃣ Trained 6 additional open models including Llama and Qwen on 800k synthetic samples from R1  
🏆 Distilled smaller models outperform previous versions.  
📈 DeepSeek-R1 achieves comparable performance to OpenAI-o1-1217 on reasoning benchmarks like AIME 2024 and MATH-500.  
🎯 Rule-based rewards for accuracy and format prove more effective than complex reward modeling  
🧮 Excels particularly in STEM tasks and long-context question answering
 
Paper: [https://lnkd.in/eSMyVu4q](https://lnkd.in/eSMyVu4q)  
Models: [https://lnkd.in/eAzEi5TA](https://lnkd.in/eAzEi5TA)
 
Read the paper if you are interested in reasoning models. It is very well written and easy to understand. 🤗
      

**Antoine Blondeau (via Yann LeCunn, Meta)**
 
[https://albertoai.substack.com/p/ai-update-22](https://albertoai.substack.com/p/ai-update-22)
 
Monday's [NVIDIA](https://www.linkedin.com/company/nvidia/) stock correction is vastly overblown. This is NOT a "Sputnik moment".
 
Here are a few thoughts in no particular order of importance:
 
1. no-one in the West is going to build an enterprise app and scaled consumer apps on a Chinese API. On the other hand, the fully open sourced [DeepSeek AI](https://www.linkedin.com/company/deepseek-ai/) model will be super useful to many, and as shown by the traffic on [Hugging Face](https://www.linkedin.com/company/huggingface/), it already is. That's more innovation in an already extremely competitive ecosystem.
 
2. Deepseek is built off of Western open source approaches with a surdose of Reinforcement Learning, and Multi-Head Latent Attention, a ground-breaking approach explained in details here ( [https://lnkd.in/d54p5U5i](https://lnkd.in/d54p5U5i)) by my dear colleague [Alberto Pelliccione](https://www.linkedin.com/in/albertopelliccione/), that reduces the amount of memory required to compute a transformer's attention by a factor of 7.5x to 20x. But Deepseek would not exist without [Meta Facebook](https://www.linkedin.com/company/metafacebook/)'s Llama open source disclosures. Conversely, if indeed Deepseek's V3 and R1 model training methodologies can be verified, then the US LLM providers will follow suit, and compete.
 
3. China will do well in the AI space, as the country has a large number of very talented scientists, but the businesses Chinese firms build will be broadly constrained to operating within the Chinese domestic market.
 
4. As demonstrated by [OpenAI](https://www.linkedin.com/company/openai/)'s recent product releases (e.g. Operator), the action is moving towards productization and distribution, i.e. end-user value creation and revenue generation. Sam Altman is building an AI-enabled business, so are [Microsoft](https://www.linkedin.com/company/microsoft/), Meta, [Google](https://www.linkedin.com/company/google/).
 
5. Deepseek is great competition for OpenAI, Google, [Anthropic](https://www.linkedin.com/company/anthropicresearch/), but these firms do not need Deepseek to feel the heat. Competition within US big tech is so intense already that innovation and business building efforts are on an unprecedented scale. And that is going to compound under the Trump administration's deregulation approach. China is the only country that can try and keep up.
 
6. In my book I definitely want LLMs to be as compute-light as possible so that I can assign freed-up GPUs to do multi-modal processing, including video of course, work on spatial intelligence for robotics, or crunch DNA sequences for virus mutation predictions. Each of these problems (and hundreds of others) are massively compute-intensive. It is not like we are going to run out of problems to solve, Deepseek or not.
 
7. Breakthroughs in the AI race are assessed on a daily/weekly/monthly basis. Moats do not last. This is not rocket engineering in the 50s and 60s. Here, startups and big tech alike move at breakneck speed to precisely break things as fast as they can at any layer of the stack. ChatGPT was a welcome "accident", in my view Deepseek is a similar, welcome, accident. These accidents happen in places where smart people tinker. Critical mass of talent (tinkerers), critical mass of compute, and an environment that rewards innovation, will continue to win the day(s), and that combination is found first and foremost in Silicon Valley.
   

**Jim Fan (Nvidia)**
 
We are living in a timeline where a non-US company is keeping the original mission of OpenAI alive - truly open, frontier research that empowers all. It makes no sense. The most entertaining outcome is the most likely.
 
DeepSeek-R1 not only open-sources a barrage of models but also spills all the training secrets. They are perhaps the first OSS project that shows major, sustained growth of an RL flywheel.
 
Impact can be done by "ASI achieved internally" or mythical names like "Project Strawberry".  
Impact can also be done by simply dumping the raw algorithms and matplotlib learning curves.
 
I'm reading the paper:
 
\> Purely driven by RL, no SFT at all ("cold start"). Reminiscent of AlphaZero - master Go, Shogi, and Chess from scratch, without imitating human grandmaster moves first. This is the most significant takeaway from the paper.  
\> Use groundtruth rewards computed by hardcoded rules. Avoid any learned reward models that RL can easily hack against.  
\> Thinking time of the model steadily increases as training proceeds - this is not pre-programmed, but an emergent property!  
\> Emergence of self-reflection and exploration behaviors.  
\> GRPO instead of PPO: it removes the critic net from PPO and uses the average reward of multiple samples instead. Simple method to reduce memory use. Note that GRPO was also invented by DeepSeek in Feb 2024 ... what a cracked team.
 
DeepSeek R1, model weights are under MIT License (!!): [https://lnkd.in/gaXP9J2D](https://lnkd.in/gaXP9J2D)  
Whitepaper: [https://lnkd.in/gSprEY-B](https://lnkd.in/gSprEY-B)
 
-------------------------------
 
That a *second* paper dropped with tons of RL flywheel secrets and *multimodal* o1-style reasoning is not on my bingo card today. Kimi's (another startup) and DeepSeek's papers remarkably converged on similar findings:
 
\> No need for complex tree search like MCTS. Just linearize the thought trace and do good old autoregressive prediction;  
\> No need for value functions that require another expensive copy of the model;  
\> No need for dense reward modeling. Rely as much as possible on groundtruth, end result.
 
Differences:
 
\> DeepSeek does AlphaZero approach - purely bootstrap through RL w/o human input, i.e. "cold start". Kimi does AlphaGo-Master approach: light SFT to warm up through prompt-engineered CoT traces.  
\> DeepSeek weights are MIT license (thought leadership!); Kimi does not have a model release yet.  
\> Kimi shows strong multimodal performance (!) on benchmarks like MathVista, which requires visual understanding of geometry, IQ tests, etc.  
\> Kimi paper has a LOT more details on the system design: RL infrastructure, hybrid cluster, code sandbox, parallelism strategies; and learning details: long context, CoT compression, curriculum, sampling strategy, test case generation, etc.
 
Upbeat readings on a holiday! [https://lnkd.in/gURcgekD](https://lnkd.in/gURcgekD)
   

**Marcel Salathe (ETH)**
 
The [hashtag#DeepSeek](https://www.linkedin.com/feed/hashtag/?keywords=deepseek&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7289672555605499905) story will be unfolding over coming weeks and months, but here are two points re compute worth considering:
 
(For context on DeepSeek, see my post from two days ago about their impressive new models: [https://lnkd.in/ehWFA8Qm](https://lnkd.in/ehWFA8Qm))
 
🤔 The compute paradox: For years, the formula was simple - more data + more compute = better models. DeepSeek showed we can build powerful models, even reasoning ones, with "relatively little" compute. End of the compute era? Not quite, perhaps the opposite: reasoning models get better the more you give them compute to "think" - which is why the focus is shifting from training compute to test-time compute (i.e. when you use the model).
 
💰 The investment angle: Some worry this efficiency breakthrough means chip makers and announcements like Stargate are "peak hype". If you believe that demand for AI is fixed, clearly this is bad news for these types of investments. If you believe that demand for AI is compute-constrained (i.e. 10x more efficient models will simply lead to 10x more use), these investment make sense. I personally subscribe to the second view.
 
If you want a deeper analysis of what this means, this is the best deep dive I've found, in form of a long (60min) but extremely well-informed article: [https://lnkd.in/e2X5Xi6E](https://lnkd.in/e2X5Xi6E)
    
Dario Amodei (Anthropic CEO)
 ![No alternative text description for this image](Exported%20image%2020260222122122-1.jpeg)  

[https://darioamodei.com/on-deepseek-and-export-controls](https://darioamodei.com/on-deepseek-and-export-controls)

Workflows:
   

Aymeric Roucher (Hugging Face)
 
I just ran [DeepSeek AI](https://www.linkedin.com/company/deepseek-ai/)'s newest reasoning model R1 on smolagents benchmark.  
➡️ It's an absolute beast 🤯🤯
 
The team at DeepSeek really cooked, putting this open model on top of the world. Looking forward to whichever crazy stuff the Chinese ecosystem creates next!
 
The smolagents benchmark only tests a sample of questions, with a basic CodeAgent setup.  
It's available here 👉 [https://lnkd.in/gR_A-jbf](https://lnkd.in/gR_A-jbf)
 \> From \<[https://www.linkedin.com/feed/update/urn:li:activity:7287512560256368641/](https://www.linkedin.com/feed/update/urn:li:activity:7287512560256368641/)\>     

**Phil Schmidt (Hugging Face)**
 
My new workflow for generating test & validation data for new AI use cases using Reasoning Models like [Google DeepMind](https://www.linkedin.com/company/googledeepmind/) Gemini Flash Thinking, [OpenAI](https://www.linkedin.com/company/openai/) o1, or DeepSeek:
 
1️⃣ Prompt Reasoning LLM with a short description of the task you want to solve and that it should generate detailed task instructions, including definitions, clear goals, examples, and output format for expert workers.
 
2️⃣ Refine the task instructions together with the reasoning LLM
 
3️⃣ Prompt the Reasoning LLM to generate verification samples and include your work instructions, e.g.  
\> “You are provided with task instructions for expert workers to classify X. Help me Generate 100 data samples that can be used for verification. Generate them as JSON with a tuple (query, class). Here are the task instructions that are provided to expert workers:”
 
4️⃣ Manually go through the sample data for validated samples that can be used for tests or few-shot prompting
   

Here are the "task instructions" for my use case to classify "Google Search Queries" (Result of steps 1️⃣ and 2️⃣ ):  
👉 [https://lnkd.in/eMw44-Zb](https://lnkd.in/eMw44-Zb)
 ![No alt text provided for this image](Exported%20image%2020260222122123-2.jpeg)   
------
 
How can we build effective agents? 🤔 Efficiency is not defined by the framework you use! Simple, composable patterns outperform complex frameworks, giving you more control and awareness! Anthropic released a good blog post on successful agent patterns.
 
Successful agent patterns:  
1️⃣ Decompose LLM calls into sequential calls (e.g., draft text → check draft → finalize text).  
2️⃣ Use Classifier to direct inputs into specialized prompts or models (e.g., route “refund request” to a refund workflow).  
3️⃣ In dynamic scenarios, use a central “orchestrator” LLM that breaks down tasks into a plan and assigns them to multiple “specialized Agents”.  
4️⃣ Implement cost/iteration limits and automated unit & sandbox testing to verify functionality and keep cost under control  
5️⃣ Invest time in “prompt-engineering” each tool (e.g., designing clear input/output formats and descriptions).
 
Blog: [https://lnkd.in/eqfKWRpj](https://lnkd.in/eqfKWRpj)  
Cookbook: [https://lnkd.in/e5h7RZqA](https://lnkd.in/e5h7RZqA)
 
------
 
Stop treating reasoning models like OpenAI o1 or Google DeepMind Gemini thinking as chat models and start using them as "report generators"! Focus on describing WHAT you want, not HOW you want it done! 👀
 
Guidelines:  
1️⃣ Goal/Instruction: Clearly state what you want to achieve, not how!  
2️⃣ Response Format: Define exactly how you want the information to be structured  
3️⃣ Warnings/Rules: Specify any constraints or requirements that must be followed  
4️⃣ Context Dump: Provide extensive background about your situation - much more than you think necessary
 
Insights:  
💡 Reasoning models aren’t chat models - they are one-shot report generator  
📖 Provide 10× more context than you think you need  
🎯 Focus on describing WHAT you want, not HOW you want it done  
📚 Use it for large, one-shot tasks (e.g. entire file generation, complex planning)  
⚠️ Struggles with specific writing styles/voices - defaults to academic/corporate tone  
🎨 UX improvement needed: Better hierarchy navigation, context management
 
Blog: [https://lnkd.in/ekHf4kWF](https://lnkd.in/ekHf4kWF)
 
Kudos to Shawn swyx W and Ben Hylak for this awesome and thorough write-up!
   

LangChain:
 
🤖 Multi-Agent Orchestration Tutorial
 
A guide showing how to build AI multi-agent systems with LangGraph. Create specialized agents for research, RAG & NL2SQL tasks, coordinated by a supervisor agent to work together seamlessly.
 
Learn more: [https://lnkd.in/gTnBKRnw](https://lnkd.in/gTnBKRnw)