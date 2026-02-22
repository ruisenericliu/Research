Don't sleep on new AI at Meta Vision-Language release! 🔥  
Links to all models and datasets in comments, keep reading to learn more 👀
 
Metta dropped swiss army knives for vision with A2.0 license 👏  
\> image/video encoders for vision language modelling and spatial understanding (object detection etc) 👏  
\> The vision LM outperforms InternVL3 and Qwen2.5VL 👏  
\> They also release gigantic video and image datasets
 
The authors attempt to come up with single versatile vision encoder to align on diverse set of tasks.  
They trained Perception Encoder (PE) Core: a new state-of-the-art family of vision encoders that can be aligned for both vision-language and spatial tasks. For zero-shot image tasks, it outperforms latest sota SigLIP2 👏
 
\> Among fine-tuned ones, first one is PE-Spatial. It's a model to detect bounding boxes, segmentation, depth estimation and it outperforms all other models 😮
 
\> Second one is PLM, Perception Language Model, where they combine PE-Core with Qwen2.5 LM 7B. it outperforms all other models (including InternVL3 which was trained with Qwen2.5LM too!)
 
The authors release the following checkpoints in sizes base, large and giant:  
\> 3 PE-Core checkpoints (224, 336, 448)  
\> 2 PE-Lang checkpoints (L, G)  
\> One PE-Spatial (G, 448)  
\> 3 PLM (1B, 3B, 8B)  
\> Datasets
 
Authors release following datasets 📑  
\> PE Video: Gigantic video datasete of 1M videos with 120k expert annotations ⏯️  
\> PLM-Video and PLM-Image: Human and auto-annotated image and video datasets on region-based tasks  
\> PLM-VideoBench: New video benchmark on MCQA
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>        

We are excited to introduce Meta Perception Encoder, a state-of-the-art vision encoder that excels in image and video tasks, surpassing existing models.
 
Read the research paper ➡️ [https://go.fb.me/vkxu6f](https://go.fb.me/vkxu6f)  
Download the dataset ➡️ [https://go.fb.me/50xu4d](https://go.fb.me/50xu4d)  
Download the code ➡️ [https://go.fb.me/iac6rk](https://go.fb.me/iac6rk)  
Download the model➡️ [https://go.fb.me/pety5z](https://go.fb.me/pety5z)
 
Discover how Meta Perception Encoder sets new standards in vision modeling.
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>