[https://www.physicalintelligence.company/blog/pi0](https://www.physicalintelligence.company/blog/pi0)
 
[https://www.physicalintelligence.company/download/pi0.pdf](https://www.physicalintelligence.company/download/pi0.pdf)
   

Some quick notes from the Physical Intelligence Pi0 paper:  
They split the model in two experts  
a VLM expert that processes language and images to an intermediate representation (embeddings)  
a smaller action expert that uses the robot state + action tokens + noise (similar to diffusion) and the VLM outputs to predict a chunk of actions (inspired by ACT and the BID paper)  
vision transformers as image encoders rather than resnets (not sure how much it matters)  
They start with a pre-trained VLM (not sure if it's frozen or if they modify the weights during training), and their pre-training process uses Open-X and proprietary data (looks like most of the prop data is from a bimanual ARX robot, same as my setup that will be supported by lerobot )  
Besides pre-training they have a special post-training stage where they fine-tune the policy using "highly curated" expert demonstrations, as well as mistake recovery episodes. Not much is said about this, so I think this curation of your best data might be the most important step