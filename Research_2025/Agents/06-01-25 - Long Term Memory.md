Consistent, long-term memory across conversations is a big challenge in Agents! Mem0 tries to solve this by dynamically extracting, consolidateing, and retrieving salient information, achieving 26% better performance while reducing latency by 91% and token costs by 90%.
 
How it works:  
1️⃣ Extract salient information from conversations using an LLM with dual context (a conversation summary combined with recent messages).  
2️⃣ Use LLM to process context and extract important new information and compares them against existing ones using semantic similarity.  
3️⃣ Update Memory (ADD, UPDATE, DELETE, or NOOP), for Mem0g variant (graph), extract entities and relationships.  
4️⃣ Use vector similarity search to fetch relevant memories for response generation.
 
Key Insights  
- 💡 A scalable memory-centric architecture with graph-based variant.  
- 🔧 Dynamically extracts, consolidates, and retrieves salient information.  
- 🧠 Uses an LLM to determine memory updates (ADD, UPDATE, DELETE, NOOP).  
- 🕸️ Can represents memories as graph (entities are nodes, relationships are edges).  
- 📊 Outperform on LOCOMO, RAG, full-context, open, and closed memory solutions.  
- 🏆 91% lower p95 latency and over 90% token cost savings compared to full-context.  
- ⏱️ Memory construction completes in under a minute.
 
Paper: [https://lnkd.in/eFv_NnYq](https://lnkd.in/eFv_NnYq)  
Github: [https://lnkd.in/ee_aag8p](https://lnkd.in/ee_aag8p)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>