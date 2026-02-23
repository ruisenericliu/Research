Introducing Diffusion Transformer Block Policies, a sota architecture that outperforms ACT and Diffusion Policies by 20%, needs no hyperparam tuning, scales with model size and data, and enables dexterous long horizon bimanual tasks like sushi cutting! 🍣  
So what are the ingredients for a scalable diffusion transformer policy? It turns out that adding custom adaptive Layer Norm (adaLN) to the attention block is key to stabilizing training. Together with efficient obs tokenization this provides a big boost! 📈  
We release all our code, checkpoints and our BiPlay dataset, which consists of 10 hours of diverse, long horizon bimanual dexterous tasks with an ALOHA robot including language annotations!
 
Project: [https://lnkd.in/gNgC-Sur](https://lnkd.in/gNgC-Sur)  
Paper: [https://lnkd.in/gAhxpP2j](https://lnkd.in/gAhxpP2j)  
Code: [https://lnkd.in/gS6k6-Xe](https://lnkd.in/gS6k6-Xe)
 
This was a wonderful collaboration with rockstars [Sudeep Dasari](https://www.linkedin.com/in/sudeep-dasari-032997149/) who interned at [Berkeley Artificial Intelligence Research](https://www.linkedin.com/company/bair-lab/) with us and led the project, Sebastian Zhao, Mohan Srirama and [Sergey Levine](https://www.linkedin.com/in/sergey-levine-5a31a24/).
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>