The Hugging Face team just released some very useful resources for vision-language models (VLMs) in 2025! VLMs are models like ChatGPT which can take images as input.
 
First off, Merve Noyan and team released a very nice overview of everything that happened to VLMs so far, and brings you up to speed with the latest and greatest advancements.
 
This includes model trends, like any-to-any models which can take in any modality (text, vision, audio) and produce any modality as output. Another trend is the "reasoning" or "inference-time compute scaling" one, where models produce a set of reasoning tokens before spitting out their final answer. The Kimi-VL model by Moonshot AI is a great example of that. Finally, the trends of MoE (mixture-of-experts) and smaller models which can run on-device are discussed. Hugging Face made a big effort in this regard with their SmolVLM series, led by Andrés Marafioti.
 
The second part of the blog discusses all the amazing things you can do with them, like detecting or segmenting objects just via prompting. Multimodal RAG now also becomes feasible with models like ColPali - these directly embed screenshots of PDFs rather than OCR'ing them. The final part discusses UI agents (models which directly operate on a computer screen) and video understanding models. Highly recommend if you want to get up to speed!
 
Next to that, Xuan-Son Nguyen made a pretty awesome demo to run SmolVLM on your own laptop. This is to celebrate the fact that llama cpp (a popular framework for running LLMs on-device) now supports VLMs natively!
 
Llama cpp is, as the name suggests, written in the C and C++ programming languages. These are much faster languages than Python, allowing people to run ever-large models fast on-device, like your phone, laptop or NVIDIA Jetson. The framework was born when Meta released LLaMa, one of the first great openly available LLMs. The framework works with a file format called GGUF to efficiently store the weights.
 
It took some time however before llama cpp added native support for VLMs, as this is a non-trivial task. This was done by Son, who maintains the package together with Georgi Gerganov, the original creator. The demo linked below is ran on his Macbook with an M3 chip.
 
Resources:  
- blog: [https://lnkd.in/edwDxjbW](https://lnkd.in/edwDxjbW)  
- Son's demo: [https://lnkd.in/eVvz8jMN](https://lnkd.in/eVvz8jMN)  
- VLM support in llama cpp: [https://lnkd.in/epvN32yn](https://lnkd.in/epvN32yn)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>