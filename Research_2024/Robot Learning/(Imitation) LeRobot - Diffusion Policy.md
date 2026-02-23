Visuomotor Policy Learning via Action Diffusion (published March 7, 2023)
 
Cheng Chi, Siyuang Feng, Yilun Du, Zhenjia Xu, Eric Cousineau, Benjamin Burchfiel, Shuran Song (moved to Stanford)
 
Columbia, TRI, MIT
 
Backstory:
 
Each task is task specific; behavior cloning is still task specific, especially for deformable object manipulation
 
Human demonstration is the way - widespread belief in bitter lesson of AI
 
But, Implicit Behavior Cloning (Pete Florence, Robotics @ Google) --\> when we tried out this result, have a lot of difficulty reproducing on specific hardware; stochastic results. However, the idea of energy based models to represent discrete behaviors stuck. Then we looked at stable diffusion, and cross pollinated. Somehow, we backtrack back into the manifold.
 ![Exported image](Exported%20image%2020260222202931-0.png)  

Same both correct and incorrect actions - trying to reduce energy for positive actions, and increase for everything else - need increasing samples for normalizing constant. However, Z(0, \theta) should go to zero
 ![Exported image](Exported%20image%2020260222202932-1.png)  

Then found:
 ![Exported image](Exported%20image%2020260222202934-2.png)  

Then decided to do this paper together with Yilun
 ![Exported image](Exported%20image%2020260222202936-3.png)  

But it worked fairly well - let's do a systematic evaluation, which lead to scalable code
   

TRI added to their book in a week
 ![Exported image](Exported%20image%2020260222202941-4.png)  

Concurrent works:  
Imitation Human Behaviour with Diffusion Models - Microsoft Research  
Goal-Conditioned Imitation Learning using Score Based Diffusion Policies - KIT, Germany
 
**Difference: predicting sequence instead of actions is really really important (still don't know why)**
 
**Whether it uses a diffusion model is not that important - it's better to use a multi-modal approach to generation**  
**Next generative approach post diffusion will also probably do better for action space**  
**Another intuition - slowing down execution is better for performance (still don't know why)**
 
**Even if the policy is slow, you can predict a sequence and drop the sequence in to keep the robot running**  
**Intuition on step size/ sequence length --\> Humans have 300 ms reaction time- each action chunk should be around the same order of magnitude - quarter to half a sec.**
 
**Future Directions:**

1. ACT came out - Where does diffusion shine and when does ACT shine
    1. Answer: these are very similar methods
    2. Diffusion vs VAE for generating action
    3. ACT converts faster when collected by 1 person -- Diffusion may do better when the data collection comes from multiple people
        1. Same is true for image generation - diffusion images are crisp, VAE generation is more blurry
2. Data
    1. Conclusions we draw may be overfit for the data we have
    2. Focusing on data rather than new methods
3. Training from scratch was better than finetuning originally, but probably because weights were frozen
    1. Use ViT-Owl
4. TRI trying mixed data - language label or one-hot encoding - which task is it doing now?
5. What about planners?
6. Add randomization to training to deal with colors 
Per-ACT - can be understood as doing categorical distributions  
However, may require too much memory - however, discretization of grid results in aliasing problem when re-sampling  
Any time action space is greater than 3, probably want to use generative approaches
 
Actual slides:
 
All visuomotor policies - POINT: even simple policies can work pretty well
 ![Exported image](Exported%20image%2020260222202945-5.png)   
What is diffusion policy? --\> sequence of action generations from an image
 ![Exported image](Exported%20image%2020260222202946-6.png)   
Repeats at 2 Hz - can run for 20hz, but should run slower (reducing the speed of the policy makes performance better)  
Predicting the same amount of steps each time - but inference time dictates how many steps are open loop
   

(160 demonstrations for T example)
 ![Exported image](Exported%20image%2020260222202948-7.png)  

Gains - 1 : can represent multiple actions from same policy;
 
Input: Vision encoder + concat with pose values  
Output: Action space is relative end-effector space. Can also use relative pose. Haven't used joint space.  
No global reference really - eye moves as hand moves (consider 3 year old paper - grasp in the wild - but too many engineering details, UMI needs fish eye camera; SLAM accuracy, etc )  
Policy intuitively feels out of distribution when there's jittering between items
 
Neural networks represent functions; Diffusion represents bimodal representations ; diverts aggregation/averaging issue from positive behaviors.
 ![Exported image](Exported%20image%2020260222202955-8.png)   
Difficult to optimize mixture of gaussian models

![Exported image](Exported%20image%2020260222202957-9.png)   ![Exported image](Exported%20image%2020260222202958-10.png)  
![Exported image](Exported%20image%2020260222203002-11.png)  
![Exported image](Exported%20image%2020260222203004-12.png)  
![Exported image](Exported%20image%2020260222203004-13.png)  
![Exported image](Exported%20image%2020260222203005-14.png)  
![Exported image](Exported%20image%2020260222203006-15.png)  
![Exported image](Exported%20image%2020260222203007-16.png)