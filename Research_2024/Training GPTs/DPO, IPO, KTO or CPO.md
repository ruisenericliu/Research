DPO, IPO, KTO or CPO? What should you use for RLAIF?🤔 A new paper compares the performance across three distinct scenarios: (1) keeping the Supervised Fine-Tuning (SFT) part, (2) skipping the SFT part, and (3) skipping the SFT part and utilizing an instruction-tuned model.
 
𝗜𝗺𝗽𝗹𝗲𝗺𝗲𝗻𝘁𝗮𝘁𝗶𝗼𝗻  
1️⃣ Models: Zephyr-sft-full, Mistral-7B-v0.1, Mistral-instruct-7B-v0.2  
2️⃣ Datasets: UltraChat for SFT training; UltraFeedback-binarized for alignment method training.  
3️⃣ Fine-Tuning: Apply alignment methods (DPO, IPO, KTO, CPO) to different models depending on the Scenario  
4️⃣ Evaluation: Test the models across 13 benchmarks (MT-Bench, Big Bench, and Open LLM Leaderboard).
 
𝗜𝗻𝘀𝗶𝗴𝗵𝘁𝘀  
💻 Tested methods performed better with smaller datasets (Contrary to PPO) 🧮 KTO outperforms in tasks like mathematical problem-solving  
📝 None of the tested methods outperformed SFT in MMLU  
✅ KTO and IPO outperformed SFT by 17.5% on TruthfulQA  
💬 CPO performed worse than SFT on MT-Bench, indicating weaker performance in dialogue.  
🧠 Tested methods didn't significantly improve model reasoning  
🤗 Used [Hugging Face](https://www.linkedin.com/company/huggingface/) TRL for fine-tuning
 
Paper: [https://lnkd.in/e4WTwQVR](https://lnkd.in/e4WTwQVR)
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>