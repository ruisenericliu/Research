𝐕𝐢𝐬𝐢𝐨𝐧 𝐥𝐚𝐧𝐠𝐮𝐚𝐠𝐞 𝐦𝐨𝐝𝐞𝐥𝐬: 𝐭𝐡𝐞 𝐠𝐢𝐚𝐧𝐭 𝐥𝐞𝐚𝐩𝐬 𝐨𝐟 𝐨𝐩𝐞𝐧-𝐬𝐨𝐮𝐫𝐜𝐞 𝐦𝐨𝐝𝐞𝐥𝐬 🦘
 
[Andrew Reed](https://www.linkedin.com/in/ACoAABHNSP4BCf6sKFrMia_cGyhzXSnSBFicC8U) built a cool space that shows that OS LLMs are catching up with closed source LLMs in ELO ranking in the Arena (link below).  
For vision, the same dynamic is happening: the field is still evolving fast, but soon OS models will be able to match GPT-4o’s vision skills.
 
I witnessed the Idefics team’s work and their many late nights before their publishing of Idefics-2-8b. Now they just published a paper that summarizes their insights!
 
𝙃𝙚𝙧𝙚’𝙨 𝙖 𝙨𝙪𝙢𝙢𝙖𝙧𝙮 𝙤𝙛 𝙬𝙝𝙖𝙩 𝙩𝙝𝙚𝙮 𝙛𝙤𝙪𝙣𝙙:
 
➤ 𝗣𝗲𝗿𝗳𝗼𝗿𝗺𝗮𝗻𝗰𝗲 𝗼𝗳 𝗩𝗟𝗠𝘀 𝗶𝘀 𝗹𝗮𝗿𝗴𝗲𝗹𝘆 𝗱𝗿𝗶𝘃𝗲𝗻 𝗯𝘆 𝗽𝗲𝗿𝗳 𝗼𝗳 𝘁𝗵𝗲𝗶𝗿 𝘁𝗲𝘅𝘁-𝗼𝗻𝗹𝘆 𝗯𝗮𝗰𝗸𝗯𝗼𝗻𝗲𝘀. In ablation studies, replacing the llama-1-7b with Mistral-7b directly brings +7% performance 🤯
 
➤ 𝗧𝗵𝗲𝘆 𝗰𝗼𝗺𝗽𝗮𝗿𝗲𝗱 𝘁𝘄𝗼 𝗰𝗼𝗺𝗽𝗲𝘁𝗶𝗻𝗴 𝗮𝗿𝗰𝗵𝗶𝘁𝗲𝗰𝘁𝘂𝗿𝗲𝘀:  
- 🔀 𝗖𝗿𝗼𝘀𝘀 𝗮𝘁𝘁𝗲𝗻𝘁𝗶𝗼𝗻 𝗮𝗿𝗰𝗵𝗶𝘁𝗲𝗰𝘁𝘂𝗿𝗲: images are encoded through the vision backbone, and their information is inserted within the text processing at various places  
- 🔢 𝗙𝘂𝗹𝗹𝘆 𝗮𝘂𝘁𝗼𝗿𝗲𝗴𝗿𝗲𝘀𝘀𝗶𝘃𝗲 𝗮𝗿𝗰𝗵𝗶𝘁𝗲𝗰𝘁𝘂𝗿𝗲: the output is directly concatenated to the sequence of text embeddings, and entire sequence passed as input to the LM (cf image)  
The comparison's outcome is the following ⇒ 𝗙𝘂𝗹𝗹𝘆 𝗮𝘂𝘁𝗼𝗿𝗲𝗴𝗿𝗲𝘀𝘀𝗶𝘃𝗲 𝗮𝗿𝗰𝗵𝗶𝘁𝗲𝗰𝘁𝘂𝗿𝗲 𝗼𝘂𝘁𝗽𝗲𝗿𝗳𝗼𝗿𝗺𝘀 𝗰𝗿𝗼𝘀𝘀-𝗮𝘁𝘁𝗲𝗻𝘁𝗶𝗼𝗻 𝗮𝗿𝗰𝗵𝗶𝘁𝗲𝗰𝘁𝘂𝗿𝗲 when you fine-tune the whole system using LoRA
 
➡️ 𝗧𝗵𝗲𝘀𝗲 𝗳𝗶𝗻𝗱𝗶𝗻𝗴𝘀 𝗹𝗲𝗱 𝘁𝗼 𝘀𝗲𝘃𝗲𝗿𝗮𝗹 𝗮𝗿𝗰𝗵𝗶𝘁𝗲𝗰𝘁𝘂𝗿𝗮𝗹 𝗶𝗺𝗽𝗿𝗼𝘃𝗲𝗺𝗲𝗻𝘁 𝗶𝗻 𝗜𝗱𝗲𝗳𝗶𝗰𝘀-𝟮:  
➤ Replaced cross-attention architecture with fully autoregressive architecture  
➤ Enable treating images with varying aspect ratio  
➤ Allow to split an image in 4, to be encoded on 320 vision tokens instead of 64, if you want to increase perf at the cost of more compute
 
✨ As a result, Idefics-2 reaches state-of-the-art performance for this model size! Now just a few more steps to catch up to GPT-4o!
 
Congrats for this great release [Léo Tronchon](https://www.linkedin.com/in/ACoAACAdueYBmpnFOU8_oo7CAOBp-zGvll6mmV8) [Hugo Laurençon](https://www.linkedin.com/in/ACoAACMxEXQBc5mFHZjXBGUGf8lXLH54NjgGr_A) [Victor Sanh](https://www.linkedin.com/in/ACoAABuSz-MBn6jxcRvc72Y7BoEWaz4cUTI8D0A)! 👏
 
👉 𝗥𝗲𝗮𝗱 𝘁𝗵𝗲 𝗜𝗱𝗲𝗳𝗶𝗰𝘀-𝟮 𝗽𝗮𝗽𝗲𝗿: [https://lnkd.in/esKMq6Eu](https://lnkd.in/esKMq6Eu)  
🚀 𝗔𝗻𝗱𝗿𝗲𝘄’𝘀 𝘀𝗽𝗮𝗰𝗲 𝘁𝗵𝗮𝘁 𝘀𝗵𝗼𝘄𝘀 𝗢𝗦 𝗺𝗼𝗱𝗲𝗹𝘀 𝗰𝗮𝘁𝗰𝗵𝗶𝗻𝗴 𝘂𝗽 (𝗳𝗼𝗿 𝘁𝗲𝘅𝘁 𝗺𝗼𝗱𝗲𝗹𝘀): [https://lnkd.in/e5vX_Ukb](https://lnkd.in/e5vX_Ukb)  
⚔️ 𝗖𝗼𝗺𝗽𝗮𝗿𝗲 𝘃𝗶𝘀𝗶𝗼𝗻 𝗺𝗼𝗱𝗲𝗹𝘀 𝗶𝗻 𝘁𝗵𝗲 𝗩𝗶𝘀𝗶𝗼𝗻 𝗮𝗿𝗲𝗻𝗮: [https://lnkd.in/eAuDnSiV](https://lnkd.in/eAuDnSiV)
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>