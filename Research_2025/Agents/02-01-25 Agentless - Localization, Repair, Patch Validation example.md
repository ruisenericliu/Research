You don’t need agent libraries to solve complex business problems. Agentless is a non-agent framework adopted by OpenAI to achieve the highest accuracy on the SWE Bench with o3. SWE-bench is a benchmark of real-world software engineering problems from GitHub. Agentless follows a simple three-phase process: localization, repair, and patch validation:
 
1️⃣ Generate a tree-like structure of the repository along with the issue/feature description.  
2️⃣ Use prompting and embedding-based retrieval to identify the top suspicious files.  
3️⃣ Only provide the LLM with class and function signatures (the “skeleton”) for each suspicious file.  
4️⃣ Within the identified classes/functions, pinpoint exact lines to modify.  
5️⃣ LLM generates multiple Search/Replace diffs (patches) for each location that might resolve the issue.  
6️⃣ Prompt the LLM to create tests that confirm whether the bug still appears.  
7️⃣ Run regression tests to avoid breaking existing behavior.  
8️⃣ Pick the best patch (via majority vote and test consistency) and update the files
 
Insights:  
🥇 Anthropic Claude 3.5 Sonnet achieves 40.7% and 50.8% solve rate on SWE-bench lite and verified  
🧠 Adopted by OpenAI for GPT-4o, o1 and o3 model performance.  
💰Average cost of $0.70 per issue, significantly lower than agent-based approaches  
🔍 Combining embedding and prompt retrieval improves accuracy  
🧪 Generating reproduction tests significantly boost patch selection  
📝 Using Search/Replace diffs instead of complete code rewrites reduces errors  
💡 A simple localize+repair pipeline can beat agent-based frameworks
 
Paper: [https://lnkd.in/e83yniwq](https://lnkd.in/e83yniwq)  
Github: [https://lnkd.in/eqq8w9iJ](https://lnkd.in/eqq8w9iJ)
 
Agentless is a great example of how focusing on solving problems can avoid the complexity and pitfalls of traditional agent-based systems.
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>