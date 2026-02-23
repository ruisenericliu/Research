[https://eureka-research.github.io/](https://eureka-research.github.io/)
 
If you look at Eureka from Nvidia:  It doesn't actually change the RL algorithm
 
it just says:  - Eureka achieves human-level reward design by in-context **evolving** reward functions More specifically, Eureka first takes unmodified environment source code and language task description as context to zero-shot generate executable reward functions from a coding LLM.
 
which then it's like, if the LLM can generate the entirety of the code AND specify the reward value, then interesting  
but if you've written the code and then are just editing the reward value
 
is it that interesting to do the following:
 
"LLM (GPT-4) to flexibly improve the reward functions with many distinct types of free-form, targeted modification, such as (1) changing the hyperparameter of existing reward components, (2) changing the functional form of existing reward components, and (3) introducing new reward components"
 
and that's it.
 
That ends the technical discussion of the github.io - it goes straight to experiments after
 
So: if the reward value an LLM can intuit is "better than human" the question is really why - or rather, does it just have the flexibility to iterate in simulation and try and try again