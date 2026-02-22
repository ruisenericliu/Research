Cornell: Track Any State:  
👉Discussion [https://lnkd.in/dMgakzWm](https://lnkd.in/dMgakzWm)  
👉Paper [https://lnkd.in/d4pA3bXJ](https://lnkd.in/d4pA3bXJ)  
👉Project [https://lnkd.in/dgbNfCuj](https://lnkd.in/dgbNfCuj)  
👉Repo [https://lnkd.in/dtVWq2z7](https://lnkd.in/dtVWq2z7)
    
Graph EQA: [https://saumyasaxena.github.io/grapheqa/](https://saumyasaxena.github.io/grapheqa/)  
Evaluate: Prsmatic VLMS: [https://arxiv.org/abs/2402.07865](https://arxiv.org/abs/2402.07865)
   

D-Fine: [https://github.com/Peterande/D-FINE](https://github.com/Peterande/D-FINE)  
- Inference: [https://lnkd.in/d3HfXGUQ](https://lnkd.in/d3HfXGUQ)  
- Fine-tuning on a custom dataset: [https://lnkd.in/dje4V8DG](https://lnkd.in/dje4V8DG)
   

Pro-tracker: [https://michaelszj.github.io/protracker/](https://michaelszj.github.io/protracker/)
 
Megasam: [https://mega-sam.github.io/](https://mega-sam.github.io/)
 
Another week, another impressive openly available model by Meta. This time, the Hugging Face team collaborated with the authors of CoTracker3, a Transformer-based model for point tracking across a video.
 
The model works as follows: given a video, sample a grid of points on top of it (indicated by different colours). Next, the model can track each of those points across a video consistently. It even works when points you want to track are occluded (for instance, when a tree is in front of a cyclist you're tracking). The model can track up to 70k points on a single GPU.
 
The authors employ a clever formulation of the problem to leverage a Transformer architecture, and use semi-supervised learning to scale up the dataset on which the model is trained. The idea is to simply collect a lot of unlabeled videos, employ a pre-trained model (so-called "teacher") to label those, and finally train a model on the labeled dataset.
 
This was a nice collaboration with Nikita Karaev and team at Meta.
 
Resources:  
- project page: [https://lnkd.in/eqWuDXWq](https://lnkd.in/eqWuDXWq)  
- paper (with linked model and demo): [https://lnkd.in/eHFBZVxW](https://lnkd.in/eHFBZVxW)  
- good intro regarding its applications: [https://lnkd.in/endQ6Gwj](https://lnkd.in/endQ6Gwj)
   

We’re excited to share Cubify Anything, redefining the boundaries of data and modeling in 3D object detection.
 
Following the release of [hashtag#ARKitScenes](https://www.linkedin.com/feed/hashtag/?keywords=arkitscenes&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7271294037691658241) and Apple’s first 3D Object Detection model in [hashtag#RoomPlan](https://www.linkedin.com/feed/hashtag/?keywords=roomplan&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7271294037691658241) two years ago, Cubify Anything takes things to the next level.
 
Introducing Cubify Anything 1M (CA-1M), a dataset that sets new standards in diversity, scale, and accuracy with 400K+ 3D objects, 1K+ laser-scanned scenes, and 3.5K handheld egocentric captures, providing near-perfect alignment and unmatched richness.
 
Complementing this is Cubify Transformer (CuTR), a fully Transformer-based 3D object detection model that predicts 3D boxes directly from 2D features derived from RGB inputs. CuTR not only surpasses traditional point-based methods but also demonstrates superior performance in handling noise, uncertainty, and RGB(D) only scenarios.
 
Together, CA-1M and CuTR challenge conventional 3D modeling, proving that data-rich approaches unlock possibilities beyond traditional 3D biases. This marks a transformative step toward building models that can truly Cubify Anything.
 
arXiv: [https://lnkd.in/gtk3QaK9](https://lnkd.in/gtk3QaK9)  
Dataset and Models: Coming Soon
 
This is a great work by [Justin Lazarow](https://www.linkedin.com/in/justin-lazarow-919b784a/) and [David Griffiths](https://www.linkedin.com/in/davidngriffiths/) in collaboration with [Gefen Kohavi](https://www.linkedin.com/in/gefenkohavi/) and [Francisco Crespo](https://www.linkedin.com/in/f-crespo-dev/)
    
Learning Spatial-Semantic Features for Robust Video Object Segmentation
 
nanoSAM and nanoOWL both out
 
SAM2 [https://ai.meta.com/blog/segment-anything-2/?utm_source=linkedin&utm_medium=organic_social&utm_content=reel&utm_campaign=sam2](https://ai.meta.com/blog/segment-anything-2/?utm_source=linkedin&utm_medium=organic_social&utm_content=reel&utm_campaign=sam2)  
With memory over videos  
44 FPS, Occlusion head, Memory Bank  
[https://huggingface.co/collections/merve/sam2-66ac9deac6fca3bc5482fe30](https://huggingface.co/collections/merve/sam2-66ac9deac6fca3bc5482fe30)
 
[https://arxiv.org/pdf/2407.06984](https://arxiv.org/pdf/2407.06984)  
Coders
 
Demystifying CLIP  
[https://arxiv.org/abs/2309.16671](https://arxiv.org/abs/2309.16671)  
[https://paperswithcode.com/dataset/laion-400m](https://paperswithcode.com/dataset/laion-400m)
 
Rt-detr: [https://debuggercafe.com/rt-detr/](https://debuggercafe.com/rt-detr/)
 
DiffusionMOT: [https://diffmot.github.io/](https://diffmot.github.io/)
 
Radsplat: [https://arxiv.org/abs/2403.13806](https://arxiv.org/abs/2403.13806)
 
Yolo V10: [https://arxiv.org/pdf/2405.14458](https://arxiv.org/pdf/2405.14458)  
[https://medium.com/@hashiimkalam/is-yolo-v10-the-best-one-so-far-891065e692b8](https://medium.com/@hashiimkalam/is-yolo-v10-the-best-one-so-far-891065e692b8)
 
Object Reconstruction: [https://arxiv.org/pdf/2405.05858](https://arxiv.org/pdf/2405.05858)
 
Dynamic 3d Gaussians  
Representations: [https://arxiv.org/abs/2405.07987](https://arxiv.org/abs/2405.07987)
 
FEAT UP: [https://arxiv.org/abs/2403.10516](https://arxiv.org/abs/2403.10516)
 
BootsTAP: - Tracking Any point: [https://arxiv.org/pdf/2402.00847](https://arxiv.org/pdf/2402.00847)