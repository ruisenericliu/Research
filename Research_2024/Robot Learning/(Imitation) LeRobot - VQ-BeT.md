Generative modeling of complex behaviors from labeled datasets has been a longstanding problem in decision-making. Unlike language or image generation, decision-making requires modeling actions – continuous-valued vectors that are multimodal in their distribution, potentially drawn from uncurated sources, where generation errors can compound in sequential prediction. A recent class of models called Behavior Transformers (BeT) addresses this by discretizing actions using k-means clustering to capture different modes.
 
However, k-means struggles to scale for high-dimensional action spaces or long sequences and lacks gradient information, and thus BeT suffers in modeling long-range actions. In this work, we present Vector-Quantized Behavior Transformer (VQ-BeT), a versatile model for behavior generation that handles multimodal action prediction, conditional generation, and partial observations. VQ-BeT augments BeT by tokenizing continuous actions with a hierarchical vector quantization module. Across seven environments including simulated manipulation, autonomous driving, and robotics, VQ-BeT improves on state-of-the-art models such as BeT and Diffusion Policies. Importantly, we demonstrate VQ-BeT’s improved ability to capture behavior modes while accelerating inference speed 5× over Diffusion Policies.
 \> From \<[https://sjlee.cc/vq-bet/](https://sjlee.cc/vq-bet/)\>     

Prediction on a finite number of tokens gives an advantage for multi-modal conditions
 ![Exported image](Exported%20image%2020260222202903-0.png)  

Historically, z(x) is still Gaussian, like an VAE  
However, VQ-Bet wants z(x) to be discrete - hence, vector quantization
 
BeT:

![Exported image](Exported%20image%2020260222202905-1.png)  

Note: must use a residual VQ encoder and Decoder - took from Audio Generation Literature ( a high freq domain)

![Exported image](Exported%20image%2020260222202906-2.png)   
2 Layers of quantization

![Exported image](Exported%20image%2020260222202908-3.png)  

Loss function:

![Exported image](Exported%20image%2020260222202909-4.png)  

More expressive distribution with 2 layers of quantization:

![Exported image](Exported%20image%2020260222202911-5.png)  

From Behavior Transformers:
 ![Exported image](Exported%20image%2020260222202915-6.png)

Code Predictor is given an offset head to allow for adjustment
 ![Exported image](Exported%20image%2020260222202916-7.png)

Then add goal sequence at high level to observation sequences
    ![Exported image](Exported%20image%2020260222202917-8.png)   ![Exported image](Exported%20image%2020260222202918-9.png)  

Counting Demos:

![Exported image](Exported%20image%2020260222202920-10.png)        
![Exported image](Exported%20image%2020260222202922-11.png)  
![Exported image](Exported%20image%2020260222202923-12.png)

￼Use higher attention size if you want your actions to be smoother
 ![Exported image](Exported%20image%2020260222202927-13.png)  

Not so important:

![Exported image](Exported%20image%2020260222202928-14.png)  
![Exported image](Exported%20image%2020260222202929-15.png)  

Q/A:
 
Diffusion policy is better for fine actions;
 
Distracted, work;