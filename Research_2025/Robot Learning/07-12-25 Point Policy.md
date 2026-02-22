Point Policy:
 
The robot behaviors shown below are trained without any teleop, sim2real, genai, or motion planning. Simply show the robot a few examples of doing the task yourself, and our new method, called Point Policy spits out a robot-compatible policy!
 
Point Policy uses sparse key points to represent both human demonstrators and robots, bridging the morphology gap. The scene is hence encoded through semantically meaningful key points from minimal human annotations.
 
The overall algorithm is simple:  
1. Extract key points from human videos.  
2. Train a transformer policy to predict future robot key points.  
3. Convert predicted key points to robot actions.
 
This project was an almost solo effort from [Siddhant Haldar](https://www.linkedin.com/in/siddhant-haldar-2ba70a136/). And as always, this project is fully opensourced.  
Project page: [https://lnkd.in/e32RtQK9](https://lnkd.in/e32RtQK9)  
Paper: [https://lnkd.in/emQpENTy](https://lnkd.in/emQpENTy)