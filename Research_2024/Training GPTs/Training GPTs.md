Karpathy on simple training GPTS: [https://github.com/karpathy/nanoGPT](https://github.com/karpathy/nanoGPT)  
Youtube video: [Let's build GPT: from scratch, in code, spelled out.](https://www.youtube.com/watch?v=kCc8FmEb1nY)  
[https://x.com/karpathy/status/1811467135279104217](https://x.com/karpathy/status/1811467135279104217) gpt 2 for $672
 
- [Stanford's complete roadmap](https://link.alphasignal.ai/JAHCZw) for training production-ready LLMs. \> From \<[https://mail.google.com/mail/u/0/#inbox/FMfcgzQXJkcLPCXjzvlvtbTRQpGQkFsr](https://mail.google.com/mail/u/0/#inbox/FMfcgzQXJkcLPCXjzvlvtbTRQpGQkFsr)\>      
GPT-Fast: a minimalistic, PyTorch-only decoding implementation loaded with best practices: int8/int4 quantization, speculative decoding, Tensor parallelism, etc. Boosts the "clock speed" of LLM OS by 10x with no model change!
 
This is one of the best tutorial-style repos since Karpathy's minGPT, which is a clean and educational implementation of the most basic GPT training: [https://lnkd.in/gqcr2WYy](https://lnkd.in/gqcr2WYy)
 
We need more minGPTs and GPT-Fasts in the open-source world! Created by the awesome [Horace He](https://www.linkedin.com/in/horacehe/) from PyTorch team.
 
Blog: [https://lnkd.in/gwfstnBy](https://lnkd.in/gwfstnBy)  
Code: [https://lnkd.in/gycy4AeE](https://lnkd.in/gycy4AeE)  
Another related repo is Lit-GPT, more feature-rich and complex: [https://lnkd.in/gZzx9CvF](https://lnkd.in/gZzx9CvF)
 \> From \<[https://www.linkedin.com/feed/update/urn:li:activity:7136404458715938816/?updateEntityUrn=urn%3Ali%3Afs_updateV2%3A%28urn%3Ali%3Aactivity%3A7136404458715938816%2CFEED_DETAIL%2CEMPTY%2CDEFAULT%2Cfalse%29](https://www.linkedin.com/feed/update/urn:li:activity:7136404458715938816/?updateEntityUrn=urn%3Ali%3Afs_updateV2%3A%28urn%3Ali%3Aactivity%3A7136404458715938816%2CFEED_DETAIL%2CEMPTY%2CDEFAULT%2Cfalse%29)\>   
Code for GPT2 in C: [https://github.com/karpathy/llm.c](https://github.com/karpathy/llm.c)
 \> From \<[https://mail.google.com/mail/u/0/#inbox/FMfcgzQXJkcLPCXjzvlvtbTRQpGQkFsr](https://mail.google.com/mail/u/0/#inbox/FMfcgzQXJkcLPCXjzvlvtbTRQpGQkFsr)\>      ![Embedded YouTube video](https://www.youtube.com/embed/kCc8FmEb1nY?feature=oembed&autoplay=true)         \> From \<[https://www.linkedin.com/feed/update/urn:li:activity:7136404458715938816/?updateEntityUrn=urn%3Ali%3Afs_updateV2%3A%28urn%3Ali%3Aactivity%3A7136404458715938816%2CFEED_DETAIL%2CEMPTY%2CDEFAULT%2Cfalse%29](https://www.linkedin.com/feed/update/urn:li:activity:7136404458715938816/?updateEntityUrn=urn%3Ali%3Afs_updateV2%3A%28urn%3Ali%3Aactivity%3A7136404458715938816%2CFEED_DETAIL%2CEMPTY%2CDEFAULT%2Cfalse%29)\>   
Simplified explanations in:
 
[https://arxiv.org/abs/2303.17564](https://arxiv.org/abs/2303.17564)

Non-training augmentations:
 
Trying to create a language model that understands your own custom data? Here are techniques you can use to create a “specialized” LLM, ordered in terms of the amount of complexity/compute involved…
 
TL;DR: When trying to solve problems with language models, we should start simple and only introduce complexity as needed. Along these lines, we can just try to prompt the model first, then try a RAG approach. If this doesn’t work, we can then finetune the model, starting with LoRA (i.e., a much cheaper finetuning approach) instead of end-to-end finetuning.
 
(1) Prompting: The first step in attempting to solve a problem with an LLM is just writing a prompt! Start with a simple prompt, try adding few-shot exemplars, test different instructions, and potentially even use a more complex prompting approach (e.g., chain of thought prompting). If your desired application can be solved via prompting, this is the easiest approach in terms of time/effort.
 
(2) Retrieval Augmented Generation (RAG) is still just a form of prompting. However, we retrieve extra context to include in the language model’s prompt. First, we take all of the domain-specific data we have, split it into chunks and index/store these chunks for search (i.e., a reverse index and/or a vector database). Then, we can retrieve relevant data to include in the model’s prompt when generating output to reduce hallucinations.
 
(3) LoRA is a parameter-efficient finetuning technique that decomposes the weight update derived from finetuning into a low rank decomposition. By doing this, we minimize the number of trainable parameters during finetuning, thus drastically reducing memory overhead. However, we can achieve comparable performance to full finetuning and add no extra inference latency because this low rank weight update can be “baked in” to the existing weight matrix.
 
(4) Full Finetuning: If none of the above techniques work, one of the last strategies that we can try is finetuning the language model end-to-end. To make this successful, we want to curate a large corpus of data that contains useful knowledge relevant to problems that we are trying to solve. Then, we can further train the full model using a next token prediction strategy that is similar to pretraining, thus specializing the model over the specific domain of knowledge contained in the finetuning corpus.
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>