See Page 80 for a general timeline, and aggregation of benchmarks
   

An emerging theme in AI technical performance,  
as emphasized in last year’s report, is the observed  
saturation on many benchmarks
 ![Exported image](Exported%20image%2020260222202652-0.png)

The research indicates that ChatGPT fabricates  
unverifiable information in **approximately 19.5%**  
**of its response**s, with these fabrications spanning  
a variety of topics such as language, climate, and  
technology.
 
Even state-of-the-art LLMs face significant  
challenges with SWE-bench. Claude 2, the  
best-performing model, **solved only 4.8% of the**  
**dataset’s problems (Figure 2.3.4).** 8 In 2023, the top-  
performing model on SWE-bench surpassed the  
best model from 2022 by 4.3 percentage points.
 ![Exported image](Exported%20image%2020260222202654-1.png)

HEIM’s findings indicate that no single model  
excels in all criteria. For human evaluation of  
image-to-text alignment (assessing how well  
the generated image matches the input text),  
OpenAI’s DALL-E 2 scores highest (Figure  
2.4.3). In terms of image quality (gauging if the  
images resemble real photographs), aesthetics  
(evaluating the visual appeal), and originality  
(a measure of novel image generation and  
avoidance of copyright infringement), the Stable  
Diffusion–based Dreamlike Photoreal model  
ranks highest (Figure 2.4.4)
 
MVDream is a new 3D generation system developed by  
ByteDance and University of California, San  
Diego researchers that overcomes some of  
these hurdles (Figure 2.4.5).
 
In 2023, researchers from Stanford introduced  
a new model, **ControlNet, that improves**  
**conditional control editing for large text-**  
**to-image diffusion models (Figure 2.4.12).**  
ControlNet stands out for its ability to handle  
various conditioning inputs. Compared to  
other previously released models in 2022,  
human raters prefer ControlNet both in terms  
of superior quality and better condition fidelity  
(Figure 2.4.13).
 
**RealFusion, developed by Oxford researchers,**  
**is a new method for generating complete**  
**3D models of objects from single images,**  
overcoming the challenge of often having  
insufficient information from single images  
for full 360 degree reconstruction.
   

The question formats include charts, maps,  
tables, chemical structures, and more. **MMMU is**  
**one of the most demanding tests of perception,**  
**knowledge, and reasoning in AI to date.** As of  
January 2024, the highest performing model is  
Gemini Ultra, which leads in all subject categories  
with an overall score of **59.4% (Figure 2.6.2).11** On  
most individual task categories, top models are still  
well beyond medium-level human experts (Figure  
2.6.3).  
Note: **Multiple choice is a bit screwed**
 ![Exported image](Exported%20image%2020260222202655-2.png)  
![Exported image](Exported%20image%2020260222202656-3.png)

AgentBench  
AgentBench, a new benchmark designed for  
evaluating LLM-based agents, encompasses eight  
distinct interactive settings, including web browsing,  
online shopping, household management, puzzles,  
and digital card games (Figure 2.8.1). The study  
assessed over 25 LLM-based agents, including those  
built on OpenAI’s GPT-4, Anthropic’s Claude 2, and  
Meta’s Llama 2. GPT-4 emerged as the top performer,  
achieving an overall score of 4.01, significantly  
higher than Claude 2’s score of 2.49 (Figure 2.8.2).  
**The research also suggests that LLMs released in**  
**2023 outperform earlier versions in agentic settings.**  
**Additionally, the AgentBench team speculated that**  
**agents’ struggles on certain benchmark subsections**  
**can be attributed to their limited abilities in long-term**  
**reasoning, decision-making, and instruction-following.**
 
**Robotics**
 
**Palm-E**  
**PaLM-E is significant in that it demonstrates that**  
**language modeling techniques as well as text**  
**data can enhance the performance of AI systems**  
**in nonlanguage domains, like robotics. PaLM-E**  
**also highlights how there are already linguistically**  
**adept robots capable of real-world interaction and**  
**high-level reasoning.**
 
**RT-2**
 
**and adaptable approaches for conditioning robotic**  
**policy. It outshines state-of-the-art models like**  
**Manipulation of Open-World Objects (MOO) across**  
**various benchmarks, particularly in tasks involving**  
**unseen objects. On such tasks, an RT-2/PaLM-E**  
**variant achieves an 80% success rate, significantly**  
**higher than MOO’s (53%) (Figure 2.9.4). In unseen**  
**object tasks, RT-2 surpasses the previous year’s**  
**state-of-the-art model, RT-1, by 43 percentage**  
**Points.**
 
**RLHF:**
 
Reinforcement learning has gained popularity  
in enhancing state-of-the-art language models  
like GPT-4 and Llama 2. Introduced in 2017,  
Reinforcement Learning from Human Feedback  
(RLHF) incorporates human feedback into the  
reward function, enabling models to be trained for  
characteristics like helpfulness and harmlessness.
 
**DPO**:
 
In response, researchers from Stanford and CZ  
Biohub have developed a new reinforcement  
learning algorithm for aligning models named  
Direct Preference Optimization (DPO). DPO is  
simpler than RLHF but equally effective. The  
researchers show that DPO is as effective as other  
existing alignment methods, such as Proximal  
Policy Optimization (PPO) and Supervised Fine-  
Tuning (SFT), on tasks like summarization (Figure  
2.10.5)
 
**No emergent properties:**
 
However, research from Stanford challenges this  
notion, arguing that the **perceived emergence of new**  
**capabilities is often a reflection of the benchmarks**  
**used for evaluation rather than an inherent property**  
**of the models themselves. The researchers found**  
**that when nonlinear or discontinuous metrics like**  
**multiple-choice grading are used to evaluate**  
**models, emergent abilities seem more apparent.**  
**In contrast, when linear or continuous metrics**  
**are employed, these abilities largely vanish.**
 
**LLMs are poor self-correctors:**  
Researchers from DeepMind and the University  
of Illinois at Urbana–Champaign tested GPT-4’s  
performance on three reasoning benchmarks:  
GSM8K (grade-school math), CommonSenseQA  
(common-sense reasoning), and HotpotQA  
(multidocument reasoning). They found that when  
the model was left to decide on self-correction  
without guidance, its performance declined across  
all tested benchmarks (Figure 2.11.3)
 
**LLM improvement**
 
**Chain of thought (CoT) and Tree of Thoughts**  
**(ToT) are prompting method**s that can improve  
the performance of LLMs on reasoning tasks. In  
2023, European researchers introduced another  
prompting method, Graph of Thoughts (GoT), that  
has also shown promise (Figure 2.12.1).
 
**A paper from DeepMind has introduced**  
**Optimization by PROmpting (OPRO),** a method  
that uses LLMs to iteratively generate prompts  
to improve algorithmic performance. OPRO uses  
natural language to guide LLMs in creating new  
prompts based on problem descriptions and  
previous solutions (Figure 2.12.3).
 
**QLoRA, developed by researchers from the**  
**University of Washington in 2023,** is a new method  
for more efficient model fine-tuning. It dramatically  
reduces memory usage, enabling the fine-tuning  
of a 65 billion parameter model on a single 48  
GB GPU while maintaining full 16-bit fine-tuning  
performance.
 
**Flash-Decoding,** developed by Stanford  
researchers, tackles inefficiency in traditional  
LLMs by speeding up the attention mechanism,  
particularly in tasks requiring long sequences.