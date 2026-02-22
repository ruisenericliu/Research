How good are ReAct Agents under pressure? ReACT (Reasoning and Acting) Agents are AI Agents that combine reasoning with tool calling, enabling them to iteratively think through problems, use tools, and act based on observations to achieve goals.
 
LangChain ran benchmarks on far can we push single ReAct Agents by scaling domains (Topic Area, e.g. Customer Support) and available tools.
 
Results:  
🔬 Evaluated Tool calling trajectory (the order of the called tools) and final output with LLM as a Judge.  
🦙 Benchmarked Claude 3.5 sonnet, gpt-4o, o1, o3-mini & Llama 3.3 70B  
🧠 Both more context and more tools degrade agent performance  
📉 Performance on tasks requiring 3+ tool calls dropped more severely than simpler tasks  
🛠️ o1, o3-mini, and claude-3.5-sonnet outperform gpt-4o and llama-3.3-70B, .  
📅 Calendar Scheduling: o1 (71%) and o3-mini (68%) were top performers with the base domain.
 
Blog: [https://lnkd.in/ekrnuW62](https://lnkd.in/ekrnuW62)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>