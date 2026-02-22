Imitation is the foundation of [hashtag#LLM](https://www.linkedin.com/feed/hashtag/?keywords=llm&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7237479394858991616) training.
 
And it is a [hashtag#ReinforcementLearning](https://www.linkedin.com/feed/hashtag/?keywords=reinforcementlearning&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7237479394858991616) problem! In comparison to supervised learning, RL -here inverse RL- better exploits sequential structure, online data and further extracts rewards.
 
Beyond thrilled to share insights in our [Google DeepMind](https://www.linkedin.com/company/googledeepmind/) preprint!
 
[https://lnkd.in/eCQSbtQJ](https://lnkd.in/eCQSbtQJ)
 
Sequential Structure  
Previously, Imitation via RL (and IRL) has been hard to scale or stabilize. Its classical value iteration based formulations and variants required solving the complete RL problem before updating the rewards. Ideas like GAIL changed this but at a cost of the complexity and instability of adversarial learning.
 
Nearly a decade ago while visiting [Pieter Abbeel](https://www.linkedin.com/in/pieterabbeel/)’s lab, we’ve seen how challenging it is to stabilize GAIL even on simple control suite tasks.  
[https://lnkd.in/e8aDkr2G](https://lnkd.in/e8aDkr2G)  
[https://lnkd.in/ekKtA-w2](https://lnkd.in/ekKtA-w2)
 
A new stream of research, focuses on another basic RL object: Q-functions (which can parametrize both reward and policy) and has become drastically easier to use. For our work in particular, we reformulate a pure offline version of IQLearn as temporal difference regularized MLE enabling us to interpolate between the robustness of MLE and the efficacy of IRL.  
[https://lnkd.in/eF_h-7SP](https://lnkd.in/eF_h-7SP)
 
This leads to consistently better or on par performance with MLE and additionally considerably higher diversity of model generations. By effectively integrating sequence information during training, it is also less required during inference time: We find that IQLearn alone outperforms MLE plus beam search and does mostly not benefit from BS.
 
Online Data  
We further investigate the impact of self-generated online data and find that it is not required to outperform MLE. There is a nice toy example added which provides intuition why the autoregressive, concatenation based dynamics reduce the impact of self-generated data pointing towards the importance of expanding our action to enable corrections (which also impacts RLHF).
 
Rewards  
A key benefit of IRL compared with MLE is the ability to extract rewards. We analyze the correlation of IRL-extracted rewards and task performance metrics and find overall strong correlation.
 
But we also find that specific tasks can be harder to represent: e.g. answers for GSM8k might look stylistically good - for nearly all tokens except for the exact numerical answer. While generative behavior is good in this setting, learning discriminative reward information remains harder and represents an interesting space for future work.
 
A fantastic cross-team and cross-location effort including a total of seven different offices. Incredible work with Michael Bloesch, [Nino Vieillard](https://www.linkedin.com/in/nino-vieillard-929518137/), [Arun Ahuja](https://www.linkedin.com/in/arun-ahuja-1098aa24/), [Jörg Bornschein](https://www.linkedin.com/in/j%C3%B6rg-bornschein-8a005b216/), [Sandy Huang](https://www.linkedin.com/in/sandy-huang-490a7919/), Artem Sokolov, [Matt Barnes](https://www.linkedin.com/in/mbarnes1/), Guillaume Desjardins, [Alex Bewley](https://www.linkedin.com/in/alex-bewley-02185652/), Sarah Bechtle, Jost Tobias Springenberg, [Nikola Momchev](https://www.linkedin.com/in/nmomchev/), [Olivier Bachem](https://www.linkedin.com/in/olivier-bachem-10257756/), Matthieu Geist, and [Martin Riedmiller](https://www.linkedin.com/in/martin-riedmiller-636b3471/)!
 \> From \<[https://www.linkedin.com/feed/update/urn:li:activity:7237479394858991616/](https://www.linkedin.com/feed/update/urn:li:activity:7237479394858991616/)\>