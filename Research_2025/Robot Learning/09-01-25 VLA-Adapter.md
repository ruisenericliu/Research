Most VLAs glue a policy onto a giant VLM—slow to train, high latency, pricey.  
This paper freezes a tiny 0.5 billion parameter VLM and adds a tiny action decoder that bridges perception→control, wired layer-by-layerlike a feature pyramid for fast, long-horizon control.
 
VLA-Adapter introduces a clever "bridge" system that efficiently connects visual understanding to robotic actions using just a tiny 0.5 billion parameter model—roughly 100x smaller than typical solutions. Think of it as finding the perfect translator between what a robot sees and what it should do, without needing to teach it everything from scratch.
 
This approach achieves state-of-the-art performance while training in just 8 hours on a single consumer GPU (the kind you might have in a gaming computer). That's a reduction from months of training on expensive server farms to less than a workday on accessible hardware.
 
[https://arxiv.org/pdf/2509.09372](https://arxiv.org/pdf/2509.09372)