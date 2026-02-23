[Yann LeCun](https://www.linkedin.com/in/yann-lecun/) tells PhD students that LLMs are an off ramp on the Road to AI..
 
See… [https://lnkd.in/gx36Jg-3](https://lnkd.in/gx36Jg-3)
 
And… [https://lnkd.in/egAnriGb](https://lnkd.in/egAnriGb)
 
Related… [https://lnkd.in/epCqaeyk](https://lnkd.in/epCqaeyk)
 
“For all the remarkable recent progress in AI research, we are still very far from creating machines that think and learn as well as people do. As Meta AI’s Chief AI Scientist Yann LeCun notes, a teenager who has never sat behind a steering wheel can learn to drive in about 20 hours, while the best autonomous driving systems today need millions or billions of pieces of labeled training data and millions of reinforcement learning trials in virtual environments. And even then, they fall short of human’s ability to drive a car reliably.”
 
LeCun proposes an architecture composed of six separate modules. Each is assumed to be differentiable, in that it can easily compute gradient estimates of some objective function with respect to its own input and propagate the gradient information to upstream modules.
 
1/ The configurator module performs executive control: Given a task to be executed, it preconfigures the perception module, the world model, the cost, and the actor for the task at hand, possibly by modulating the parameters of those modules.
 
2/ The perception module receives signals from sensors and estimates the current state of the world. For a given task, only a small subset of the perceived state of the world is relevant and useful. The configurator module primes the perception system to extract the relevant information from the percept for the task at hand.
 
3/ The world model module constitutes the most complex piece of the architecture. Its role is twofold: (1) to estimate missing information about the state of the world not provided by perception, and (2) to predict plausible future states of the world. The world model may predict natural evolutions of the world or predict future world states resulting from a sequence of actions proposed by the actor module. The world model is a kind of simulator of the part of the world relevant to the task at hand.
 
4/ The cost module computes a single scalar output that predicts the level of discomfort of the agent. It is composed of two submodules: the intrinsic cost, which is hard-wired and immutable (not trainable), and computes the immediate discomfort (such as damage to the agent, violation of hard-coded behavioral constraints, etc.), and the critic, which is a trainable module that predicts future values of the intrinsic cost.
 
5/ The actor module computes proposals for action sequences.
 
6/ The short-term memory module keeps track of the current and predicted world state, as well as associated costs.
 
******
 
What I would add to this model are an adjunct to module 5. Ie., a “Conscience/Ethical Alignment module”. And an “Embodiment/Self-awareness module. IMO important to add! 😜
 
For more on these added modules see comments…
 \> From \<[https://www.linkedin.com/feed/update/urn:li:activity:7202607204158300160/?updateEntityUrn=urn%3Ali%3Afs_updateV2%3A%28urn%3Ali%3Aactivity%3A7202607204158300160%2CFEED_DETAIL%2CEMPTY%2CDEFAULT%2Cfalse%29](https://www.linkedin.com/feed/update/urn:li:activity:7202607204158300160/?updateEntityUrn=urn%3Ali%3Afs_updateV2%3A%28urn%3Ali%3Aactivity%3A7202607204158300160%2CFEED_DETAIL%2CEMPTY%2CDEFAULT%2Cfalse%29)\>   
Can generative image models be good world models?  
This work from @Meta FAIR shows that there is a tradeoff between realism and diversity.  
The more realistic a generative model becomes, the less diverse it becomes.  
Realism comes at the cost of coverage.  
In other words, the most realistic systems are mode-collapsed.
 
My hunch, supported by a growing amount of empirical evidence, is that world models should *not* be generative.  
They should make predictions in representation space.  
In representation space, unpredictable or otherwise irrelevant information is absent.  
This is the main argument in favor of JEPA (Joint Embedding Predictive Architectures).
 
[https://lnkd.in/em4aVMP3](https://lnkd.in/em4aVMP3)