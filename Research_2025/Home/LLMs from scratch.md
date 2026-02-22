[https://github.com/rasbt/LLMs-from-scratch](https://github.com/rasbt/LLMs-from-scratch)
 
Ultra LLM builder: [https://huggingface.co/nanotron](https://huggingface.co/nanotron)
   

Large Model Training:

**FB: How to Train VLMs:** [https://arxiv.org/abs/2405.17247](https://arxiv.org/abs/2405.17247)

- DeepSeek: [https://lnkd.in/gHC_U29z](https://lnkd.in/gHC_U29z)

DeepSeek Inference overview: [https://github.com/deepseek-ai/open-infra-index/blob/main/202502OpenSourceWeek/day_6_one_more_thing_deepseekV3R1_inference_system_overview.md](https://github.com/deepseek-ai/open-infra-index/blob/main/202502OpenSourceWeek/day_6_one_more_thing_deepseekV3R1_inference_system_overview.md)
   

Andrej Karpathy has released **nanochat**, a minimal, full-stack repo for training and running a ChatGPT-like model from scratch. Unlike his earlier **nanoGPT** (pretraining only), nanochat includes everything pretraining, midtraining, SFT, RL, inference, and a WebUI in ~8,000 lines of code.
 
You can boot a cloud GPU box and, in ~4 hours, get a working mini-chatbot.
 
**Key Features**

- **End-to-end:** Covers tokenizer, pretraining, midtraining, SFT, RL, and inference.
- **Minimal codebase**: ~8,000 lines, dependency-light, clean and hackable.
- **Cost-efficien**t: Train a ChatGPT-like model for ~$100 on 8×H100 (~4 hrs).
- **Scales up**: At ~$1,000 (~41 hrs), coherence improves on math/code/MCQ tasks.
- **Interfaces:** Talk to the model via CLI or ChatGPT-style WebUI.
- **Report card**: Generates a markdown summary of training metrics.

**How It Works**

- **Architecture**: Llama-like dense transformer with rotary embeddings and QK norm.
- **Optimizations**: Uses Muon + AdamW, multi-query attention, logit softcap.
- **Tokenizer**: Trains a Rust-based tokenizer from scratch.
- **Pretraining**: Runs on FineWeb and evaluates with CORE metrics.
- **Midtraining**: Uses SmolTalk conversations, MCQs, and tool-use data.
- **SFT**: Fine-tunes on ARC, MMLU, GSM8K, and HumanEval.
- **RL**: Optional reinforcement learning with GRPO on GSM8K math.
- **Inference**: Supports KV cache, prefill/decode, and Python sandbox tool use.

**Performance**

- ~$100 run (~4 hrs): Surpasses GPT-2 on CORE, simple Q&A/story tasks.
- ~$1,000 run (~41 hrs): Handles math/code problems and MCQs with coherence.
- Depth-30 model (24 hrs): 40s on MMLU, 70s ARC-Easy, 20s GSM8K.
- Coherence improves rapidly with scaling, approaching GPT-3-small behavior.

**How to Get Started**

- Clone: git clone [https://github.com/karpathy/nanochat](https://github.com/karpathy/nanochat)
- Spin up a GPU box (e.g. 8×H100 for speedrun).
- Run the training script (pretrain → midtrain → SFT → RL).
- Launch CLI or WebUI to chat with your model.

**Access & Availability**

- GitHub repo available
- Codebase: ~8,000 lines, open-source and designed to be forkable.