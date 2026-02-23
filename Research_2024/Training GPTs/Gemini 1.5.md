Jim Fan:
 
Gemini-1.5 Pro has its spotlight stolen today, and people are poking fun at Sora vs Google memes. Well, I think it's the biggest boost in LLM capability so far in 2024. v1.5's 10M token context (1) excels at retrieval; (2) generalizes zero-shot to extremely long instructions like full tutorials and codebases; and (3) works across modalities such as text, audio, and video.
 
Here's a stunning example:
 
v1.5 learns to translate from English to Kalamang purely in context, following a full linguistic manual at inference time. Kalamang is a language spoken by fewer than 200 speakers in western New Guinea. Gemini has never seen this language during training and is only provided with 500 pages of linguistic documentation, a dictionary, and ~400 parallel sentences in context. It basically acquires a sophisticated new skill in the neural activations, instead of gradient finetuning.
 
I talked about the Myth of Context Length many times before: don't get too excited by claims of 1M or even 1B context tokens. LSTMs already achieved literally infinite context length 25 yrs ago!
 
What truly matters is how well the model actually uses the context to solve real-world problems, and Gemini-1.5 has surpassed the SOTA with flying colors. The paper is also well-written with lots of solid quantitative analysis on in-context memorization and generalization.
 
Paper: “Gemini 1.5: Unlocking multimodal understanding across millions of tokens of context” [https://goo.gle/GeminiV1-5](https://goo.gle/GeminiV1-5)
 
Congrats to [Jeff Dean](https://www.linkedin.com/in/ACoAAAuWJMYBN2meCvJgo9MXMDf38oy1bKUY3Q8), [Oriol Vinyals](https://www.linkedin.com/in/ACoAAAEd34sBi3DwfHXn6Hhm2mtcoTIABbAZYZ8), and the team!
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>