Our @Reka AI Tech Report / Paper is out! 🔥
 
Tech reports with completely no information are kinda boring so we’re revealing some interesting information on how we train our series of Reka models including tokens, architecture, data & human evaluation workflows. 😎
 
We tried our best to give a behind-the-scenes experience of how we trained Core, Flash and Edge: our suite of highly performant multimodal LLMs.
 
In particular, if you enjoyed my previous blog post about training LLMs in the wilderness, there’s a dedicated section on that in this report!
 
We can’t disclose literally everything but we tried our best to make it interesting, I promise. 🙏
 
Here’s a rundown summary of some of the highlights.  
🔹 Edge and Flash are outrageously strong 7B and 21B models. They are trained on 4.5-5T tokens in total. Also, they have been improved significantly since their first public appearance! They outperform many popular faces. Some data mixture information is in the report.  
🔹 We discuss our internal human evaluation workflow, prompt distribution, and how we use Core for model development and automatic evaluation.  
🔹 We describe our infrastructure setup for training large models, quantifying node failures, and report loss curves for training our models.  
🔹 Aside from the hardware lottery, we also show how this affects node stability across time. Once we were told our cluster became less stable because there were "big guys" moving things around the data center.
 
On performance which you might have already seen on other threads.  
🔹 Core approaches frontier-class models like Claude3 Opus and GPT4-V. It outperforms Claude3 Opus on third-party blind human evaluation for multimodal chat, outperforms Gemini Ultra on video QA, and is quite competitive to other frontier models on core text metrics. It also matches GPT4-V on MMMU!  
🔹 Core ranks #2 on our internal multimodal chat leaderboard, right after GPT4-V. On text, it ranks #3 just behind Claude Opus and GPT4 Turbo. Core outperforms GPT-4 (0613) on this ranking.
 
This has been a focused and concentrated effort of a small team of ~20 people in the past 4 months (yes, we got access to 90%+ of our compute only late December last year!).
 
This tech report tells our story. Enjoy! Happy to answer any questions in replies or DM!
 
PS: it was nice writing in latex after one whole year!
 
PPS: I had quite some fun writing this.There's some puns and easter eggs and interesting tidbits in there. Trust me. 😏
 
Paper: [https://lnkd.in/g9AESjNz](https://lnkd.in/g9AESjNz)  
Launch blog: [https://lnkd.in/gun7BPPi](https://lnkd.in/gun7BPPi)  
Playground: [chat.reka.ai](http://chat.reka.ai)
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>