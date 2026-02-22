Deeper Research with LLMs becomes more relevant. STORM or “Synthesis of Topic Outlines through Retrieval and Multi-perspective” is a paper that proposes a multi-question, iterative research, verifiable content generation, very similar to Google DeepMind Gemini Deep Research and OpenAI Deep Research.
 
Implementation
 
1️⃣ User provides a topic, Wikipedia is used to identify related topics and LLM is used to generate multipe diverse perspectives per topic.
 
2️⃣ For each perspective, the Agent simulates a conversations between LLMs by generating questions, breaking them into search queries, searching the internet, filtering for reliable sources, synthesizing answers, and repeating this process iteratively.
 
3️⃣ Agent creates a draft outline based on the initial topic and then refines it using the information gathered from the simulated conversations.
 
4️⃣ For each section in the outline (3️⃣), retrieve relevant references (2️⃣) and generate section content with citations. Then concatenate sections, remove redundancy, and generate an introduction section.
 
Insights  
- 🔍 Multi-perspective lead to more comprehensive research and better coverage  
- 💬 Simulated conversations between improve information gathering  
- 📋 Two-stage outline creation (draft + refinement) improves article organization  
- 📊 GPT-4 achieves 92.73% heading recall and 85.18% citation precision  
- 📚 70% of Wikipedia editors found the articles well-organized, and 100% agreed the system helps in pre-writing.  
- ❌ Only explored Wikipedia as knowledge source  
- 🤗 Code and prompts available on Github
 
Paper: [https://lnkd.in/eCnpzjyk](https://lnkd.in/eCnpzjyk)  
Github: [https://lnkd.in/eAibPp4i](https://lnkd.in/eAibPp4i)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>