✨ICLR 2024 Spotlight✨
 
Still hand-labeling phases or tuning GANs with your trajectories? We propose FLD, a self-supervised representation method that extracts spatial-temporal relationships in high-dimensional trajectories. RL policies informed by FLD show extended generality.
 
The availability of reference trajectories has significantly propelled the advancement of motion learning techniques. How do we efficiently represent these high-dimensional, long-horizon, highly nonlinear signals such that downstream learning tasks can generalize better?
 
Fourier Latent Dynamics (FLD) achieves so by featuring dynamics in a continuously parameterized latent space. The latent encodings consist of a varying component (phi) that indicates local time indices and an invariant component (theta) that represents global motion features.
 
Each motion (or any other quasi-periodic signal) induces a ring in the latent manifold, where the radius denotes the invariant high-level features, and the angle denotes the current frame of that motion. This way, with a few parameters, FLD is able to represent diverse, theoretically infinitely long motion trajectories or any other quasi-periodic signal.
 
The open-loop reconstruction of FLD by consecutively propagating the latent dynamics and decoding to the state space demonstrates high fidelity on test data unseen during training, compared with less structured models, including FF networks and Periodic Autoencoders (PAE).
 
With such an efficient latent representation, we train a downstream tracking policy with RL. A motion is sampled at each episode. Its latent phase propagates through time while the high-level features stay constant. The tracking reward is computed for each step with reconstruction.
 
This structure enables real-time motion tracking. During inference, FLD encodes real-time motion input as tracking targets, irrespective of their periodic or quasi-periodic nature.
 
FLD provides a fallback mechanism with anomaly detection from its autoencoder nature. When a potentially risky target is proposed, FLD rejects the input and resorts to a safe motion by propagating the latent dynamics with the previous parameters.
 
This work has been published at [ICLR](https://www.linkedin.com/company/iclr/) 2024 by the Biomimetic Robotics Lab [MIT Department of Mechanical Engineering (MechE)](https://www.linkedin.com/company/mit-meche/) [Massachusetts Institute of Technology](https://www.linkedin.com/company/mit/). It will be presented as a spotlight paper in May in Vienna, Austria.
 
Authors  
[Chenhao Li](https://www.linkedin.com/in/ACoAADE97wgB6ANG9s3sNy-CWeE8qTQloGahIAE),  
[Elijah Stanger-Jones](https://www.linkedin.com/in/ACoAAB8h9jIBsaXBu1mL2kKlyUUDTOExyhSsW7k),  
Steve Heim,  
[Sangbae Kim](https://www.linkedin.com/in/ACoAAAGu49ABC-ucSSBVWVWop1UVBvm0vBdnAcs)
 
Paper  
[https://lnkd.in/eGaR2QfY](https://lnkd.in/eGaR2QfY)  
Project  
[https://lnkd.in/e43jfRBv](https://lnkd.in/e43jfRBv)  
Code  
[https://lnkd.in/evcYHjra](https://lnkd.in/evcYHjra)  
Videos  
[https://lnkd.in/e7KGz9Yz](https://lnkd.in/e7KGz9Yz)
 \> From \<[https://www.linkedin.com/posts/chenhao-li-86080b1b0_ai-representationlearning-reinforcementlearning-activity-7166894966395379712-kcGu/?utm_source=share&utm_medium=member_android](https://www.linkedin.com/posts/chenhao-li-86080b1b0_ai-representationlearning-reinforcementlearning-activity-7166894966395379712-kcGu/?utm_source=share&utm_medium=member_android)\>