Need to run 🦙 [hashtag#Llama](https://www.linkedin.com/feed/hashtag/?keywords=llama&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7180552557382045696) faster?.......turns out you can just delete half the layers 🤯......... almost no impact on accuracy, but reduces cost significantly 👇👇
 
New research by [Meta](https://www.linkedin.com/company/metaoficial/), [Cisco](https://www.linkedin.com/company/cisco/) and [Massachusetts Institute of Technology](https://www.linkedin.com/company/mit/) combines pruning, quantization and PEFT across various [hashtag#opensource](https://www.linkedin.com/feed/hashtag/?keywords=opensource&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7180552557382045696) models to improve efficiency. Surprisingly, results show you can delete 20% to 50% of the model layers without impacting performance, while memory and compute declines linearly with layers pruned.
 
Interestingly, results also suggest that shallow layers are disproportionately important for models results, allowing deletion of deeper layers with minimal impact.
 
Method:  
1️⃣ Test Llama, Qwen, Mistral and Phi families of models from 70B to 2B  
2️⃣ Use similarity score to identify model layers for removal  
3️⃣ Progressively delete layers with lowest angular distance  
4️⃣ Apply post-pruning QLoRA tune on C4 dataset  
5️⃣ Test against MMLU and BoolQ benchmarks
 
Insights:  
🔹 Llama 70B: limited drop in accuracy after 40% layers removed  
🔹 Llama 13B: limited drop in accuracy after 50% layers removed  
🔹 Other models: limited drop in accuracy after 20-30% layers removed  
🔹 Memory / inference cost reduces linearly with layers pruned  
🔹 Shallow layers disproportionately impact model results  
🔹 Suggests current training might not leverage deeper layers effectively
 
Paper 👉 [https://lnkd.in/g4kix3HH](https://lnkd.in/g4kix3HH)
 \> From \<[https://www.linkedin.com/feed/update/urn:li:activity:7180552557382045696/](https://www.linkedin.com/feed/update/urn:li:activity:7180552557382045696/)\>