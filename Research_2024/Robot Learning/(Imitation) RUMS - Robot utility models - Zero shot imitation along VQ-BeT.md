We just released Robot Utility Models (RUMs). RUMs enable basic tasks – door opening, drawer opening, object reorientation, etc. – at ~90% accuracy without ANY finetuning (i.e. zero-shot) in unseen new environments.
 
We think this is super exciting, why?
 
1. Unlocks many practical home utility tasks that often involve these basic tasks as part of an action chain. “Go get me a fork” involves opening the kitchen door and then opening the cutlery drawer.  
2. This works well **zero-shot in unseen and new** environments, which is practically a huge deal. Turn the robot on, and get going.  
3. The recipe for building a new model is fairly generic, and we think with a bit more refinement this can be a general recipe to build many more Utility models.
 
As always, our code, data, and models are fully open.  
🔗 [https://lnkd.in/eQMTfaWc](https://lnkd.in/eQMTfaWc)  
💻 [https://lnkd.in/eagTCVWV](https://lnkd.in/eagTCVWV)  
📄 [https://lnkd.in/em4qKm4k](https://lnkd.in/em4qKm4k)
 
And here are more details on our work:
 
RUMs are imitation-learned single-task policies that we can run zero-shot in new envs, made with a simple recipe:  
1. Collect diverse data (40 env x 25 demos = 1000)  
2. Train a multi-modal VQ-BeT/DP model  
3. Deploy in new env with mLLM feedback (retry if GPT says you failed)
 
It's a straightforward recipe, so we made five models: door & drawer opening, object reorientation, tissue & bag pickup. We ran 2950 real world rollouts to understand what's making this simple recipe work.
 
The secret sauce is simple: train on HIGH-QUALITY but DIVERSE data.
 
Diverse means 40 env x 25 demos is much better than 5 env x 200 demos, depending on the task we see a 50% drop!  
High quality means only use data you can train good policies on. Contrary to common belief, co-training can hurt instead of helping based on task & data quality.
 
To get here, we made a new data collection tool, mixing Dobb·E's iPhone stick with UMI's handheld size. This means it's super flexible, and you start collecting data in seconds w/ 0 calibration. We also made wrists for arms like XArm, so you can run RUMs on your lab robot!
 
Once you have good data, we see that your choice of algorithm matters little. Diffusion policy works slightly better at smaller dataset size, but VQ-BeT scales much better with data and overtakes at around 900-1200 demos. (But the err bars are overlapping, so take your pick)
 
The final piece that takes the avg success from 74.4% to 90% is... GPT. Take images from the robot camera, give it to GPT-4o, and ask if we completed the task successfully. If GPT says no, reset and retry.  
Such a simple scheme makes our policies succeed in avg 1.31 tries
 
~5500 robot demos and 3000 robot rollouts + home evals is a lot of labor!  
This work was lead by [Haritheja Etukuru](https://www.linkedin.com/in/haritheja/) and [Mahi Shafiullah](https://www.linkedin.com/in/nshafiul/) with lots of work by Nori Naka, [Zijin Hu](https://www.linkedin.com/in/zijin-hu-3100661ab/) [Seungjae Lee](https://www.linkedin.com/in/sjlee11/) support from [Hello Robot Inc](https://www.linkedin.com/company/hello-robot-inc/) [Chris Paxton](https://www.linkedin.com/in/chris-paxton-41aba958/) [Soumith Chintala](https://www.linkedin.com/in/soumith/) & [Lerrel Pinto](https://www.linkedin.com/in/lerrel/) !
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>  

[https://arxiv.org/pdf/2409.05865](https://arxiv.org/pdf/2409.05865)
 
What is the MLP-BC architecture they talk about in here? Some non generative model behaviour cloning model? There is no reference or citation for it so I'm a bit confused.  
If it is non generative I am very surprised that it performs similar to ACT
 
olivier_sigaud — Yesterday at 2:34 AM  
That's most probably just training a multi-layer perceptron (MLP) with behavioral cloning (BC). The most naive thing one can do.
 
2
 
@retoc  
[https://arxiv.org/pdf/2409.05865](https://arxiv.org/pdf/2409.05865) What is the MLP-BC architecture they talk about in here? Some non generative model behaviour cloning model? There is no reference or citation for it so I'm a bit confused. If it is non generative I am very surprised that it performs similar to ACT
 
Alexander Soare — Yesterday at 2:46 AM  
Lots of people report that ACT without the VAE objective performs just as well as with for many tasks. Does that make you less surprised?
 
@Alexander Soare  
Lots of people report that ACT without the VAE objective performs just as well as with for many tasks. Does that make you less surprised?
 
retoc — Yesterday at 2:50 AM  
Does this mean dropping the VAE encoder and using just a transformer for next action prediction? My perplexity would then be that using a simple MLP can yield results comparable to transformer based models.
 
@retoc  
Does this mean dropping the VAE encoder and using just a transformer for next action prediction? My perplexity would then be that using a simple MLP can yield results comparable to transformer based models.
 
Alexander Soare — Yesterday at 2:52 AM  
Does this mean dropping the VAE encoder and using just a transformer for next action prediction?  
Yep
 
My perplexity would then be that using a simple MLP can yield results comparable to transformer based models.  
I have two ideas to bounce off this one:  
Are the tasks / observations spaces difficult? If not, maybe an MLP will do?  
Do the observations get encoded with strong backbone architectures prior to going to the MLP? If so, maybe that's where the heavy lifting is.
 
retoc — Yesterday at 2:54 AM  
As for the visual encoder they use ResNet34 so not too much of heavy lifting. Tasks are not super complex though: door opening, objects rotations and similar and they use the halllo robot stick so actions and observations are a bit easier compared to 6dof arms I guess
 
@Alexander Soare  
Lots of people report that ACT without the VAE objective performs just as well as with for many tasks. Does that make you less surprised?
 
retoc — Yesterday at 2:54 AM  
Thanks for the insights, always exciting to learn new stuff
 
1
 
@retoc  
[https://arxiv.org/pdf/2409.05865](https://arxiv.org/pdf/2409.05865) What is the MLP-BC architecture they talk about in here? Some non generative model behaviour cloning model? There is no reference or citation for it so I'm a bit confused. If it is non generative I am very surprised that it performs similar to ACT
 
Mahi Shafiullah (NYU) — Yesterday at 11:32 AM  
Author here!
 
As @asoare mentioned above, the commonly used ACT these days (one without the VAE) is not a generative model, even though it uses a transformer. There's also a question of how well it scales to very large datasets, for example Aloha Unleashed by the same authors ([https://openreview.net/pdf?id=gvdXE7ikHI](https://openreview.net/pdf?id=gvdXE7ikHI)) is using a version of diffusion policy.  
One of our running hypothesis is that if you have good data, other parts matter much less. If that is true, it might be that ACT is generally spending a lot of its representational powers ironing out weird manifolds in the data. However, this is still a hypothesis, and we would love to do more experiments to confirm/deny this.
 
2  
[11:33 AM]  
But yes Olivier is correct, MLP-BC is ResNet34 + multi layer perceptrion trained with BC loss, it's the same architecture we used for Dobb-E [https://dobb-e.com/](https://dobb-e.com/)