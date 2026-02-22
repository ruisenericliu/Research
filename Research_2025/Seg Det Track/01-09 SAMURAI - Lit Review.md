Excited to share our latest work on Visual Object Tracking:  
🌊 SAMURAI: Adapting Segment Anything Model for Zero-Shot Visual Tracking with Motion-Aware Memory
 
The Segment Anything Model 2 (SAM 2) has set a high bar for object segmentation, but visual object tracking in challenging scenarios remains a hurdle. That’s where SAMURAI comes in. By integrating the motion cues with a motion-aware memory selection mechanism, SAMURAI tackles issues like crowded scenes, fast motion, and self-occlusion without computational overhead!
 
💡 Key Highlights:  
- Zero-shot Generalization: No fine-tuning or retraining required, we use the exact identical models provided by SAM 2. SAMURAI can directly adapts to VOT tasks!  
- SoTA Performance: SAMURAI achieves state-of-the-art performance on various VOT benchmarks including GOT-10k, LaSOT-ext, and NeedForSpeed!
 
From dynamic environments to real-world applications, SAMURAI demonstrates precision, robustness, and efficiency, setting a new standard in visual object tracking.
 
🔗 Learn more:  
📄 Paper: [arXiv 2411.11922]( [https://lnkd.in/gHVmi6hS](https://lnkd.in/gHVmi6hS))  
🌐 Project: [SAMURAI Website]( [https://lnkd.in/gY3zjHke](https://lnkd.in/gY3zjHke))  
💻 Code: [GitHub Repository]( [https://lnkd.in/gXgQmZBp](https://lnkd.in/gXgQmZBp))
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>   
leveraging the history of object trajectories, we can enhance  
the model’s ability to differentiate between visually simi-  
lar objects and maintain tracking accuracy in the presence  
of occlusions. Additionally, optimizing SAM 2’s memory  
management is crucial. The current approach [14, 35] of in-  
discriminately storing recent frames in the memory bank in-  
troduces irrelevant features during occlusions, compromis-  
ing tracking performance
 
Our proposed method incorporates two key advancements: (1) a motion modeling  
system that refines the mask selection
 ![Exported image](Exported%20image%2020260222122734-0.png)  

We then select the mask that maximizes a  
weighted sum of the KF-IoU score and the original affinity  
score:
   

(2) an optimized memory selection mechanism that leverages a hybrid scoring system, combining the original mask  
affinity, object, and motion scores to retain more relevant historical information
   

To construct an effective memory bank of object cues considering motion, we employ a selective approach for  
choosing frames from previous time steps based on three scoring:  
the mask affinity score,  
object occurrence score,  
and motion score