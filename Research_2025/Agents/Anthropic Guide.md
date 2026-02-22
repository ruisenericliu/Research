Anthropic is killing it with these technical posts.
 
If you're an AI dev, stop what you are doing and go read this.
 
It shows, in great detail, how to implement an effective multi-agent research system.
 
Pay attention to these key parts:
 
Anthropic shares how they built Claude's new multi-agent Research feature, an architecture where a lead Claude agent spawns and coordinates subagents to explore complex queries in parallel.
 
They use the orchestrator-worker architecture. This system allows Claude to dynamically plan, search, and synthesize high-quality answers across large corpora using web, workspace, and custom tool integrations.
 
Orchestrator-Worker Design
 
The lead agent decomposes a query, spins up specialized subagents (each with their own tools, prompts, and memory), and integrates their results. This parallel, breadth-first design dramatically improves performance for research tasks over sequential LLM use. It yields 90% higher success rates in internal evals compared to single-agent Claude.
 
Token-efficient Scaling
 
Performance gains correlate strongly with token usage and parallel tool calls. By distributing work across multiple agents and context windows, Claude’s system scales reasoning capacity efficiently. However, this comes with a 15× token cost over standard chats, making it suitable for high-value queries only.
 
Prompt engineering is not dead!
 
Anthropic iteratively refined agent behavior via prompt design. They embedded heuristics for task complexity scaling, delegation clarity, tool selection, and thinking strategies. They also used Claude to self-optimize prompt and tool use, reducing task times by 40%.
 
Flexible Evaluation + Production Reliability
 
Anthropic uses LLM-as-judge scoring with rubrics for factuality, citation, and efficiency, alongside human testing to catch subtle failures. For reliability, they built resumable stateful agents with checkpointing, rainbow deployments, and full observability of agent decision traces, crucial for debugging non-deterministic, long-running agents.
 
[https://www.anthropic.com/engineering/built-multi-agent-research-system](https://www.anthropic.com/engineering/built-multi-agent-research-system)