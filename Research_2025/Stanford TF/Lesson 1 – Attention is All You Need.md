June, 2017  
[https://arxiv.org/pdf/1706.03762](https://arxiv.org/pdf/1706.03762)
 
The illustrated transformer: [https://jalammar.github.io/illustrated-transformer/](https://jalammar.github.io/illustrated-transformer/)
 
The annotated transformer: [http://nlp.seas.harvard.edu/annotated-transformer/](http://nlp.seas.harvard.edu/annotated-transformer/)
    
**Abstract**:

1. Dominant sequence transduction models are based on Recurrent or Convolutional Neural Networks
2. Encoder and Decoders are connected through an attention mechanism
3. Show that RNN and CNN are unnecessary for language
 
1 Introduction
 
1. RNNs have **no parallelism** - Recurrent models define a hidden state as a function of previous hidden states and position t,
2. Attention allows dependency modeling regardless of distance
3. 2021 SOTA, 12 hours on 8 P100 GPUs
 
2 Background
 
1. Transformers make relation learning linear, and use **Multi-Head Attention** (Section 3.2) to alleviate costs from average weighting  
2. **Self-attention** – relating different positions of a single sequence, to compute a representation of a sequence
 
3 Model Architecture
 
Maps an input sequence of symbol representations (x1, ..., xn) to a sequence  
of continuous representations z = (z1, ..., zn). Given z, the decoder then generates an output sequence (y1, ..., ym) of symbols one element at a time
 
At each step the model is auto-regressive [10], **consuming the previously generated symbols as additional input**
 ![Exported image](Exported%20image%2020260222122830-0.png)      ![Exported image](Exported%20image%2020260222122831-1.png)   ![Exported image](Exported%20image%2020260222122834-2.png)      
**Encoder**: 6 layers. The output of each sub-layer is LayerNorm(x + Sublayer(x)), where Sublayer(x) is the function implemented by the sub-layer itself.
 
**Decoder**: In addition to the two sub-layers in each encoder layer, the decoder inserts a third sub-layer, which performs multi-head attention over the output of the encoder stack
 
We also modify the self-attention sub-layer in the decoder stack to prevent positions from attending to subsequent position
 
**3.2** **Attention**
 
Q: Query, K – Key, V – Value; Multi-headed is just several running in parallel
 
Query: Current embedding  
Key: Descriptors for the other embeddings  
(QK focuses on cross token relations)  
Value: focuses on position (best match)
 
In decoding, K,V comes from the encoder (the source sequence)  
Whereas Q comes from the decoder (target sequence --\> but we mask as we go)
 
Used in:
 
1. Encoder-decoder attention layers

**Query comes from previous decoder layer**  
Memory Key/Value comes from output of the encoder  
**Thus every position in the decoder can attend to all positions in the input sequence**

2. Encoder Self-Attention Layers
    1. Keys/Values/Queries come from the same place – output of the previous layer
    2. Each position in the encoder can attend to all positions in the previous layer
3. Decoder Self-Attention
    1. Attend to all positions in the decoder in the previous layer
    2. Prevent leftward information flow
        1. Mask out (setting to –inf) all values in the input of the softmax which correspond to illegal positions
   
![Exported image](Exported%20image%2020260222122835-3.png)  

Say we’re calculating the self-attention for the first word in this example, “Thinking”. We need to score each word of the input sentence against this word. The score determines how much focus to place on other parts of the input sentence as we encode a word at a certain position.
 
The **third and fourth steps** are to divide the scores by 8 (the square root of the dimension of the key vectors used in the paper – 64. This leads to having more stable gradients. There could be other possible values here, but this is the default), then pass the result through a softmax operation. Softmax normalizes the scores so they’re all positive and add up to 1.
 
The **fifth step** is to multiply each value vector by the **softmax** score (in preparation to sum them up). The intuition here is to keep intact the values of the word(s) we want to focus on, and drown-out irrelevant words (by multiplying them by tiny numbers like 0.001, for example).

![Understanding the Softmax Activation Function A .....](Exported%20image%2020260222122836-4.png)  

The **sixth step** is to sum up the weighted value vectors. This produces the output of the self-attention layer at this position (for the first word).
 ![Exported image](Exported%20image%2020260222122837-5.png)     
![Exported image](Exported%20image%2020260222122838-6.png) ![Exported image](Exported%20image%2020260222122842-7.png)  
![Exported image](Exported%20image%2020260222122843-8.png)      ![Exported image](Exported%20image%2020260222122844-9.png) ![Exported image](Exported%20image%2020260222122844-10.png)  

**How do we do that? We concat the matrices then multiply them by an additional weights matrix WO.**
 ![Exported image](Exported%20image%2020260222122845-11.png)     

3.3 Position wise feed-forward network

1. Each layer of encoder and decoder containers a fully connected feed forward layer, with ReLU activation in between
 ![Exported image](Exported%20image%2020260222122847-12.png)     

3.4 Embeddings and Softmax
 
1. Convert input tokens to vector of dimension d-model
2. Same for decoder output to next-token probabilities
 
3.5 Positional Encoding

1. Must inject information about relative or absolute position of the tokens in the sequence
2. Has same dimensions as d-model
3. IN this work, use sin/cosine functions
 ![Exported image](Exported%20image%2020260222122849-13.png)  

Pos is the position, i is the dimension; Geometric progression from 2pi to 10k*2pi
 ![Exported image](Exported%20image%2020260222122852-14.png)  

Deocder difference:
   
![Exported image](Exported%20image%2020260222122853-15.png)   
**FINAL** **LAYER**:
 
Let’s assume that our model knows 10,000 unique English words (our model’s “output vocabulary”) that it’s learned from its training dataset. This would make the logits vector 10,000 cells wide – each cell corresponding to the score of a unique word. That is how we interpret the output of the model followed by the Linear layer.
       
**4 Why Self Attention**
 
**1.** Total computational complexitiy per layer  
2. Parallelizable computation  
3. Path length between long-range dependencies in the network
 ![Exported image](Exported%20image%2020260222122854-16.png)   
**5. Training**
 
1. English/German Translation  
2. 8 P100 GPUs; 300k steps  
3. Adam optimizer
 
Residual Dropout We apply dropout [ 33] to the output of each sub-layer, before it is added to the  
sub-layer input and normalized. In addition, we apply dropout to the sums of the embeddings and the  
positional encodings in both the encoder and decoder stacks. For the base model, we use a rate of  
Pdrop = 0.1.
   
![Exported image](Exported%20image%2020260222122856-17.png)     

Now, because the model produces the outputs one at a time, we can assume that the model is selecting the word with the highest probability from that probability distribution and throwing away the rest. That’s one way to do it (called greedy decoding). Another way to do it would be to hold on to, say, the top two words (say, ‘I’ and ‘a’ for example), then in the next step, run the model twice: once assuming the first output position was the word ‘I’, and another time assuming the first output position was the word ‘a’, and whichever version produced less error considering both positions #1 and #2 is kept. We repeat this for positions #2 and #3…etc. This method is called “beam search”, where in our example, beam_size was two (meaning that at all times, two partial hypotheses (unfinished translations) are kept in memory), and top_beams is also two (meaning we’ll return two translations). These are both hyperparameters that you can experiment with.