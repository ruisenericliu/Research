OpenAI Strawberry (o1) is out! We are finally seeing the paradigm of inference-time scaling popularized and deployed in production. As Sutton said in the Bitter Lesson, there're only 2 techniques that scale indefinitely with compute: learning & search. It's time to shift focus to the latter.
 
1. You don't need a huge model to perform reasoning. Lots of parameters are dedicated to memorizing facts, in order to perform well in benchmarks like trivia QA. It is possible to factor out reasoning from knowledge, i.e. a small "reasoning core" that knows how to call tools like browser and code verifier. Pre-training compute may be decreased.
 
2. A huge amount of comput**e is shifted to serving inference instead of pre/post-training. LLMs are text-based simulators. By rolling out many possible strategies and scenarios in the simulator, the model will eventually converge to good solutions.** The process is a well-studied problem like AlphaGo's monte carlo tree search (MCTS).
 
3. OpenAI must have figured out the inference scaling law a long time ago, which academia is just recently discovering. Two papers came out on Arxiv a week apart last month:
 
- Large Language Monkeys: Scaling Inference Compute with Repeated Sampling. Brown et al. finds that DeepSeek-Coder increases from 15.9% with one sample to 56% with 250 samples on SWE-Bench, beating Sonnet-3.5.  
- Scaling LLM Test-Time Compute Optimally can be More Effective than Scaling Model Parameters. Snell et al. finds that PaLM 2-S beats a 14x larger model on MATH with test-time search.
 
4. Productionizing o1 is much harder than nailing the academic benchmarks. For reasoning problems in the wild, how to decide when to stop searching? What's the reward function? Success criterion? When to call tools like code interpreter in the loop? How to factor in the compute cost of those CPU processes? Their research post didn't share much.
 
5. Strawberry easily becomes a data flywheel. If the answer is correct, the entire search trace becomes a mini dataset of training examples, which contain both positive and negative rewards.
 
This in turn improves the reasoning core for future versions of GPT, similar to how AlphaGo’s value network — used to evaluate quality of each board position — improves as MCTS generates more and more refined training data.
 ![No alt text provided for this image](Exported%20image%2020260222202529-0.jpeg)  
![Exported image](Exported%20image%2020260222202533-1.png)

[https://openai.com/index/learning-to-reason-with-llms/](https://openai.com/index/learning-to-reason-with-llms/)
 
OpenAI's big anticipated update is here. [OpenAI](https://www.linkedin.com/company/openai/) o1 is their next iteration! O1 is trained using RL to reason through complex problems step-by-step, more similar to human thought processes (no details on what they mean with that).
 
TL;DR;  
💡 o1 improved reasoning compared to GPT-4o, ranks in the 89th percentile on Codeforces  
🧠 o1 utilizes a unique chain-of-thought process, enabling it to break down problems, correct errors, and adapt its approach. (no detailed information)  
❤️ o1 is favored over GPT-4o in areas requiring strong reasoning, like data analysis, coding, and math.  
🚀 o1-preview should be available in ChatGPT (cannot see it yet) and to trusted API users.  
🤔 No comparisons to [Anthropic](https://www.linkedin.com/company/anthropicresearch/) or [Google DeepMind](https://www.linkedin.com/company/googledeepmind/) Gemini mentioned or included
 
Blog: [https://lnkd.in/e2x9bxk6](https://lnkd.in/e2x9bxk6)
 
Is the moat gone? 🤔
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>     

Here are 5 papers you want to read to understand better how [OpenAI](https://www.linkedin.com/company/openai/) o1 might work. Focusing on Improving LLM reasoning capabilities for complex tasks via training/RLHF, not prompting. 👀
 
\> Quiet-STaR: Language Models Can Teach Themselves to Think Before Speaking ( [https://lnkd.in/eCPaa-wc](https://lnkd.in/eCPaa-wc)) from Stanford
 
\> Agent Q: Advanced Reasoning and Learning for Autonomous AI Agents ( [https://lnkd.in/eebwEkPi](https://lnkd.in/eebwEkPi)) from MultiOn/Stanford
 
\> Let's Verify Step by Step ( [https://lnkd.in/egf6EpMd](https://lnkd.in/egf6EpMd)) from OpenAI
 
\> V-STaR: Training Verifiers for Self-Taught Reasoners ( [https://lnkd.in/ebRcEKBn](https://lnkd.in/ebRcEKBn)) from Microsoft, Mila**
 
\> Learn Beyond The Answer: Training Language Models with Reflection for Mathematical Reasoning ( [https://lnkd.in/eeeaqm6x](https://lnkd.in/eeeaqm6x)) from Notre Dam, Tencent
 
Not claiming this is how O1 works, but help us better understand it. I ll share summary posts in the coming days. Make sure to follow! 🫡
 \> From \<[https://www.linkedin.com/posts/philipp-schmid-a6a2bb196_here-are-5-papers-you-want-to-read-to-understand-activity-7241017716214571008-eVba/?utm_source=share&utm_medium=member_ios](https://www.linkedin.com/posts/philipp-schmid-a6a2bb196_here-are-5-papers-you-want-to-read-to-understand-activity-7241017716214571008-eVba/?utm_source=share&utm_medium=member_ios)\>     

**How it works:** o1-preview is a preliminary release, and o1-mini is a faster preliminary version that’s particularly effective at coding. OpenAI published an [o1 system card](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VWXJDJ2bNHm0W4VMJsV75HN9YW2L--MX5l6s_PN1TFhv63qgyTW7lCdLW6lZ3pCW76HK022p2pvHW7pP8sl274wdWW1V6ZcB37Q06yW59tnj-4nBDkLW3W32mZ8tzBdMW6GsjqN8d1RKzW60p7l16n88S4W8XQtM14m8JJyW716ZcW5MdbJsW7Srk9l1bJTXHW29DdhG1VCNRPW2WzB8N8LRLGpW4nQRKt31r8pBW3j9kJs4WlFrMW2NyYJH91GBYMW97xnR-6P-DfKW8j1jB62n-m00W6LF5Hx6Pz1ltW28N4vS3MykTQVwGwtq1bp0dCW3cmCtr3t0XTtW5WK72_6xfcF3W4q2Xrq36F7vkW7G05hh4VDDQQf30b-vH04) but hasn’t disclosed details about the new models’ size, architecture, or training. Both models have an input context window of 128,000 tokens. They accept only text tokens, but OpenAI plans to support other media types in future versions.

- o1-preview and o1-mini were trained on data scraped from the web, open-source databases, and proprietary data supplied by partners and OpenAI. The reinforcement learning process rewarded the models for generating desired reasoning steps and for their alignment with human values, goals, and expectations. 
- The beta models process “reasoning tokens” that the company charges for as though they were output tokens although they’re invisible to users. The use of reasoning tokens makes the models slower and costlier to produce output than GPT-4o, but they deliver superior performance in tasks that benefit from step-by-step reasoning. OpenAI provides an example in which o1-preview deciphered enciphered text in which each letter is replaced by two letters that, according to alphabetical order, are equidistant from the intended letter. In other examples, it calculates the pH of a solution of ammonium fluoride and suggests a medical diagnosis based on symptoms that are present and absent.
- o1-preview’s output is limited to around 32,768 tokens, including reasoning tokens, while o1-mini’s is capped at roughly 65,536. OpenAI [recommends](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VWXJDJ2bNHm0W4VMJsV75HN9YW2L--MX5l6s_PN1TFhw03qgyTW95jsWP6lZ3lzW9g2bGF3jP8v7W3F0DLv5Lv9PKW5KR9Dq5XL4RTW6g_RFk2S1-xDW1YwvbY4_C2j7W5gpFMD3dX_skW81HZn110LgjgMdQzLv4nCtGVzhdwX6rW5JyW62-jtz6L-HZ1W1T_ys47PnvDjW23PYkR4SG6wsW1L49w834PqzzW5H25Xk8ZDwSQVqkGDR3L7mv3Vlfpqc8QJwtmN45ZhDh4klWvW6T4gnn8-Kw4nW8KzkZh6599fTW1d2fFF7lrhb4W4k0zn_5lsFkwW5CWq8b1T6qzVW30kJNy6841vyW5h8cBw356lwtW5jn7Dh6z6nhRW6kScKr8lD8k8W7YCn4c4NDdgSW2THh5x7CqlqhW17pVmt18Qj8KW3rMmkz6NV4BXf7Bm7lC04) budgeting 25,000 tokens for reasoning.
- OpenAI keeps the chain of thought hidden to avoid exposing information that wasn’t requested. In addition, it doesn’t want users to try to control the model’s reasoning, and it doesn’t want competitors to see what’s going on behind the scenes. (Nonetheless, ChatGPT users can see a summary of steps that led to a given response)
- OpenAI and third parties conducted safety evaluations, including testing for inappropriate outputs, race, gender, and age biases, and harmful chains of thought. o1-preview and o1-mini returned fewer hallucinations and showed more resistance to jailbreaking attacks than GPT-4o and GPT-4o mini. Both models show a higher risk than previous OpenAI models of helping to produce biological threats, but the risk is within the bounds of its safety policy.

**Results:** The actual o1 model — which remains unavailable — generally [outperforms](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VWXJDJ2bNHm0W4VMJsV75HN9YW2L--MX5l6s_PN1TFhv63qgyTW7lCdLW6lZ3mgW3R_Vr93qwlpkW7Hjpn86KRyTJW4B4yg17hRL5YW8qlzKT1zNzCVN1_NpYj1RcgbN4w6VLY8z1XHW6rJVcx2zfYWCW7py-4S7tHZ1cW8kfgHJ1kDW2NW6SCQKw7-Zcy0W1SSpDV4zfx08W3Cs0Vr8CHyzKW6dCg_L2LCxKKW4l2jTw8hz05XW1wzJhN5kVDbHW9hNFWb4nySQlW8dzNDf1kTk-CW6XJkhm2qW1TTN5zVw6wVXBmZW13YCYk2XjJzyVC1ksG1SQMPKW1RQRG61VzDbQW34BTkc6CTy93W5hWL-21-SRJSf4x7D5K04) o1-preview, while both vastly outperform GPT-4o on math, science, and coding benchmarks. 

- **o1:** The forthcoming model outperformed GPT-4o on 54 out of 57 MMLU subcategories that test knowledge in fields like elementary mathematics, U.S. history, and law. It achieved an Elo score of 1,673 on coding contests drawn from the website Codeforces (in which it was allowed 10 submissions for any given problem), putting it in the 89th percentile (human expert level). On the [GPQA](https://info.deeplearning.ai/e3t/Ctc/LX+113/cJhC404/VWXJDJ2bNHm0W4VMJsV75HN9YW2L--MX5l6s_PN1TFhtR3qgyTW6N1vHY6lZ3kWW2Ndtf66ZD31wW7dqnPb4P_KkGW5M6HyN4Ltg5pVpYQX-8QmQv1W4BdL_q70vpwmN6wnGvPpf7HpW9flQlv5JsVDNN5myx6h8XWXbW1ZmGNn3PPPpkN98JJ1Bl3hbhVLNZjW8FsQMDW82NCkV4msd-6W1G_2Cd3TVhxZN1j4QPkG7CdqW6B-WjK35XPxgW61qKf67fDnfnW7pVJnk8z1TbgVDHz6065CNJpW6hqF3H4HNZXWW4LK8nx5jgV-yW6GdxGY8c-x7MW5mTRD42Pk82Xf43FcCn04) Diamond tests of graduate-level knowledge in biology, chemistry, and physics, it scored higher than PhD-level experts recruited by OpenAI. It correctly answered 74 percent of questions from the 2024 USA Math Olympiad qualifier. 
- **o1-preview:** The preview version ranked in the 62nd percentile on Codeforces. Human evaluators preferred its output to that of GPT-4o in response to prompts that tested coding, data analysis, and math. (They preferred GPT-4o’s responses to prompts that requested “personal writing.”)

**Behind the news:** In recent months, Anthropic has been using the tag \<antThinking\> to generate thinking tokens that are hidden from users. However, OpenAI’s implementation in the o1 models takes this capability much further,  
**Why it matters:** The o1 models show that the combination of reinforcement learning and chain-of-thought reasoning can solve problems that large language models generally find challenging. They’re substantially more accurate in domains such as coding, math, and science that have low tolerance for error. However, the fact that the models hide their reasoning from users makes them less transparent and explainable than their predecessors and may make their outstanding performance less valuable in some applications.  
**We’re thinking:** Agentic workflows can significantly improve a system’s ability to reflect, reason, and iterate on its output. Training a model to take such steps directly in response to even general-purpose questions opens an exciting alternative path to better reasoning beyond simply scaling up model size.
 \> From \<[https://mail.google.com/mail/u/0/#inbox/FMfcgzQXJGnzmzhTqtWjxfGjxWLShvzh](https://mail.google.com/mail/u/0/#inbox/FMfcgzQXJGnzmzhTqtWjxfGjxWLShvzh)\>   
Since [OpenAI](https://www.linkedin.com/company/openai/) released o1 models, some raised a question - are they only good because they just generate a lot of tokens? Could we do the same with just regular chain of thought?
 
Now we have a really solid answer based on research from [https://epochai.org/](https://epochai.org/) (excellent organisation btw). They tried to match o1-preview's performance on GPQA benchmark by generating a lot of tokens using 2 methods (Revisions and Majority Voting). They found that while you could get a bit of uplift from generating a lot of tokens, there is no number of tokens that will get you to the o1-preview performance.
 
The implication of this is that OpenAI have really found a way to scale inference compute, meaning that if this approach holds going forward, we could get much better results from letting the model consume more compute as it responds.
 
While we are not used to the idea of waiting for a better result, imagine in the future giving a highly complex task to the AI, going for lunch and coming back to a completed piece of work. We are not there yet, but the idea of long inference time should not be taken as a blocker.
 ![No alt text provided for this image](Exported%20image%2020260222202534-2.jpeg)  

Can Anthropic Claude 3.5 sonnet outperform OpenAI o1 in reasoning? Combining Dynamic Chain of Thoughts, reflection, and verbal reinforcement, existing LLMs like Claude 3.5 Sonnet can be prompted to increase test-time compute and match reasoning strong models like OpenAI o1. 👀
 
TL;DR:  
🧠 Combines Dynamic Chain of thoughts + reflection + verbal reinforcement prompting  
📊 Benchmarked against tough academic tests (JEE Advanced, UPSC, IMO, Putnam)  
🏆 Claude 3.5 Sonnet outperforms GPT-4 and matched O1 models  
🔍 LLMs can create internal simulations and take 50+ reasoning steps for complex problems  
📚 Works for smaller, open models like Llama 3.1 8B +10% (Llama 3.1 8B 33/48 vs GPT-4o 36/48)  
❌ Didn’t benchmark like MMLU, MMLU pro, or GPQA due to computing and budget constraints  
📈 High token usage - Claude Sonnet 3.5 used around 1 million tokens for just 7 questions
 
Blog: [https://lnkd.in/e5Z-z4DS](https://lnkd.in/e5Z-z4DS)  
Prompt: [https://lnkd.in/ebEbR4h4](https://lnkd.in/ebEbR4h4)  
Github: [https://lnkd.in/ezvRKbq2](https://lnkd.in/ezvRKbq2)