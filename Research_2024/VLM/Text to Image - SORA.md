Diffusion Transformer calculation by hand: [https://www.linkedin.com/feed/update/urn:li:activity:7165412131188752384?utm_source=share&utm_medium=member_desktop](https://www.linkedin.com/feed/update/urn:li:activity:7165412131188752384?utm_source=share&utm_medium=member_desktop)
 
We represent videos and images as collections of smaller units of data called patches, each of which is akin to a token in GPT. By unifying how we represent data, we can train diffusion transformers on a wider range of visual data than was possible before, spanning different durations, resolutions and aspect ratios.
 \> From \<[https://openai.com/sora](https://openai.com/sora)\>   
Sora builds on past research in DALL·E and GPT models. It uses the recaptioning technique from DALL·E 3, which involves generating highly descriptive captions for the visual training data. As a result, the model is able to follow the user’s text instructions in the generated video more faithfully.
 
In addition to being able to generate a video solely from text instructions, the model is able to take an existing still image and generate a video from it, animating the image’s contents with accuracy and attention to small detail. The model can also take an existing video and extend it or fill in missing frames. [Learn more in our technical report](https://openai.com/research/video-generation-models-as-world-simulators).
 \> From \<[https://openai.com/sora](https://openai.com/sora)\>         
OpenAI has introduced Sora, its latest innovation designed to transform text prompts into detailed videos up to a minute long, marking a significant evolution from the existing text-to-image models.
 
**Key Highlights:**

- **Advanced Video Creation**: Sora stands out by its ability to craft videos featuring multiple characters, diverse motions, and intricate backgrounds directly from textual instructions.
- **Innovative Technology**: The model leverages a combination of diffusion model techniques and Vision Transformers (ViT), embedding video data into a latent space for enhanced processing. This method allows video segments to be treated as tokens, similar to the way language models process text.
- **High-Quality Resolution**: Sora is engineered to support various resolutions, including high-definition formats like 1920x1080p, pushing beyond the conventional 256x256 resolution ceiling seen in many multimodal models.
- **Enhanced Realism**: By applying re-captioning techniques initially developed for DALL·E 3, Sora significantly improves the generation of realistic video patches from noisy inputs, demonstrating a deeper understanding of the physical world.
- **Scalability and Effectiveness**: Thanks to its transformer-based architecture, Sora ensures scalability and effectiveness, underlining the technical sophistication of the model.

Despite its groundbreaking capabilities, Sora faces challenges in accurately simulating complex physics and specific cause-and-effect scenarios, which could affect the precision of its generated videos. OpenAI has yet to release specific performance benchmarks or accuracy rates, choosing instead to focus on the model's broad potential and innovative aspects.
 
**Potential Applications**: Sora is primarily aimed at creative professionals in filmmaking, visual arts, and design, offering a novel tool for content creation that bridges the gap between imagination and video production.
 
**Access and Development**: For now, OpenAI is granting access to Sora exclusively to a select group of red teamers and creative professionals for risk assessment and feedback. This strategic, limited rollout reflects OpenAI's commitment to refining Sora through practical application and ethical consideration.
 \> From \<[https://mail.google.com/mail/u/0/#inbox/FMfcgzGxRnVmFVgfbrbjmMFfNBrfGTTn](https://mail.google.com/mail/u/0/#inbox/FMfcgzGxRnVmFVgfbrbjmMFfNBrfGTTn)\>      
If you think OpenAI Sora is a creative toy like DALLE, ... think again. Sora is a data-driven physics engine. It is a simulation of many worlds, real or fantastical. The simulator learns intricate rendering, "intuitive" physics, and long-horizon consistency, all by some denoising and gradient maths.
 
I won't be surprised if Sora is trained on lots of synthetic data using Unreal Engine 5. It has to be!
 
Let's breakdown the following video. Prompt: "Photorealistic closeup video of two pirate ships battling each other as they sail inside a cup of coffee."
 
- The simulator instantiates two exquisite 3D assets: pirate ships with different decorations. Sora has to solve text-to-3D implicitly in its latent space.  
- The 3D objects are consistently animated as they sail and avoid each other's paths.  
- Fluid dynamics of the coffee, even the foams that form around the ships. Fluid simulation is an entire sub-field of computer graphics, which traditionally requires very complex algorithms and equations.  
- Photorealism, almost like rendering with raytracing.  
- The simulator takes into account the small size of the cup compared to oceans, and applies tilt-shift photography to give a "minuscule" vibe.  
- The semantics of the scene does not exist in the real world, but the engine still implements the correct physical rules that we expect.
 
Next up: add more modalities and conditioning, then we have a full data-driven UE that will replace all the hand-engineered graphics pipelines.
 \> From \<[https://www.linkedin.com/feed/update/urn:li:activity:7163976340042448896/](https://www.linkedin.com/feed/update/urn:li:activity:7163976340042448896/)\>      
Boilerplate commentary from LinkedIn
 
🤔 What makes [OpenAI](https://www.linkedin.com/company/openai/)'s [#Sora](https://www.linkedin.com/feed/hashtag/?keywords=sora&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7164083803634806784) so good at creating realistic videos? Here are the big research ideas behind the model architecture:
 
1. Turning Visual Data into Patches  
⛳ Inspired by the success of LLMs, Sora employs a similar approach by transforming visual data into patches. This method involves compressing videos into a lower-dimensional latent space (using a compression network) and then decomposing them into spacetime patches, which serve as the basic building blocks for the model.  
⛳This patch-based approach allows Sora to efficiently handle diverse types of videos and images in terms of duration, aspect ratio, and resolution. Sora leverages the transformer architecture, known for its effectiveness in various domains like language and image processing, adapted here for video generation.  
⛳It uses the popular diffusion approach where the model is trained to de-noise input patches based on conditioning information, such as text prompts. This enables the generation of high-quality videos from noisy inputs.
   

2. Training on Variable Durations, Resolutions, Aspect Ratios  
⛳Unlike traditional methods that may require standardizing video dimensions, Sora can handle native-sized data, offering benefits like improved composition, framing, and the ability to generate content for different devices at their native resolutions.  
⛳Beyond generating new content, Sora can edit existing videos or images, animate static images, and extend videos in time, creating seamless loops or transformations based on textual descriptions.  
⛳Sora exhibits emergent capabilities such as 3D consistency, long-range coherence, object permanence, and interaction simulations. These aspects indicate its potential as a simulator for various scenarios in the physical and digital worlds.
 
The below image shows an example of how space-time visual patches can be used to encode videos/images. Papers are linked below

![Image preview](Exported%20image%2020260222203213-0.jpeg)   
[https://openai.com/research/video-generation-models-as-world-simulators](https://openai.com/research/video-generation-models-as-world-simulators)