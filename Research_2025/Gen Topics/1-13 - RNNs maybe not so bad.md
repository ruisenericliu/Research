Old-school RNNs can actually rival fancy transformers!
 
Remember good old RNNs (Recurrent Neural Networks)? Well, researchers from Mila - Quebec Artificial Intelligence Institute and Borealis AI just have shown that simplified versions of decade-old RNNs can match the performance of today's transformers.
 
They took a fresh look at LSTMs (from 1997!) and GRUs (from 2014). They stripped these models down to their bare essentials, creating "minLSTM" and "minGRU". The key changes:  
❶ Removed dependencies on previous hidden states in the gates  
❷ Dropped the tanh that had been added to restrict output range in order to avoid vanishing gradients  
❸ Ensured outputs are time-independent in scale (not sure I understood that well either, don't worry)
 
⚡️ As a result, you can use a “parallel scan” algorithm to train these new, minimal RNNs, in parallel, taking 88% more memory but also making them 200x faster than their traditional counterparts for long sequences
 
🔥 The results are mind-blowing! Performance-wise, they go toe-to-toe with Transformers or Mamba.
 
And for Language Modeling, they need 2.5x fewer training steps than Transformers to reach the same performance! 🚀
 
🤔 Why does this matter?
 
By showing there are simpler models with similar performance to transformers, this challenges the narrative that we need advanced architectures for better performance!
 
💬 François Chollet wrote in a tweet about this paper:  
“The fact that there are many recent architectures coming from different directions that roughly match Transformers is proof that architectures aren't fundamentally important in the curve-fitting paradigm (aka deep learning)”  
“Curve-fitting is about embedding a dataset on a curve. The critical factor is the dataset, not the specific hard-coded bells and whistles that constrain the curve's shape.”
 
It’s the Bitter lesson by Richard Sutton striking again: don’t try fancy thinking architectures, just scale up your model and data!
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>