![No alt text provided for this image](Exported%20image%2020260222122209-0.jpeg)   
𝗣𝗼𝘁𝗲𝗻𝘁𝗶𝗮𝗹 𝗽𝗮𝗿𝗮𝗱𝗶𝗴𝗺 𝘀𝗵𝗶𝗳𝘁 𝗶𝗻 𝗟𝗟𝗠𝘀: 𝗻𝗲𝘄 𝗽𝗮𝗽𝗲𝗿 𝗯𝘆 𝗠𝗲𝘁𝗮 𝗰𝗹𝗮𝗶𝗺𝘀 𝘁𝗵𝗮𝘁 𝘄𝗲 𝗰𝗮𝗻 𝗴𝗲𝘁 𝗿𝗶𝗱 𝗼𝗳 𝘁𝗼𝗸𝗲𝗻𝗶𝘇𝗲𝗿𝘀! 🥳
 
Current LLMs process text by first splitting it into tokens. They use a module named "tokenizer", that -spl-it-s- th-e- te-xt- in-to- arbitrary tokens depending on a fixed dictionnary.  
On the Hub you can find this dictionary in a model's files under tokenizer.json.
 
➡️ This process is called BPE tokenization. It is suboptimal, everyone says it. It breaks text into predefined chunks that often fail to capture the nuance of language, struggles with non-english languages (grouping "the" as 1 token makes sense for english, but is useless in other languages). But it has been a necessary evil in language models since their inception.
 
💥 In Byte Latent Transformer (BLT), researchers at [Meta](https://www.linkedin.com/company/meta/) propose an elegant solution by eliminating tokenization entirely, working directly with raw bytes (on a lower level, text is encoded as bytes: 011011110101) while maintaining efficiency through dynamic "patches."
 
This had been tried before with different byte-level tokenizations, but it's the first time that an architecture of this type scales as well as BPE tokenization. And it could mean a real paradigm shift! 👏👏
 
𝗧𝗟;𝗗𝗥:  
🏗️ 𝗔𝗿𝗰𝗵𝗶𝘁𝗲𝗰𝘁𝘂𝗿𝗲:  
Instead of a lightweight tokenizer, BLT has a lightweight encoder that process raw bytes into patches. Then the patches are processed by the main heavy-duty transformers as we do normally (but for patches of bytes instead of tokens), before converting back to bytes.
 
🧩 𝗗𝘆𝗻𝗮𝗺𝗶𝗰 𝗣𝗮𝘁𝗰𝗵𝗶𝗻𝗴:  
Instead of fixed tokens, BLT groups bytes based on their predictability (measured by entropy) - using more compute for complex sequences and efficiently handling simple ones. This allows efficient processing while maintaining byte-level understanding.
 
🚀 𝗣𝗲𝗿𝗳𝗼𝗿𝗺𝗮𝗻𝗰𝗲:  
BLT matches or exceeds token-based models like Llama 3 while using up to 50% less compute at inference! It shows particular strength in handling noisy inputs, different scripts, and character-level tasks.
 
This shows that removing tokenization altogether can not only maintain, but improve performance and efficiency, challenging the long-held assumption that tokenization is necessary for practical language models.
 
I hope this breakthrough is confirmed and we can get rid of all the tokenizer stuff, it will make model handling easier!
 
Read their paper here 👉 [https://lnkd.in/eavCY4_2](https://lnkd.in/eavCY4_2)
 \> From \<[https://www.linkedin.com/feed/update/urn:li:activity:7273382398891810816/](https://www.linkedin.com/feed/update/urn:li:activity:7273382398891810816/)\>