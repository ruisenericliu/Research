Some thoughts on Self-Play and self critiquing in LLMs (responding to replies to the tweet below--doing a quote tweet so I can consolidate the responses). [A mini Post-thanksgiving Teach-in]
 
1. If by self-play we mean LLMs generating and critiquing their own ideas by themselves, I don't see it working. That is because  
2. Self critiquing by LLMs doesn't quite work; LLMs generating ideas and having them critiqued with external verifiers (aka LLM-Modulo mode) does seem to (c.f. [https://x.com/rao2z/status/1715800819239678013?s=20](https://twitter.com/rao2z/status/1715800819239678013?s=20))
 
3. If you allow for an external verifier (be it a CSP solution checker, a plan correctness checker like VAL, or a proof checker like Lean) as part of self-play, then sure that could work--for those narrow domains. There are no "universal verifiers".
 
4. If you are thinking of self-play with external verifier as a way to generate oodles more synthetic data on which LLM fine-tunes itself--that is a possibility.
 
5. You can view this as a round-about System 2 to System 1 compilation (c.f. [https://x.com/rao2z/status/1708329785745928558?s=20](https://twitter.com/rao2z/status/1708329785745928558?s=20)) --except that the system 2 is part outside the LLM. Specifically the test part of generate-test, supported by the verifier--is being brought into the generate part (something Minsky considered the main point of intelligence, btw..).
 
6. Seen this way, self-play with external verifiers is just converting reasoning into retrieval--by computing the deductive closure by generate-test, and then finetuning the generator (c.f. [https://x.com/rao2z/status/1699928891652219132?s=20](https://twitter.com/rao2z/status/1699928891652219132?s=20) )
 
7. Computing the deductive closure to speedup later processing is nothing new of course. (c.f. [https://x.com/rao2z/status/1289700742836580357?s=20](https://twitter.com/rao2z/status/1289700742836580357?s=20)) Where as the deductive closure would be indexed in the past, it is now used to fine tune the LLM n-gram model. Unlike indexing--which ensures that re-use of the stored data will be correct, fine-tuning LLM no longer retains that guarantee. We are instead hoping for any incidental generalization caused by the compression.
 
8. If any of this makes sense to you, then you realize that Q*Anon parade is not so much a harbinger of thanksgiving-eve AGI, but a teachable moment to connect seemingly disparate things and ridding them of magic..
 \> From \<[https://twitter.com/rao2z/status/1728121216479949048](https://twitter.com/rao2z/status/1728121216479949048)\>  

In my decade spent on AI, I've never seen an algorithm that so many people fantasize about. Just from a name, no paper, no stats, no product. So let's reverse engineer the Q* fantasy. LONG READ, Part I:
 
To understand the powerful marriage between Search and Learning, we need to go back to 2016 and revisit AlphaGo, a glorious moment in the AI history.  
It's got 4 key ingredients:
 
1. Policy NN (Learning): responsible for selecting good moves. It estimates the probability of each move leading to a win.
 
2. Value NN (Learning): evaluates the board and predicts the winner from any given legal position in Go.
 
3. MCTS (Search): stands for "Monte Carlo Tree Search". It simulates many possible sequences of moves from the current position using the policy NN, and then aggregates the results of these simulations to decide on the most promising move. This is the "slow thinking" component that contrasts with the fast token sampling of LLMs.
 
4. A groundtruth signal to drive the whole system. In Go, it's as simple as the binary label "who wins", which is decided by an established set of game rules. You can think of it as a source of energy that *sustains* the learning progress.
 
How do the components above work together?
 
AlphaGo does self-play, i.e. playing against its own older checkpoints. As self-play continues, *both Policy NN and Value NN are improved iteratively*: as the policy gets better at selecting moves, the value NN obtains better data to learn from, and in turn it provides better feedback to the policy. A stronger policy also helps MCTS explore better strategies.
 
That completes an ingenious "perpetual motion machine". In this way, AlphaGo was able to bootstrap its own capabilities and beat the human world champion, Lee Sedol, 4-1 in 2016. *An AI can never become super-human just by imitating human data alone.*
 
-----  
Q* will likely have 4 corresponding components as above. Let's take a deep dive in Part II: [https://lnkd.in/g2BYB_ES](https://lnkd.in/g2BYB_ES)
 \> From \<[https://www.linkedin.com/posts/drjimfan_in-my-decade-spent-on-ai-ive-never-seen-activity-7133879775399481344-Io9z/?utm_source=share&utm_medium=member_desktop](https://www.linkedin.com/posts/drjimfan_in-my-decade-spent-on-ai-ive-never-seen-activity-7133879775399481344-Io9z/?utm_source=share&utm_medium=member_desktop)\>