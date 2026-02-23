[CVPR24 Tutorial | Chelsea Finn: Humanoids and Robot Generalists](https://m.youtube.com/watch?v=0OaBpuU1-YQ&feature=youtu.be)
 
If you can teleoperate it, a robot can learn it ( surgery + ALOHA)  
Unclear if we can do this for whole-body control  
Can we scale data to train generalist policies?  
Humanoids  
Model-based control / or Sim2Real + RL  
Pose heavy; which requires a precision we don't do as humans  
Ego-EXO 4D - direct Human to Robot (doesn't work)  
HST - Human Shadowing Transformer (50 Hz)  
Instead, train a shadowing policy - AMASS dataset & retargeting  
+ Large Scale RL in Sim; reward some stability characteristics  
Adaptive policy architecture
 
If you can teleoperate it, a robot can learn it ( surgery + ALOHA)
 ![Exported image](Exported%20image%2020260222202612-0.png)  

HumanPlus: Shadowing
 ![Exported image](Exported%20image%2020260222202615-1.png)  
![Exported image](Exported%20image%2020260222202616-2.png)

Closed Loop is Essential
 ![Exported image](Exported%20image%2020260222202618-3.png)  

Can we scale data to train generalist policies?
   

RT2, RT2-X (55B Model) --\> match performance via OpenVLA (7B)  
LLAMA 2 7B, --- DinoV2, SigLIP (MLP Projector)  
970k robot demos curated from OpenX dataset  
64 A100, 15 days  
Much stronger on Zero shot  
Diffusion policy is strongest for narrow, single instruction tasks  
PEFT does not work; LoRA is
 ![Exported image](Exported%20image%2020260222202618-4.png)