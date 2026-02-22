An interesting reply from François Chollet on X on my tweet last week :)
 
Last Friday, OpenAI unveiled their new o3 model, which is a large language model (LLM) trained using large-scale reinforcement learning to improve the reasoning, math and coding capabilities of models like ChatGPT.
 
Importantly, the team shared some early evaluation results which sets it apart: the model obtains a score of 75.7% on ARC-AGI, a benchmark created by François, in low-compute mode and 87.5% in high-compute mode. ARC-AGI is a puzzle game quite similar to what you'd see in an IQ test. No AI model could get a decent score on this benchmark for the last 5 years, with GPT-4 getting only 2%, whereas humans typically get 85%.
 
An interesting footnote in the blog post shared by François was that the o3 models were shown as "tuned", indicating that OpenAI did include 75% of the public ARC-AGI training examples in its reinforcement learning tuning process.
 
This made me wonder why, as I thought the point of ARC-AGI was to test true generalization of an AI model beyond the same distribution as your training set. Hence I tweeted that they "trained on the training set" - making many people confused as that's what you use a training set for right? It reminded me a bit of the talk by Alec Radford (the person behind GPT, CLIP and Whisper) at ICML '21 where he discussed that the CLIP model was so robust and general thanks to its pre-training on internet-scale web data (figure on the bottom right below).
 
However, training on internet-scale data makes it difficult to know whether the model has effectively already seen examples in its training dataset or not. It might give the illusion of true generalization, since you're theoretically making everything in-distribution. This is a bit in line with a paper that came out this year which shows that CLIP falls short if you test it on true out-of-domain (OOD) generalization (figure on the top right below).
 
The result by OpenAI is nevertheless super impressive and makes me wonder whether they have achieved true generalization with an AI model. I'd be curious to see the results when the model wouldn't have been tuned on any ARC data at all.
 
Resources:  
- ARC-AGI introduction: [https://arcprize.org/arc](https://arcprize.org/arc)  
- François's blog post: [https://lnkd.in/ePkD2vZZ](https://lnkd.in/ePkD2vZZ)  
- OpenAI's o3 evaluation results reveal: [https://lnkd.in/ekuhwcT3](https://lnkd.in/ekuhwcT3)  
- Alec Radford's talk: [https://lnkd.in/egJNBWec](https://lnkd.in/egJNBWec)  
- CLIP's shortcomings on OOD generalization: [https://lnkd.in/eySkMigq](https://lnkd.in/eySkMigq)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>   ![No alt text provided for this image](Exported%20image%2020260222122207-0.jpeg)