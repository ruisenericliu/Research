**Look into Langchain**
 
**Stack for Generative AI development:**  
[https://medium.com/cowboy-ventures/the-new-infra-stack-for-generative-ai-9db8f294dc3f](https://medium.com/cowboy-ventures/the-new-infra-stack-for-generative-ai-9db8f294dc3f)
 
LLM Agent building: [https://lilianweng.github.io/posts/2023-06-23-agent/](https://lilianweng.github.io/posts/2023-06-23-agent/)
 
Long text: [https://lmsys.org/blog/2023-06-29-longchat/](https://lmsys.org/blog/2023-06-29-longchat/)
 
**UI Interfaces for Auto GPT:**  
**In particular:** [https://arxiv.org/abs/2303.17580](https://arxiv.org/abs/2303.17580)  
What is Hugging face up to?? [https://apply.workable.com/huggingface/](https://apply.workable.com/huggingface/)  
[https://huggingface.co/spaces/microsoft/ChatGPT-Robotics](https://huggingface.co/spaces/microsoft/ChatGPT-Robotics)  
[https://www.microsoft.com/en-us/research/group/autonomous-systems-group-robotics/articles/chatgpt-for-robotics/](https://www.microsoft.com/en-us/research/group/autonomous-systems-group-robotics/articles/chatgpt-for-robotics/)
 
Replacing photoshop UI: [https://huggingface.co/papers/2305.10973](https://huggingface.co/papers/2305.10973)
 
**Retraining Llama 2 :** [https://www.philschmid.de/instruction-tune-llama-2](https://www.philschmid.de/instruction-tune-llama-2)
 
How RLHF works for GPT: [https://huyenchip.com/2023/05/02/rlhf.html](https://huyenchip.com/2023/05/02/rlhf.html)
   

NLP:  
Stanford Natural Language Inference  
ReCLor  
Visual Question Answering Challenge  
Proc Gen

Compute faster: [https://geohot.github.io//blog/jekyll/update/2023/05/24/the-tiny-corp-raised-5M.html](https://geohot.github.io//blog/jekyll/update/2023/05/24/the-tiny-corp-raised-5M.html)
 
Misc:
 
Preserving dead languages: [https://www-technologyreview-com.cdn.ampproject.org/c/s/www.technologyreview.com/2023/05/22/1073471/metas-new-ai-models-can-recognize-and-produce-speech-for-more-than-1000-languages/amp/](https://www-technologyreview-com.cdn.ampproject.org/c/s/www.technologyreview.com/2023/05/22/1073471/metas-new-ai-models-can-recognize-and-produce-speech-for-more-than-1000-languages/amp/)
 
Some guy's kooky philosophy on binding things together via GNN-GPT: [https://experiencestack.co/embrace-complexity-part-1-39483f10a47f](https://experiencestack.co/embrace-complexity-part-1-39483f10a47f)
 
Something in Quantum backprop that will make sense in ~ 5 years:  
[https://scirate.com/arxiv/2305.13362](https://scirate.com/arxiv/2305.13362)

Vectorizing Your Knowledge: Connecting Knowledge Graphs with LLMs 🔗
 
Are you looking to unleash the true potential of your organisation's knowledge assets? Combining the power of Large Language Models (LLMs) with the reliability of Knowledge Graphs can be a game-changer. However, bridging the gap between these two representations has been an ongoing challenge. Today, I'll introduce a simple and pragmatic technique to connect your knowledge graph to LLMs effectively.
 
Here's a step-by-step approach to get you started:
 
⭕ Extract Relevant Nodes: Begin by pulling all the nodes that you wish to index from your Knowledge Graph, including their descriptions:
 
rows = rdflib_graph.query(‘SELECT * WHERE {?uri dc:description ?desc}’)
 
⭕Generate Embedding Vectors: Employ your large language model to create an embedding vector for the description of each node:
 
node_embedding = openai.Embedding.create(input = row.desc, model=model) ['data'][0]['embedding']
 
⭕Build a Vector Store: Store the generated embedding vectors in a dedicated vector store:
 
index = faiss.IndexFlatL2(len(embedding))  
index.add(embedding)
 
⭕Query with Natural Language: When a user poses a question in natural language, convert the query into an embedding vector using the same language model. Then, leverage the vector store to find the nodes with the lowest cosine similarity to the query vector:
 
question_embedding = openai.Embedding.create(input = question, model=model) ['data'][0]['embedding']  
d, i = [index.search](http://index.search)(question_embedding, 100)
 
⭕Semantic Post-processing: To further enhance the user experience, apply post-processing techniques to the retrieved related nodes. This step refines the results and presents information in a way that best provides users with actionable insights.
 
Remember, there are several approaches to connecting LLMs and Knowledge Graphs, but the method outlined here is one of the simplest and most accessible options for developers. It serves as an excellent starting point for those interested in harnessing the power of both technologies effectively.
 
This is a scheduled post, I am still on holiday right now and enjoying a digital detox, but I will answer comments upon my return in one week. (As mentioned before this family holiday was designed by ChatGPT – let me know in the comments if you would like a no-BS review of how that went 😱)
 
⭕Checkout my previous post on Continuous and Discrete Knowledge for some background: [https://lnkd.in/e2FJp8g7](https://lnkd.in/e2FJp8g7)  
⭕What is RDFlib?: [https://lnkd.in/e3UAsvg4](https://lnkd.in/e3UAsvg4)  
⭕ What are Openai Embeddings?: [https://lnkd.in/e3D8N2Ku](https://lnkd.in/e3D8N2Ku)  
⭕What is the FAISS Vector Store?:   [https://lnkd.in/e8YpmUjk](https://lnkd.in/e8YpmUjk)
 
[#KnowledgeGraph](https://www.linkedin.com/feed/hashtag/?keywords=knowledgegraph&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7095675217133359104) [#LLMs](https://www.linkedin.com/feed/hashtag/?keywords=llms&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7095675217133359104) [#DataScience](https://www.linkedin.com/feed/hashtag/?keywords=datascience&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7095675217133359104) [#ai](https://www.linkedin.com/feed/hashtag/?keywords=ai&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7095675217133359104) [#SemanticSearch](https://www.linkedin.com/feed/hashtag/?keywords=semanticsearch&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7095675217133359104)
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>    
Yann LeCun  
My unwavering opinion on current (auto-regressive) LLMs  
1. They are useful as writing aids.  
2. They are "reactive" & don't plan nor reason.  
3. They make stuff up or retrieve stuff approximately.  
4. That can be mitigated but not fixed by human feedback.  
5. Better systems will come.  
6. Current LLMs should be used as writing aids, not much more.  
7. Marrying them with tools such as search engines is highly non trivial.  
8. There *will* be better systems that are factual, non toxic, and controllable. They just won't be auto-regressive LLMs.  
9.I have been consistent with the above while defending Galactica as a scientific writing aid.  
10. Warning folks that AR-LLMs make stuff up and should not be used to get factual advice.  
11. Warning that only a small superficial portion of human knowledge can ever be captured by LLMs.  
12. Being clear that better system will be appearing, but they will be based on different principles.  
They will not be auto-regressive LLMs.  
13. Why do LLMs appear much better at generating code than generating general text?  
Because, unlike the real world, the universe that a program manipulates (the state of the variables) is limited, discrete, deterministic, and fully observable.  
The real world is none of that.  
14. Unlike what the most acerbic critics of Galactica have claimed  
- LLMs *are* being used as writing aids.  
- They *will not* destroy the fabric of society by causing the mindless masses to believe their made-up nonsense.  
- People will use them for what they are helpful with.
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>