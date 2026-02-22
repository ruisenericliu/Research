There's a new super impressive model in the Transformers library!
 
It's called "Prompt Depth Anything" and can accurately estimate depth in images, i.e. tell you how far off each pixel is from the camera, up to 4K resolution. Depth estimation has several applications, like developing 3D representations based on 2D images, or self-driving cars which allow them to estimate how far off pedestrians are for example.
 
It extends an AI model for depth estimation by prompting it. A prompt can be seen as a form of conditioning an AI model. You probably already know how to prompt (vision) language models like ChatGPT. Prompt engineering, i.e. the task of conditioning a model in such a way that you get the best performance out of it, has become a skill. But we can prompt computer vision models too!
 
e.g. Meta's Segment Anything Model (SAM) can be prompted using point or bounding box prompts, after which it will generate a segmentation mask for a specific instance you care about. Inspired by this, the Prompt Depth Anything authors add prompting (conditioning) to an important AI model for depth estimation: Depth Anything - available in Transformers as well.
 
The prompt used here is Apple's LiDAR (the 3D scanner available in your iPhone or iPad). LiDAR is laser technology which targets an object or a surface with a laser and measures the time for the reflected light to return to the receiver. This is also heavily adopted by self-driving cars like Waymo for instance. Hence this can be used to guide/condition the model to improve its performance!
 
That's exactly what the authors at Zhejiang University and ETH Zürich did. It allows to capture accurate point clouds - just based on a video!
 
Now it's available in a few lines of code! Note: you need an iPhone or iPad device to create the prompt ;)
 
Resources:  
- docs: [https://lnkd.in/e5B3FRii](https://lnkd.in/e5B3FRii)  
- demo: [https://lnkd.in/ee9YG_Ps](https://lnkd.in/ee9YG_Ps)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>