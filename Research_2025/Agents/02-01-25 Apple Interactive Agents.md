Excited to share our latest preprint on training interactive AI agents with RL!
 
We train a digital agent that solves diverse day-to-day tasks from the AppWorld benchmark by interacting with a stateful environment using API calls. The AppWorld environment contains nine simulated apps (phone, email, payments, notes, etc.) with a total of 457 APIs.
 
Here’s an example task:  
"I paid for our last month's cable bill. Its amount is supposed to be shared equally among my roommates and me. Make Venmo requests to my roommates, with a description note, 'I paid for cable bill.'. The bill receipt is in my file system."
 
AppWorld is hard! Solving a single task involves chains of information-gathering and state-changing actions (sending messages, deleting files), as well as replanning in response to newly gathered information. The previous best open-weight agent (Llama 3) reached only a 24% success rate (test-normal). Our approach (LOOP) achieves a 70% success rate, outperforming even OpenAI o1 by 9 points.
 
We train our agent with reinforcement learning (RL), allowing the agent to discover solutions on its own. One of the most exciting findings is how effective LLMs are at exploration. Even toward the end of training, the agent rarely repeats the same solution, producing trajectories with unique API call sequences, e.g. for a single task we found 96 out of 100 call sequences were unique. This exploratory capacity enables RL agents to learn new behaviors even when training scenarios are relatively few.
 
Shout out to my wonderful collaborators: Marco Cusumano-Towner, Brody Huval, Aleksei Petrenko, Jackson Hamburger, Vladlen Koltun, Philipp Krähenbühl
 
Check out the paper for more details.  
arXiv: [https://lnkd.in/grYEMAQ4](https://lnkd.in/grYEMAQ4)  
Twitter: [https://lnkd.in/gfYZvs7H](https://lnkd.in/gfYZvs7H)  
AppWorld: [https://appworld.dev/](https://appworld.dev/)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>