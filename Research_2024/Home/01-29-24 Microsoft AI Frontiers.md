# Panel Discussion: AI Frontiers
 
(Multimodality, Goals, Intentions, Preferences, Open source to product)
 
Microsoft AI researchers discuss frontiers in small language models and where AI research and capabilities are headed next.
 
AI Frontiers: Coordinate ourselves very well on a very well-defined mission and go with it with conviction and go with it with speed and agility. So that’s what we are doing in our new organization that’s called AI Frontiers.  
One of the things I think we’ll do with AI Frontiers is provide more of a channel, a more coherent channel, of research artifacts like this into product.
 
**The truth is, nobody knows where AI is going to be 10 years from now, so it’s meaningless to plan at time horizons which are the usual time horizon that we are used to in research.**
 
**Ahmed Awadallah** – advantages of **multimodality**
 
- It looks like an AI that can perceive and operate in the real world is not that far off from where we are.
 
Imagine that we have an AI system that we can ask to do things on our behalf, both in the digital and in the physical world
 
**ECE KAMAR:** My dream for the AI systems is that they become our helpers, companions, longer-term collaborators than just, like, prompting something and it gives me an answer.
 
**Goals, Intentions, Preferences**
 
initial technologies to build on, to get to those AI systems that have a memory, that have a history, that have a deep understanding of human concepts,
 
**SÉBASTIEN BUBECK:** Yeah, my aspiration for AI, actually, has nothing to do with the technology itself. I hope that AI will illuminate how the human mind works.
 
**BUBECK:** It’s a terrible analogy. [LAUGHS] So it really … the transformer is absolutely not, in my mind, trying to mimic what the human brain is doing. It’s more like the emergent properties are similar.
 
At the end of the day, it has enormous **economical impact, because when you answer these questions, you go make everything smalle**r. And this is what we’ve been doing with the Phi series of models, trying to build those small language models.
 
Phi series, which is “Textbooks Are All You Need.”
 
the textbooks approach is perhaps a little bit weird because **there’s no textbook to teach you commonsense reasoning**
 
Reasoning as an emergent property:
 
**AWADALLAH:** We started with reasoning, as well, because reasoning is a pretty hard property, and we haven’t really seen reasoning emerging even to that level we have in models like GPT-4 right now, except after scaling to so large size in the model and in the data size, as well
 
We have never seen that with a small model, but what we have found out is that you can, actually, use a powerful model to demonstrate the solution strategy to the small model, and you can actually demonstrate so many solution strategies for so many tasks.
 
Fine tuning:
 
The one layer above that is all of the work that **Orca team is doing with fine-tuning specialization.** Taking a capability, taking a domain, taking some constraints and trying to see, like, I have these base models, but how do I make them work even better for the different domains and capabilities
 
Autogen (multi-agents)
 
So that multi-agent, what we mean by multi-agent orchestration is that imagine you have a complex task that you cannot reliably do by just prompting even the best model we have in our family. But what you can do is something very similar to how humans work actually. We take a complex prolem. We divide it into smaller pieces and then assign smaller pieces to different people that have different capabilities. That’s exactly how AutoGen framework works.
 
Kamar: Learning
 
They may be interacting with millions of people every day and getting feedback from them or seeing how people respond to it, but it does not make any of those systems better or more intelligent or understand their users any better. So I feel like this is one of the areas that we have to push forward very strongly.
 
What about benchmarks?
 
Requires a different way of thinking about the evaluation where we are not only evaluating the models, but we are evaluating the whole stack. We are actually saying, OK, let’s think about prompting. Let’s think about orchestration and understanding the complementarity of the stack