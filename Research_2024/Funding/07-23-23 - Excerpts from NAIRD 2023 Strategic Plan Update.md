Let's target a white paper is to submit a novel research proposal for AI/Robotics development at LM that can sequentially scale with the business interests and needs of autonomy as aligned with national funding. My current hypothesis for an IRAD is that fundamental use cases at LM align with National Artificial Intelligence R&D (NAIRD) 2023 subcategories in Strategies **1 ( Pursuing Research on Scalable General-Purpose AI System; Developing More Capable and Reliable Robots)** and **2 (Developing the Science of Human-AI Teaming, Developing New Paradigms for AI Interactions and Collaboration).** While the majority of request for feedback responses target ethical, legal, and societal implications of AI (Strategy 3) or safety and security of AI systems (Strategy 4), it is likely not advantageous for us to pursue policy research or safe ML research in the short run.
   

Tying to long range funding: Currently (07/24) the System for Award Management (SAM) Lists the following active contract opportunities aligned with Strategies 1 and 2:
 
SAM List:

1. Artificial Intelligence Integration Center (AI2C) - Transformative Artificial Intelligence Research and Applications Broad Agency Announcement (BAA)
2. Program Announcement for Artificial Intelligence Exploration (AIE)
3. Next Generation Identification and Awareness Initiative
4. ROBUST AND EFFICIENT COMPUTING ARCHITECTURES, ALGORITHMS AND APPLICATIONS FOR EMBEDDED DEEP LEARNING
5. AI Reinforcements (AIR)
   

In terms of verbiage, there are a couple quotes to help with layman explanation if aims with Strategies 1 and 2:
 
1. On Foundational Models and Robotics - From Peter Abeel
    
    1. There is a trend of foundation models and a trend of generative AI. They are very intertwined, but they’re distinct. A foundation model is a model that is trained on a lot of data, including data that is only tangentially possibly related to what you care about. B
    2. Essentially, all generative models are foundation models, but there are foundation models that are not generative AI models, because they do something else. The Covariant Brain is a foundation model, the way it’s set up right now.
    3. It’s a shift in paradigm. Traditionally, people would have said, ‘Oh, if you’re going to do groceries, groceries, groceries, groceries. That’s all your training, a neural network based on groceries. That’s not what we’ve been doing. It’s all about chasing the long tail of edge cases. The more things you’ve seen, the better you can make sense of an edge case.
    4. In robotics, there are a few angles. One is building a deeper understanding of the world. Instead of me saying, “I’m going to label data to teach the neural network,” I can say, “I’m going to record a video of what happens,” and my generative model needs to predict the next frame, the next frame, the next frame. And by forcing it to understand how to predict the future, I’m forcing it to understand how the world works.
    5. You’re giving it two tasks and it learns how to do the one task, because the two tasks are related. Predicting the next frame is such a difficult thinking exercise, you force it to think through so much more to predict actions that it predicts actions much, much faster.
    6. But the idea is that there are different ways of teaching a robot. You can program it. You can give it demonstrations. It can learn from reinforcement, where it learns from its own trial and error. Programming has seen its limitations. It’s not really going beyond what we’ve seen for a long time in car factories
    7. One of the big challenges with robotics has been high-level reasoning. There are two challenges: 1. how do you do the actual motor skill and 2. what should you actually do. If someone asked you, ‘make me scrambled eggs,’ what does that even mean? And that’s where generative AI models come in handy in a different way. They’re pre-trained. The simplest version just uses language.
    8. The whole thing in robotics has traditionally been logic or task planning, and people who have to program it in somehow have to describe the world in terms of logical statements that somehow come after each other, and so forth. The language models kind of seem to take care of it in a beautiful way. That’s unexpected to many people.
    
    - We now have a tool that can handle language very well. And what’s cool about it is that it gives you access to the semantics of a scene. A very well known paper from Google did the following: You have a robot and you say “I just spilled something, and I need help to clean it up.” Typically the robot wouldn’t know what to do with that, but now you have language. You run that into ChatGPT and it generates: “get a sponge. Get a napkin. Get a cloth. Look for the spilled can, make sure it can pick that up.” All of that stuff can come out. What they do is exactly that: They take all of that output and they say, “is there a sponge around? Let me look for a sponge.”
    - The connection between semantic of the world – a spill and a sponge – ChatGPT is very good at that. That fills a gap that we’ve always had. It’s called the Open World Problem.
    - We have a project on that’s called Language Embedded Radiance Field. It’s brand new. It’s how to use that language to figure out where to pick things up. We say, “here’s a cup. Pick it up by the handle,” and it seems to be able to identify where the handle is. It’s really interesting.
      
    
2. From previous papers:
    1. Human-Robot Teaming: [https://bpb-us-w2.wpmucdn.com/sites.gatech.edu/dist/d/958/files/2021/07/T_HRI_Scheduling_Full-1.pdf](https://bpb-us-w2.wpmucdn.com/sites.gatech.edu/dist/d/958/files/2021/07/T_HRI_Scheduling_Full-1.pdf)
    2. Aerospace manufacturing: [https://arc.aiaa.org/doi/pdf/10.2514/6.2021-0270](https://arc.aiaa.org/doi/pdf/10.2514/6.2021-0270)
      
    

Ken Goldberg:
      

NAIRD Notes: Update date: May 2023
 
**Strategy 1: Make long-term investments in fundamental and responsible AI research.**

- Most AI R&D thus far has focused on the advancement of AI for individual tasks. Additional work is needed to solve increasingly difficult science and technology challenges covering multiple domains and applications, moving toward the vision of general-purpose AI. AI R&D increasingly attempts to consider how various areas of AI work can fit together into an integrated system.
- knowledge discovery, improving the abilities of AI to perceive and act, and developing scalable, general-purpose systems to work in real and virtual environments.
- **Subcategories:**
    - Knowledge Discovery;
        - Crosspollination with Strategy 5
    - Fostering Federated ML Approaches;
        - g allows multiple computers or devices to collaborate in building a shared global ML model based on the data that is locally stored on each device.
    - Understanding Theoretical Capabilities and Limitations of AI;
        - better understand how some AI techniques, especially generative AI , work and their emerging properties
    - Pursuing Research on Scalable General-Purpose AI Systems;
        - **emergence of so-called foundation models that are trained on large amounts of unlabeled data, usually using self-supervised learning,** and can be adapted to many application domains such as law, healthcare, and science
        - Further research is needed to enhance the validity and reliability as well as security and resilience of these large models, especially in response to adversarial attacks.
    - Developing AI Systems and Simulations Across Real and Virtual Environments;
        - A key requirement is that the physical system is instrumented so that the collected data is interactively shared with the digital or computational model of itself. The digital-twin approach enables smart automation of physical systems across real and virtual environments.
    - Enhancing the Perceptual Capabilities of AI Systems;
        - Better sensors
        - the perception of humans, including the states of their attention and emotion, must be greatly improved by using an appropriate combination of sensors and algorithms so that AI systems can work more effectively with people
    - **Developing More Capable and Reliable Robots;**
        - **One noteworthy development involves the introduction of AI-controlled robots into the research environment, yielding “autonomous laboratories” that can enable closed-loop synthesis characterization and testing systems** capable of designing new drugs, chemicals, advanced electronic materials, and countless other materials far faster and with greater variety and precision than previously possible .
        - Robotic technologies are now showing promise in their ability to complement, augment, enhance, or emulate human physical capabilities or human intelligence. However, scientists and engineers need to make these robotic systems more capable, reliable, easy-to use, and safe.
        - Progress is needed in cognition and reasoning to allow robots to better understand and interact with the physical world. **An improved ability to adapt and learn, building abstract representations of low-level physical tasks, will allow robots to generalize their skills**, self-assess their current performance, and learn a repertoire of physical movements from human teachers.
        - Robots need to learn to team together in a **seamless fashion and collaborate with humans in a way that is trustworthy and predictable.** Robotic systems must safely and cooperatively interact with humans and other actors in complex built and natural environments.
        - Research is also needed to deal with adversarial systems, or systems that operate in disguise to collect data or interfere with legitimate operations.
    - Advancing Hardware for Improved AI;
        - GPU improvements
    - Creating AI for Improved Hardware
        - Vice versa
    - Embracing Sustainable AI and Computing Systems.

**Strategy 2: Develop effective methods for human-AI collaboration.**

- Fully autonomous systems that involve little or no human interaction will continue to be crucial for applications in industry (e.g., automated factories, control of energy systems), hazardous domains (e.g., deep space, radioactive environments), and other areas. However, other applications, **ranging from disaster recovery to scientific discovery, are most effectively addressed by a combination of humans and AI** systems working together
- **Subcategories:**
    - **Developing the Science of Human-AI Teaming;**
        - These studies will involve understanding the additional capabilities that a machine needs in order to become an effective teammate for the relevant tasks and environments and includes the modeling of human interactions.
        - AI systems perform peripheral tasks that support the human decision-maker
        - AI systems perform complex monitoring functions
        - AI systems perform tasks for which humans have very limited capabilities
        - **Low hanging fruit - just need to do efficacy study**
    - Seeking Improved Models and Metrics of Performance;
        - Waste of time - no long term excitement
    - Cultivating Trust in Human-AI Interactions;
        - Waste of time - academic research
    - Pursuing Greater Understanding of Human-AI Systems;
        - More about replicability: testbeds and methodologies to measure the effectiveness of human-AI teaming in settings that replicate the complexity of the operational environments also becomes critically important.
    - and **Developing New Paradigms for AI Interactions and Collaborations**.
        - research is needed to understand the influence of **interaction design on decision-making, skill retention**, training requirements, job satisfaction, and overall human-AI team performance and resilience.
        - **Low hanging fruit - just need to do efficacy study**
        - **Skip human factors - do** research areas include understanding user needs and user requirements; the role of context in AI-teaming application use; the use of task analysis and iterative design methods; and ways to measure efficiency, effectiveness, and performance of AI-teaming applications.

Strategy 3: Understand and address the ethical, legal, and societal implications of AI.  
Skip - Lockheed Martin is not ready to scale this - it's policy work for the most part.  
Strategy 4: Ensure the safety and security of AI systems.  
Current Contexts and Concerns” workshop report,52 which defines safety as mitigating against a system producing new harm, and security as monitoring a system’s integrity. This usage is consistent with the NIST AI RMF  
Strategy 5: Develop shared public datasets and environments for AI training and testing.  
Not a private business interest.  
Strategy 6: Measure and evaluate AI systems through standards and benchmarks.  
Not a private business interest.  
Strategy 7: Better understand the national AI R&D workforce needs  
Not a private business interest.  
Strategy 8: Expand public-private partnerships to accelerate advances in AI  
Not a private business interest.  
Strategy 9: Establish a principled and coordinated approach to international collaboration in AI research. P  
Not a private business interest.