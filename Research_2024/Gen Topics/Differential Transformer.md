|   |
|---|
|**Differential Transformer**|
|⇧ 1,708 Likes|
|**Problem**  <br>Transformer models tend to overallocate attention to irrelevant context, leading to challenges in accurately retrieving key information.<br><br>  <br><br>**Solution**  <br>The paper introduces Differential Transformer, which uses a differential attention mechanism that calculates attention scores as the difference between two separate softmax attention maps. This cancels out noise and promotes sparse attention patterns.<br><br>  <br><br>**Results**  <br>Differential Transformer outperforms standard Transformer in language modeling across various model sizes and training regimes. It shows notable advantages in long-context modeling, key information retrieval, hallucination mitigation, and in-context learning. The architecture reduces activation outliers, potentially enabling more efficient quantization. Scaling studies indicate Differential Transformer requires only about 65% of the model size or training tokens needed by Transformer to achieve comparable performance.|
 ![No alt text provided for this image](Exported%20image%2020260222202457-0.jpeg)   
⚡️ Most important breakthrough this month: Differential Transformer vastly improves attention ⇒ better retrieval and fewer hallucinations!
 
Thought that self-attention could not be improved anymore?
 
Researchers from [Microsoft Research](https://www.linkedin.com/company/microsoftresearch/) and [Tsinghua University](https://www.linkedin.com/company/tsinghua-university/) have dropped a novel "differential attention" mechanism that amplifies focus on relevant context while canceling out noise. It sounds like a free lunch, but it does really seem to vastly improve LLM performance!
 
Key insights:
 
🧠 Differential attention computes the difference between two separate softmax attention maps, canceling out noise and promoting sparse attention patterns
 
🔥 DIFF Transformer outperforms standard Transformers while using 35-40% fewer parameters or training tokens
 
📏 Scales well to long contexts up to 64K tokens, leveraging increasing context length more effectively
 
🔎 Dramatically improves key information retrieval, enhancing in-context learning, and possibly reducing risk of hallucinations 🤯
 
🔢 Reduces activation outliers, potentially enabling lower-bit quantization without performance drop!
 
⚙️ Can be directly implemented using existing FlashAttention kernels
 
This new architecture could lead much more capable LLMs, with vastly improved strengths in long-context understanding and factual accuracy.
 
But they didn’t release weights on the Hub: let’s wait for the community to train the first open-weights DiffTransformer! 🚀
 
Read their paper 👉 [https://lnkd.in/eDezNXyT](https://lnkd.in/eDezNXyT)
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>  

⚡️ Most important breakthrough this month: Differential Transformer vastly improves attention ⇒ better retrieval and fewer hallucinations!
 
Thought that self-attention could not be improved anymore?
 
Researchers from [Microsoft Research](https://www.linkedin.com/company/microsoftresearch/) and [Tsinghua University](https://www.linkedin.com/company/tsinghua-university/) have dropped a novel "differential attention" mechanism that amplifies focus on relevant context while canceling out noise. It sounds like a free lunch, but it does really seem to vastly improve LLM performance!
 
Key insights:
 
🧠 Differential attention computes the difference between two separate softmax attention maps, canceling out noise and promoting sparse attention patterns
 
🔥 DIFF Transformer outperforms standard Transformers while using 35-40% fewer parameters or training tokens
 
📏 Scales well to long contexts up to 64K tokens, leveraging increasing context length more effectively
 
🔎 Dramatically improves key information retrieval, enhancing in-context learning, and possibly reducing risk of hallucinations 🤯
 
🔢 Reduces activation outliers, potentially enabling lower-bit quantization without performance drop!
 
⚙️ Can be directly implemented using existing FlashAttention kernels
 
This new architecture could lead much more capable LLMs, with vastly improved strengths in long-context understanding and factual accuracy.
 
But they didn’t release weights on the Hub: let’s wait for the community to train the first open-weights DiffTransformer! 🚀
 
Read their paper 👉 [https://lnkd.in/eDezNXyT](https://lnkd.in/eDezNXyT)
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>