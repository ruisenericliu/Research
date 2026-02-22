obotics data is expensive and slow to collect.  
A lot of videos are available online, but not readily usable by robotics because of lack of action labels.
 
AMPLIFY solves this problem by learning Actionless Motion Priors that unlock better sample efficiency, generalization, and scaling for robot learning.
 
Our key insight is to factor the problem into two stages:  
The "what": Predict the visual dynamics required to accomplish a task  
The "how": Map predicted motions to low-level actions
 
This decoupling enables remarkable generalizability: our policy can perform tasks where we have NO action data, only videos. We outperform SOTA BC baselines on this by 27x 🤯
 
AMPLIFY is composed of three stages:  
1. Motion Tokenization: We track dense keypoint grids through videos and compress their trajectories into discrete motion tokens.  
2. Forward Dynamics: Given an image and task description (e.g., "open the box"), we autoregressively predict a sequence of motion tokens representing how keypoints should move over the next second or so. This model can train on ANY text-labeled video data - robot demonstrations, human videos, YouTube videos.  
3. Inverse Dynamics: We decode predicted motion tokens into robot actions. This module learns the robot-specific mapping from desired motions to actions. This part can train on ANY robot interaction data - not just expert demonstrations (think off-task data, play data, or even random actions).
 
So, does it actually work?  
Few-shot learning: Given just 2 action-annotated demos per task, AMPLIFY nearly doubles SOTA few-shot performance on LIBERO. This is possible because our Actionless Motion Priors provide a strong inductive bias that dramatically reduces the amount of robot data needed to train a policy.
 
Cross-embodiment learning: We train the forward dynamics model on both human and robot videos, but the inverse model sees only robot actions. Result: 1.4× average improvement on real-world tasks. Our system successfully transfers motion information from human demonstrations to robot execution.
 
And now my favorite result: AMPLIFY enables zero-shot task generalization. We train on LIBERO-90 tasks and evaluate on tasks where we’ve seen no actions, only pixels. While our best baseline achieves ~2% success, AMPLIFY reaches a 60% average success rate, outperforming SOTA behavior cloning baselines by 27x.
 
This is a new way to train VLAs for robotics which dont always start with large scale teleoperation.  
Instead of collecting millions of robot demonstrations, we just need to teach robots how to read the language of motion. Then, every video becomes training data.
 
led by Jeremy Collins & Loránd Cheng in collaboration with Kunal Aneja, Albert Wilcox, Benjamin Joffe at College of Computing at Georgia Tech
 
Check out our paper and project page for more details:
 
📄 Paper: [https://lnkd.in/eZif-mB7](https://lnkd.in/eZif-mB7)  
🌐 Website: [https://lnkd.in/ezXhzWGQ](https://lnkd.in/ezXhzWGQ)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>