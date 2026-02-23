Armbench dataset
 
[http://armbench.s3-website-us-east-1.amazonaws.com/](http://armbench.s3-website-us-east-1.amazonaws.com/) (Object Segmentation, Object Identification, Defect Detection)
 
With metadata for pick and place results
 
Vacuum based end effector
 
“The benchmark dataset for this task contains 235K+ labeled pick activities corresponding to 190K+ unique objects. Each pick activity comprises one query image from the pick scene and up to three query images from the transfer phase.”(Mitash et al., 2023, p. 4)
 
Demonstrating Large-Scale Package Manipulation via Learned Metrics of Pick Succes  
[https://arxiv.org/abs/2305.10272](https://arxiv.org/abs/2305.10272)
 
This paper is on ranking pick options sequentially, memoryless (pick based on now)
 
SEGMENT AN OBJECT AND GET THE MAX LIKELIHOOD PICK
 
RANK SEGMENTED OBJECTS BASED ON PICK PROBABILITY
   

“Specifically, the system was trained on over 394K picks. It is used for singulating up to 5 million packages per day and has manipulated over 200 million packages during this paper’s evaluation period.”(Li et al., 2023, p. 1)
   

“It is a shallow machine learning model, which allows us to evaluate which features are most important for the prediction”(Li et al., 2023, p. 1)
 
An online pick ranker leverages the learned success predictor to prioritize the most promising picks for the robotic arm, which are then assessed for collision avoidance
 
“The segmentation module is a deep network based on Mask Scoring R-CNN [6] with a Swin-T backbone [8] for predicting the package material, instance segmentation masks, and the classification and segmentation scores.”(Li et al., 2023, p. 4)
 
Remainder is from point cloud data - selected features:

1. Package height
2. Quality of plan fitting
3. Number of activated suction cups
4. Alignment quality between suction cups and package surface
 
Then make an adjacency graph
 
Trade off on exploration vs exploitation in pick selection behavior