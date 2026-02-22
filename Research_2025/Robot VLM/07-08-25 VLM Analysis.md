How well does GPT 4o understand vision? [https://github.com/EPFL-VILAB/fm-vision-evals](https://github.com/EPFL-VILAB/fm-vision-evals)
 
Very cool paper came out of EPFL, Switzerland which investigates whether vision-language models like GPT-4o and Gemini-2.0 Flash can replace task-specific computer vision models.
 
The short answer is: no. The foundation models consistently underperform task-specific state-of-the-art (SOTA) models, typically available in Hugging Face Transformers or Timm, across all tasks.
 
The longer answer is that:  
1. They are respectable generalists, which is remarkable as they are presumably trained primarily on image-text-based tasks.  
2. They perform semantic tasks notably better than geometric ones.  
3. GPT-4o performs the best among non-reasoning models, getting the top position in 4 out of 6 tasks.  
4. Reasoning models like OpenAI o3 show improvements in geometric tasks.  
5. The 'image generation' models such as GPT-4o Image Generation which have been natively trained multimodally, exhibit quirks. E.g., they hallucinate objects, show misalignment between the input and output, etc.  
6. While the prompting techniques affect performance, better models exhibit less sensitivity to variations in prompts. We control for the variance introduced by the prompting methods in our experiments.
 
This is good news for open-source as there's still a use case for fine-tuning! This means:  
- if you want to do image classification, use a model like DINOv2 or SigLIP 2  
- if you want to do object detection, use a model like RT-DETRv2 or D-FINE  
- if you want to do depth estimation, use a model like Depth Anything v2  
- if you want to do image segmentation, use a model like EoMT (see my post last week)  
- etc.
 
Since this paper is pretty cool I've submitted it to Daily Papers here: [https://lnkd.in/eGMxSkhW](https://lnkd.in/eGMxSkhW)  
Source: [https://lnkd.in/eezkVs_r](https://lnkd.in/eezkVs_r)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>