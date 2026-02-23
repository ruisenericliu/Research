Yesterday Apple strongly advocated for on-device AI with [Apple](https://www.linkedin.com/company/apple/) Intelligence! Today, we know they will run ~3B LLM on device (Mac, iPhone, iPad) using fine-tuned LoRA Adapters for different tasks, claiming to outperform other 7B and 3B LLMs! 👀
 
What we know:  
📱 On-device 3B with grouped-query-attention, activation and embedding quantization running on the neural engine  
📊 iPhone 15 Pro 0.6 ms time-to-first-token with 30 tokens/second latency  
❌ Server model size and details are unknown  
🔄 Dynamically load, cache, and swap LoRA adapter models as needed  
📈 On-device model 49K vocab size, while the server model 100K  
🛠️ Used Rejection Sampling and descent policy optimization and a leave-one-out advantage for RLHF  
📝 Used synthetic data generation for tasks like summaries  
🔍 750 evaluation samples for each production use case  
🇺🇸 Seems to be an English model, this would explain the limitation to US only  
🧠 Used Apple's AXLearn framework (JAX) and FSP to train on TPUs and GPUs  
⚡ 3B + Adapter outperforms Phi-3 mini on summarization  
🏆 3B + Adapter achieves 78.7% on IFEval \> Mistral 7B; Server Model matches GPT-4-Turbo
 
Blog: [https://lnkd.in/eE4et2kh](https://lnkd.in/eE4et2kh)
 
Excited to see Apple share details on how they productionize AI. It's especially exciting that they use fine-tuned adapters for different tasks to outperform much bigger and stronger models! 🤗 That’s the way! 🚀
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>