What if robots could dream inside a video generative model? Introducing DreamGen, a new engine that scales up robot learning not with fleets of human operators, but with digital dreams in pixels. DreamGen produces massive volumes of neural trajectories - photorealistic robot videos paired with motor action labels - and unlocks strong generalization to new nouns, verbs, and environments. Whether you’re a humanoid (GR1), an industrial arm (Franka), or a cute little robot (HuggingFace SO-100), DreamGen enables you to dream.
 
Video generation models like Sora & Veo are neural physics engines. By compressing billions of internet videos, they learn a multiverse of plausible futures, i.e. superpositions of how the world could unfold from any initial image frame. DreamGen taps into this power with a simple 4-step recipe:
 
1. Fine-tune a SOTA video model on your target robot;  
2. Prompt the model with diverse language prompts to simulate parallel worlds: how your robot would have acted in new scenarios. Filter out the bad dreams (ha!) that don’t follow instructions;  
3. Recover pseudo-actions using inverse dynamics or latent action models;  
4. Train robot foundation models on the massively augmented dataset of neural trajectories.
 
That’s it. Just more data, and plain old supervised learning. Simple, right?
 
What’s remarkable is how far this goes. Starting with just a single-task dataset of pick-and-place, our humanoid robot learns 22 new behaviors, such as pouring, folding, scooping, ironing, and hammering, despite never seeing those verbs before. Better yet, we can take the robot out of the lab and drop it into the NVIDIA HQ Cafe, and let DreamGen work its magic. We show true zero-to-one generalization: from 0% success to over 43% for novel verbs, and 0 -\> 28% in unseen environments.
 
Compared to a traditional graphics engine, DreamGen doesn’t care if the scene involves deformable objects, fluids, translucent materials, contact-rich interactions, or crazy lighting. Good luck engineering those by hand. For DreamGen, every world is just a forward pass through a diffusion neural net. No matter how complex the dream is, it takes constant compute time to roll out.
 
Read our blog and paper today!  
Project website with lots of dreamy videos: [https://lnkd.in/g4B5-NgT](https://lnkd.in/g4B5-NgT)  
Paper: [https://lnkd.in/gp4rmhae](https://lnkd.in/gp4rmhae)  
DreamGen is featured in Jensen's Computex Keynote as the new GR00T Dreams workflow: [https://lnkd.in/gkKT8i_V](https://lnkd.in/gkKT8i_V)  
We plan to fully open-source the entire pipeline in the next few weeks. Stay tuned!