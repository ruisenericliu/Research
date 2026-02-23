Today, [Boston Dynamics](https://bostondynamics.com/) and the [Toyota Research Institute (TRI)](https://spectrum.ieee.org/toyota-research-future-of-robots) announced a new partnership “to accelerate the development of general-purpose [humanoid robots](https://spectrum.ieee.org/tag/humanoid-robots) utilizing TRI’s Large Behavior Models and [Boston Dynamics’ Atlas robot](https://spectrum.ieee.org/atlas-humanoid-robot).” Committing to working towards a general purpose robot may make this partnership sound like a every other commercial humanoid company right now, but that’s not at all that’s going on here: BD and TRI are talking about **fundamental** **robotics** **research, focusing on hard problems, and (most importantly) sharing the results.**
 
The broader context here is that Boston Dynamics has an exceptionally capable humanoid platform capable of advanced and occasionally painful-looking whole-body motion behaviors along with some relatively basic and brute force-y manipulation. Meanwhile, TRI has been working for quite a while on developing [AI-based learning techniques](https://medium.com/toyotaresearch/tris-robots-learn-new-skills-in-an-afternoon-here-s-how-2c30b1a8c573) to tackle a variety of complicated manipulation challenges. TRI is working toward what they’re calling [large behavior models (LBMs)](https://pressroom.toyota.com/toyota-research-institute-unveils-breakthrough-in-teaching-robots-new-behaviors/), which you can think of as analogous to [large language models](https://spectrum.ieee.org/tag/large-language-models) (LLMs), except for robots doing useful stuff in the physical world. The appeal of this partnership is pretty clear: Boston Dynamics gets new useful capabilities for Atlas, while TRI gets Atlas to explore new useful capabilities on.  
Here’s a bit more from [the press release](https://pressroom.toyota.com/boston-dynamics-and-toyota-research-institute-announce-partnership-to-advance-robotics-research/):
 
The project is designed to leverage the strengths and expertise of each partner equally. The physical capabilities of the new electric [Atlas robot](https://robotsguide.com/robots/atlas2016), coupled with the ability to programmatically command and teleoperate a broad range of whole-body bimanual manipulation behaviors, will allow research teams to deploy the robot across a range of tasks and collect data on its performance. This data will, in turn, be used to support the training of advanced LBMs, utilizing rigorous hardware and simulation evaluation to demonstrate that large, pre-trained models can enable the rapid acquisition of new robust, dexterous, whole-body skills.
 
The joint team will also conduct research to answer fundamental training questions for humanoid robots, the ability of research models to leverage whole-body sensing, and understanding human-robot interaction and safety/assurance cases to support these new capabilities.
 
For more details, we spoke with [Scott Kuindersma](https://www.linkedin.com/in/scott-kuindersma-06a38152/) (Senior Director of Robotics Research at Boston Dynamics) and [Russ Tedrake](https://www.linkedin.com/in/russ-tedrake-88648a4a/) (VP of Robotics Research at TRI).
 
**How did this partnership happen?**
 
**Russ Tedrake:** We have a ton of respect for the Boston Dynamics team and what they’ve done, not only in terms of the hardware, but also the controller on Atlas. They’ve been growing their [machine learning](https://spectrum.ieee.org/tag/machine-learning) effort as we’ve been working more and more on the machine learning side. On TRI’s side, we’re seeing the limits of what you can do in tabletop manipulation, and we want to explore beyond that.
 
**Scott Kuindersma:** The combination skills and tools that TRI brings the table with the existing platform capabilities we have at Boston Dynamics, in addition to the machine learning teams we’ve been building up for the last couple years, put us in a really great position to hit the ground running together and do some pretty amazing stuff with Atlas.
 
**What will your approach be to communicating your work, especially in the context of all the craziness around humanoids right now?**
 
**Tedrake:** There’s a ton of pressure right now to do something new and incredible every six months or so. In some ways, it’s healthy for the field to have that much energy and enthusiasm and ambition. But I also think that there are people in the field that are coming around to appreciate the slightly longer and deeper view of understanding what works and what doesn’t, so we do have to balance that.
 
The other thing that I’d say is that there’s so much hype out there. I _am_ incredibly excited about the promise of all this new capability; I just want to make sure that as we’re pushing the science forward, we’re being also honest and transparent about how well it’s working.
 
**Kuindersma:** It’s not lost on either of our organizations that this is maybe one of the most exciting points in the history of robotics, but there’s still a tremendous amount of work to do.
 
**What are some of the challenges that your partnership will be uniquely capable of solving?**
 
**Kuindersma:** One of the things that we’re both really excited about is the scope of behaviors that are possible with humanoids—a [humanoid robot](https://spectrum.ieee.org/tag/humanoid-robot) is much more than a pair of grippers on a mobile base. I think the opportunity to explore the full behavioral capability space of humanoids is probably something that we’re uniquely positioned to do right now because of the historical work that we’ve done at Boston Dynamics. Atlas is a very physically capable robot—the most capable humanoid we’ve ever built. And the platform software that we have allows for things like data collection for whole body manipulation to be about as easy as it is anywhere in the world.
 
**Tedrake:** In my mind, we really have opened up a brand new science—there’s a new set of basic questions that need answering. Robotics has come into this era of big science where it takes a big team and a big budget and strong collaborators to basically build the massive data sets and train the models to be in a position to ask these fundamental questions.
 
**Fundamental questions like what?**
 
**Tedrake:** Nobody has the beginnings of an idea of what the right training mixture is for humanoids. Like, we want to do pre-training with language, that’s way better, but how early do we introduce vision? How early do we introduce actions? Nobody knows. What’s the right curriculum of tasks? Do we want some easy tasks where we get greater than zero performance right out of the box? Probably. Do we also want some really complicated tasks? Probably. We want to be just in the home? Just in the factory? What’s the right mixture? Do we want backflips? I don’t know. We have to figure it out.
 
There are more questions too, like whether we have enough data on the Internet to train robots, and how we could mix and transfer capabilities from Internet data sets into robotics. Is robot data fundamentally different than other data? Should we expect the same scaling laws? Should we expect the same long-term capabilities?  
The other big one that you’ll hear the experts talk about is evaluation, which is a major bottleneck. If you look at some of these papers that show incredible results, the statistical strength of their results section is very weak and consequently we’re making a lot of claims about things that we don’t really have a lot of basis for. It will take a lot of engineering work to carefully build up empirical strength in our results. I think evaluation doesn’t get enough attention.
 
**What has changed in robotics research in the last year or so that you think has enabled the kind of progress that you’re hoping to achieve?**
 
**Kuindersma:** From my perspective, there are two high-level things that have changed how I’ve thought about work in this space. One is the convergence of the field around repeatable processes for training manipulation skills through demonstrations. The pioneering work of diffusion policy ([which TRI was a big part of](https://medium.com/toyotaresearch/tris-robots-learn-new-skills-in-an-afternoon-here-s-how-2c30b1a8c573)) is a really powerful thing—it takes the process of generating manipulation skills that previously were basically unfathomable, and turned it into something where you just collect a bunch of data, you train it on an architecture that’s more or less stable at this point, and you get a result.
 
The second thing is everything that’s happened in robotics-adjacent areas of AI showing that data scale and diversity are really the keys to generalizable behavior. We expect that to also be true for robotics. And so taking these two things together, it makes the path really clear, but I still think there are a ton of open research challenges and questions that we need to answer.
 
**Do you think that simulation is an effective way of scaling data for robotics?**
 
**Tedrake:** I think generally people underestimate simulation. The work we’ve been doing has made me very optimistic about the capabilities of simulation as long as you use it wisely. Focusing on a specific robot doing a specific task is asking the wrong question; you need to get the distribution of tasks and performance in simulation to be predictive of the distribution of tasks and performance in the real world. There are some things that are still hard to simulate well, but even when it comes to frictional contact and stuff like that, I think we’re getting pretty good at this point.
 
**Is there a commercial future for this partnership that you’re able to talk about?**
 
**Kuindersma:** For Boston Dynamics, clearly we think there’s long-term commercial value in this work, and that’s one of the main reasons why we want to invest in it. But the purpose of this collaboration is really about fundamental research—making sure that we do the work, advance the science, and do it in a rigorous enough way so that we actually understand and trust the results and we can communicate that out to the world. So yes, we see tremendous value in this commercially. Yes, we are commercializing Atlas, but this project is really about fundamental research.
 
**What happens next?**
 
**Tedrake:** There are questions at the intersection of things that BD has done and things that TRI has done that we need to do together to start, and that’ll get things going. And then we have big ambitions—getting a generalist capability that we’re calling LBM (large behavior models) running on Atlas is the goal. In the first year we’re trying to focus on these fundamental questions, push boundaries, and write and publish papers.
 
I want people to be excited about watching for our results, and I want people to trust our results when they see them. For me, that’s the most important message for the robotics community: Through this partnership we’re trying to take a longer view that balances our extreme optimism with being critical in our approach.
 \> From \<[https://spectrum.ieee.org/boston-dynamics-toyota-research](https://spectrum.ieee.org/boston-dynamics-toyota-research)\>  

Tighter integration between LBM and specific hardware

Tabletop manipulation has reached its limits

Need humanoids experience

Diffusion for humanoids?

What stage to insert language, vision, and actions?
 
What set of tasks to handle?
 
How much data from VLMs is transferrable?
 
Do we have scaling laws?
 
How do we evaluate empirically?
   

Fundamental shifts:
 
1. Convergence around repeatability from LfD
2. Data scale and diversity from GenAI is probably true in robotics

Simulation optimism
   

This is about fundamental research; rigorous scientific advancement

First year benchmark is getting LBM for a humanoid on ATLAS