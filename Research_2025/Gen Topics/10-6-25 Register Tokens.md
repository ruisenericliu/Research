[https://open.substack.com/pub/mlhonk/p/40-vision-transformers-need-registers?r=50rx1o&utm_campaign=post&utm_medium=web&showWelcomeOnShare=true](https://open.substack.com/pub/mlhonk/p/40-vision-transformers-need-registers?r=50rx1o&utm_campaign=post&utm_medium=web&showWelcomeOnShare=true)
   

Large and sufficiently trained Vision Transformers are very smart.
 
So much so, they actually cause problems.
 
In short, they first figure out which image tokens are redundant, and then repurpose them as places to store, process, and retrieve global information.
 
Sneaky move, right? 🤨
 
Irrelevant background patches are the best candidates for the job, since their content can be easily inferred from the surroundings anyway.
 
This behavior is not bad in itself, but the fact that it happens inside regular patch tokens is undesirable, as it hurts performance on dense tasks by screwing up attention maps.
 
The solution? Add a few extra "register" tokens, train the model with those, and discard their output both during training and inference ✅
 
With just a little overhead due to the newly added tokens, global information gets stashed there, and the problem is solved. This is used in recent DINOv3 models, for example, with visible positive effects.
 
Read more about it in the article in the comments, it's a super interesting phenomenon that emerges at scale! ⏬
   

Great insights! Registers have been around since DINOv2 and they help, a tiny scratchpad so regular patches don’t get hijacked. Still, with long training, dense features can get messy. Gram Anchoring, introduced in DINOv3, really fixes that: it keeps the student in step with the EMA teacher’s patch similarities, which stops the slow drift and lifts dense feature quality beyond what registers alone deliver.