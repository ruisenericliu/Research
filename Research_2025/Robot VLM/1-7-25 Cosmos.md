Introducing NVIDIA Cosmos, an open-source, open-weight Video World Model. It's trained on a whopping 20M hours of videos (!!) and weighs from 4B to 14B. To put in perspective, 20M hours is like watching YouTube 24/7 non-stop from the age of Roman Empire to today. Cosmos offers two flavors: diffusion (continuous tokens) and autoregressive (discrete tokens); and two generation modes: text-\>video and text+video-\>video.
 
Physical AI has a big data problem. Synthetic data to the rescue! We apply Cosmos to large-scale synthetic data generation for robotics and autonomous driving, and now you can too! It's all yours to finetune.
 
Check it out: [https://lnkd.in/gbUWrhmP](https://lnkd.in/gbUWrhmP)
    
NVIDIA solved physics and open-sourced it? Can we just build our own autonomous robots now? 🤯  
They released Cosmos: new family of open world foundation models (WFMs) 🌌  
Unwrapping the release and why it's so revolutionary 🧶 All links to models in the comments 💬
 
They have released 7 models:  
- four autoregressive video2world models  
- four diffusion-based video2world and text2world models  
- prompt upsampler  
- content safety model
 
\> The autoregressive models above can generate future frames when you pass image or an input video of 9 frames and output 24 frames, the video2world ones also accept text input  
\> Diffusion models on the other hand output 120 frames  
\> The models are focused on robotic applications
 
World Foundation Models (WFMs) are essentially pre-trained on open-world video data, which you can then fine-tune it on your specific application with less labels (be it autonomous driving or robotic arms)  
This release matters so much for embodied applications because labelling frames for post-training of robotics models cost a lot of time, it will immensely accelerate the development of the embodied AI 🤖
 
Some of my highlights from the paper ✨  
The release comes with Cosmos Tokenizer, a suite of tokenizers based on sort of an encoder-decoder architecture with temporal convolution and causal temporal attention, they also release their tokenizers on [Hugging Face](https://www.linkedin.com/company/huggingface/)  
The paper is essentially making the separation on how we should model the world generation: should it be next token prediction or LDMs to work within the latent space of the tokenizer  
Across all the downstream fine-tunes, diffusion seems to be the best! 🔥
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>