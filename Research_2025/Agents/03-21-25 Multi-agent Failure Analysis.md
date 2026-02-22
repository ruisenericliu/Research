Why Do Multi-Agent LLM Systems “still” Fail? A new study explores why Multi Agent Systems are not significantly outperforming single-agent. The study identifies 14 failure modes multi-agent system. Multi-agent system (MAS) are agents that interact, communicate, and collaborate to achieve a shared goal, which would to be difficult or unreliable for a single agent to accomplish.
 
Benchmark:  
- Selected five popular, open-source MAS (MetaGPT, ChatDev, HyperAgent, AppWorld, AG2)  
- Chose tasks representative of the MAS intended capabilities (Software D Development, SWE-Bench Lite, Utility Service Tasks, GSM-Plus) total of 150 tasks  
- Recorded the complete conversation logs, human annotators reviews, Cohen's Kappa score to ensure consistency and reliability, LLM-as-a-Judge Validation
   

Multi Agent Failure modes:  
1. Disobey Task Spec: Ignores task rules and requirements, leading to wrong output.  
2. Disobey Role Spec: Agent acts outside its defined role and responsibilities.  
3. Step Repetition: Unnecessarily repeats steps already completed, causing delays.  
4. Loss of History: Forgets previous conversation context, causing incoherence.  
5. Unaware Stop: Fails to recognize task completion, continues unnecessarily.  
6. Conversation Reset: Dialogue unexpectedly restarts, losing context and progress.  
7. Fail Clarify: Does not ask for needed information when unclear.  
8. Task Derailment: Gradually drifts away from the intended task objective.  
9. Withholding Info: Agent does not share important, relevant information.  
10. Ignore Input: Disregards or insufficiently considers input from others.  
11. Reasoning Mismatch: Actions do not logically follow from stated reasoning.  
12. Premature Stop: Ends task too early before completion or information exchange.  
13. No Verification: Lacks mechanisms to check or confirm task outcomes.  
14. Incorrect Verification: Verification process is flawed, misses critical errors.
    
How to improve Multi-Agent LLM System:  
📝 Define tasks and agent roles clearly and explicitly in prompts.  
🎯 Use examples in prompts to clarify expected task and role behavior.  
🗣️ Design structured conversation flows to guide agent interactions.  
✅ Implement self-verification steps in prompts for agents to check their reasoning.  
🧩 Design modular agents with specific, well-defined roles for simpler debugging.  
🔄 Redesign topology to incorporate verification roles and iterative refinement processes.  
🤝 Implement cross-verification mechanisms for agents to validate each other.  
❓ Design agents to proactively ask for clarification when needed.  
📜 Define structured conversation patterns and termination conditions.
   

Github: [https://lnkd.in/ebmCg28d](https://lnkd.in/ebmCg28d)  
Paper: [https://lnkd.in/etgsH6BH](https://lnkd.in/etgsH6BH)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>