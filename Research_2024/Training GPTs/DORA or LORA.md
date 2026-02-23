DoRA a new, better, and faster LoRA? 🤔 DoRA, or Weight-Decomposed Low-Rank Adaptation, is a new, Parameter Efficient fine-tuning technique that claims to enhance the learning capacity and training stability of LoRA, while avoiding any additional overhead. 🤯
 
DoRA decomposes the weights into two components, magnitude, and direction. DoRA adjusts how important each part of the data is (magnitude) and how the model should focus on learning (direction). It's like fine-tuning the details of a picture without needing to redraw the whole thing. 🖼️
 
𝗜𝗻𝘀𝗶𝗴𝗵𝘁𝘀:  
🏅 DoRA consistently outperforms LoRA  
🤗 Supported in Hugging Face PEFT  
♻️ Trained Adapters can be merged back into the model  
📈 +3.4% on Llama 7B and +1.0% on Llama 13B compared to LoRA on common reasoning  
🔐 Improved training stability compared to LoRA  
❌ In PEFT, DoRA only supports linear layers at the moment.
 
Paper: [https://lnkd.in/eiQ-ZVTW](https://lnkd.in/eiQ-ZVTW)  
Peft documentation: [https://lnkd.in/eMYWeGip](https://lnkd.in/eMYWeGip)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>