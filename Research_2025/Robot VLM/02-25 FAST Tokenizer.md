Excited to release FAST, a universal tokenizer that trains VLAs x5 faster! This is going to be a game changer for dexterous high frequency control like humanoids! 🤖  
What's the main idea? When we tokenize actions for VLAs, we typically use naive discretization. But this is suboptimal, because within action chunks, sequential actions are very similar. These correlations between actions mean that the information in each token is very low. Our proposed tokenizer, FAST, uses DCT to compress actions, followed by BPE. This makes the tokenization much better -- the same action chunks require many fewer tokens and are much more information-dense, leading to much more effective training.  
One of my favorite results: we train a VLA on the DROID dataset that can do zero-shot language tasks in the wild! We tested it in real unseen kitchens across Berkeley, Stanford and UW.
 
This was a fantastic collab between Physical Intelligence and Berkeley Artificial Intelligence Research led by rockstars Karl Pertsch and Kyle Stachowicz!  
Project: [https://lnkd.in/gz5cCiu9](https://lnkd.in/gz5cCiu9)  
Paper: [https://lnkd.in/gJEYd4mr](https://lnkd.in/gJEYd4mr)  
Code & Tokenizer: [https://lnkd.in/gxn4tdmy](https://lnkd.in/gxn4tdmy)
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>