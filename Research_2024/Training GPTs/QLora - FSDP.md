Something big happened in open source AI land past week.
 
Finetuning open LLMs (like Mistral, Llama2, Gemma) has required expensive data center-class GPUs, putting this sort of training out of reach for most individuals & smaller teams thus limiting the ability to fine tune these small open source models for very specific tasks.
 
In the last years, two techniques emerged to work around this.
 
1. QLoRA (Quantized Low-Rank Adaptation) combines quantization (reducing the number of bits required to represent each weight in a neural network, thus saving memory) and Low-Rank Adaptation (training small, adaptable parts of the model, called adaptors, instead of the whole model).
 
**2. FSDP (Fully Sharded Data Parallel) distributes the parameters of a large model across multiple GPUs, allowing each GPU to work on a portion of the model simultaneously.**
 
**A team of researchers of** **answer.ai** **combined both techniques and open sourced a system based on FSDP and QLoRA, to enable training a 70b model on consumer-grade hardware (aka standard gaming GPUs).**
 
Effectively this will enable startups to build more competitive LLMs that are going to be competitively good at specific tasks compared to the closed source ones.
 
If you're a dev, you can already play around with this using the popular open source finetuning framework Axolotl. I know I am this weekend :)
 
The article:  
[https://www.answer.ai/posts/2024-03-06-fsdp-qlora.html](https://www.answer.ai/posts/2024-03-06-fsdp-qlora.html)
 
Axolotl example:  
[https://github.com/OpenAccess-AI-Collective/axolotl/blob/main/examples/llama-2/qlora-fsdp.yml](https://github.com/OpenAccess-AI-Collective/axolotl/blob/main/examples/llama-2/qlora-fsdp.yml)
 
Affordable GPU in the cloud to FAFO with:  
[https://jarvislabs.ai/pricing](https://jarvislabs.ai/pricing)
 \> From \<[https://www.linkedin.com/feed/update/urn:li:activity:7172199961898405889/?updateEntityUrn=urn%3Ali%3Afs_updateV2%3A%28urn%3Ali%3Aactivity%3A7172199961898405889%2CFEED_DETAIL%2CEMPTY%2CDEFAULT%2Cfalse%29](https://www.linkedin.com/feed/update/urn:li:activity:7172199961898405889/?updateEntityUrn=urn%3Ali%3Afs_updateV2%3A%28urn%3Ali%3Aactivity%3A7172199961898405889%2CFEED_DETAIL%2CEMPTY%2CDEFAULT%2Cfalse%29)\>