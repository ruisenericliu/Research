Why do we needs 100-1000s of demos to train even simple robot tasks? The answer: Supervised Learning wastes rich observational information.
 
To fix this, we built DynaMo, a Self-Supervised method that operates on small in-domain data by exploiting the dynamics of temporal data. Instead of learning a denoising or contrastive objective on a bag of frames, we exploit the sequential and causal structure of the demonstration observations.
 
DynaMo jointly learns inverse dynamics to a latent action, and forward dynamics predicting the next frame embedding. It requires no augmentations, contrastive sampling, or ground truth actions.
 
We are releasing our open-source code, data, and videos here: [https://lnkd.in/e5TFR49w](https://lnkd.in/e5TFR49w) . Try it out!
 
This work is led by [Zichen Jeff Cui](https://www.linkedin.com/in/zichen-cui/) w/ [Hengkai Pan](https://www.linkedin.com/in/hengkaipan/), [Aadhithya Iyer](https://www.linkedin.com/in/aadhithya-iyer-147697176/) and [Siddhant Haldar](https://www.linkedin.com/in/siddhant-haldar-2ba70a136/).
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>