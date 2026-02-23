Let's build a multi-agent internet research assistant using OpenAI Swarm & Llama 3.2 (100% local)!
 
The app takes a user query, searches the web for it, and turns it into a well-crafted article.
 
Here's what you'll learn:
 
- [Ollama](https://www.linkedin.com/company/ollama/) for running LLMs locally  
- [OpenAI](https://www.linkedin.com/company/openai/) Swarm for multi-agent orchestration  
- [Streamlit](https://www.linkedin.com/company/streamlit/) for the UI
 
Let's go! 🚀
 
Key component:
 
1️⃣ Agent 1: Web search and tool use
 
The web-search agent takes a user query and then use the DuckDuckGo search tool to fetch results from internet.
 
2️⃣ Agent 2: Research Analyst
 
The role of this agent is to analyse and curate the raw search results and make them ready to use for the content writer agent.
 
3️⃣ Agent 3: Technical Writer
 
The role of technical writer is to use the curated results and turn them into a polished, publication-ready article .
 
4️⃣ The Chat interface
 
Finally we create a Streamlit UI to provide a chat interface for our application.  
____  
Find all the code in this GitHub repo: [https://lnkd.in/gMTZDvR9](https://lnkd.in/gMTZDvR9)  
____
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>     

This came unexpected! [OpenAI](https://www.linkedin.com/company/openai/) released Swarm, a lightweight library for building multi-agent systems. Swarm provides a stateless abstraction to manage interactions and handoffs between multiple agents and does not use the Assistants API. 👀
 
How it works:  
1️⃣ Define Agents, each with its own instructions, role (e.g., "Sales Agent"), and available functions (will be converted to JSON structures).  
2️⃣ Define logic for transferring control to another agent based on conversation flow or specific criteria within agent functions. This handoff is achieved by simply returning the next agent to call within the function.  
3️⃣ Context Variables provide initial context and update them throughout the conversation to maintain state and share information between agents.  
4️⃣ [Client.run](http://Client.run)() initiate and manage the multi-agent conversation. Needs initial agent, user messages, and context and returns a response containing updated messages, context variables, and the last active agent.
 
Insights  
🔄 Swarm manages a loop of agent interactions, function calls, and potential handoffs.  
🧩 Agents encapsulate instructions, available functions (tools), and handoff logic.  
🔌 The framework is stateless between calls, offering transparency and fine-grained control.  
🛠️ Swarm supports direct Python function calling within agents.  
📊 Context variables enable state management across agent interactions.  
🔄 Agent handoffs allow for dynamic switching between specialized agents.  
📡 Streaming responses are supported for real-time interaction.  
🧪 The framework is experimental. Maybe to collect feedback?  
🔧 Flexible and works with any OpenAI client, e.g. Hugging Face TGI or vLLM hosted models.
 
Repository: [https://lnkd.in/eWKMBkqU](https://lnkd.in/eWKMBkqU)
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>