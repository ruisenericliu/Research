Apple just dropped a new paper on LRMs and it’s not pretty. 🙈
 
Paper title: The Illusion of Thinking: Understanding the Strengths and Limitations of Reasoning Models via the Lens of Problem Complexity.
 
Some highlights:
 
🧩 Using controlled puzzle environments (e.g. Tower of Hanoi), the authors show that frontier LRMs like Claude 3.7 and DeepSeek-R1 𝗰𝗼𝗹𝗹𝗮𝗽𝘀𝗲 𝘁𝗼 𝟬% 𝗮𝗰𝗰𝘂𝗿𝗮𝗰𝘆 beyond a certain complexity threshold.
 
⚠️ Surprisingly, giving these models the 𝗲𝘅𝗮𝗰𝘁 𝘀𝗼𝗹𝘂𝘁𝗶𝗼𝗻 𝗮𝗹𝗴𝗼𝗿𝗶𝘁𝗵𝗺 doesn't help. They still fail to execute logical steps correctly - exposing severe limits in symbolic reasoning and step-by-step verification.
 
📉 Even worse, as problems get harder, 𝘁𝗵𝗲𝘀𝗲 𝗺𝗼𝗱𝗲𝗹𝘀 𝘀𝘁𝗮𝗿𝘁 𝘁𝗵𝗶𝗻𝗸𝗶𝗻𝗴 𝙡𝙚𝙨𝙨 - using fewer tokens despite having available budget. This suggests a compute scaling limit 𝘯𝘰𝘵 caused by external constraints, but internal brittleness.
 
🤖 They exhibit “overthinking”: generating correct answers early, then undermining them by exploring incorrect paths. And as complexity increases, the models stop finding correct answers altogether.
 
𝗜𝗺𝗽𝗹𝗶𝗰𝗮𝘁𝗶𝗼𝗻𝘀?
 
To me all this is consistent with the fact that current LRMs don’t “reason” in any robust or generalisable sense. They simulate reasoning through pattern-matching - and once the patterns break down so does their ability to reason.
 
Mistaking examples of reasoning for actual reasoning is a logical fallacy. Don't fall for it.
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>