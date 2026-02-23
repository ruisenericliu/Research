Robots are deployed for long periods of time, but how can they answer questions and generate goals based on their long-horizon history?
 
At my internship at [NVIDIA](https://www.linkedin.com/company/nvidia/), we built ReMEmbR, a retrieval-augmented memory for embodied robots!
 
People interacting with robots may want to ask questions like where something happened, when it occurred, or how long ago it took place, which would require the robot to reason over a long history of their deployment. A long-context VLM would not be able to process potentially unbounded robot histories. We split the problem into a memory building and querying phase
 
During the memory building phase, we use NVIDIA’s VILA to caption the robot’s history in real time, and aggregates position, time, and caption information in a vector database.
 
Then, when a user asks a question, ReMEmbR’s querying phase iteratively calls functions that query the vector database based on text, time, or position. This allows ReMEmbR to correct itself or answer more difficult questions that require multiple steps of reasoning.
 
To evaluate ReMEmbR, we introduce the Navigation Video Question Answering (NaVQA) dataset. This evaluation dataset consists of 210 spatial, temporal, and descriptive questions across different lengths of time.
 
We found that ReMEmbR can answer all sorts of questions such as “How long were you in the building” or “Take me somewhere with a nice view”. We also found in our paper that ReMEmBR performs faster than simply running a VLM, and performs better as the length of time increases!
 
I would like to thank my collaborators: [John Welsh](https://www.linkedin.com/in/john-welsh-213126183/), [Joydeep Biswas](https://www.linkedin.com/in/joydeep-biswas-1579568/), [Yan Chang](https://www.linkedin.com/in/yanchang1/), and [Soha Pouya](https://www.linkedin.com/in/sohapouya/). Also we got a lot of great help from [Dustin Franklin](https://www.linkedin.com/in/dustin-franklin-b3aaa173/), [Yao (Jason) Lu](https://www.linkedin.com/in/yao-jason-lu-a0291938/), [Khannah Shaltiel](https://www.linkedin.com/in/khannah-shaltiel/), and many others!   Website: [https://lnkd.in/gfDdHa3X](https://lnkd.in/gfDdHa3X)  
Paper: [https://lnkd.in/g2k9eN-8](https://lnkd.in/g2k9eN-8)  
GitHub: [https://lnkd.in/gjar5h26](https://lnkd.in/gjar5h26)
 
Take a look at the video below, and the technical blog post, which incorporates a lot of information on how to replicate the setup yourself!
 \> From \<[https://www.linkedin.com/feed/update/urn:li:activity:7244102539275599873/](https://www.linkedin.com/feed/update/urn:li:activity:7244102539275599873/)\>