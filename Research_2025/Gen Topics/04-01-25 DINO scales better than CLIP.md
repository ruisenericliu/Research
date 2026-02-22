Can visual self-supervised learning (SSL) match CLIP for visual question answering (VQA)? Yes! We perform apples-to-apples comparisons between SSL and CLIP by controlling the pretraining distribution and evaluation, and obtain novel insights into the scaling behavior of SSL in this new data regime. Our major findings are:
 
1. SSL scales better with model size and data size than CLIP on a diverse range of VQA tasks, but especially on OCR/Chart VQA. This means that vision-only models can also perform well on tasks that were traditionally dominated by CLIP.  
2. SSL can learn text-sensitive features purely from web images that contain text. This suggests a deeper connection between vision and language features.  
3. Performance in classic vision tasks remains competitive. This means we are getting closer to developing vision encoders that excel at both pure vision and multimodal capabilities!  
4. Other visual SSL methods such as MAE also show similar potential! The observed scaling behavior is not unique to DINOv2.  
5. High resolution versions of Web-DINO 7B can nearly match the performance of SOTA off-shelf CLIP-family models such as SigLIP 2, despite seeing only on images.
 
tl;dr: The data matters. The success of CLIP may not be purely due to language supervision, and SSL has a lot of untapped potential.
 
It was a pleasure to co-lead this side project with [Peter Tong](https://www.linkedin.com/in/tongsbpeter/), and many thanks to [Jiachen Zhu](https://www.linkedin.com/in/jiachen-zhu-119459155/), [Koustuv Sinha](https://www.linkedin.com/in/koustuvsinha/), [Zhuang Liu](https://www.linkedin.com/in/zhuang-liu-19306b1b1/), [Xinlei Chen](https://www.linkedin.com/in/xinlei-chen-623b6a22/), [Michael Rabbat](https://www.linkedin.com/in/michael-rabbat-66a00b7/), [Nicolas Ballas](https://www.linkedin.com/in/nicolas-ballas-a188583/), [Yann LeCun](https://www.linkedin.com/in/yann-lecun/), [Amir Bar](https://www.linkedin.com/in/amirbar/), and [Saining Xie](https://www.linkedin.com/in/sainxie/) for being amazing collaborators! Special thanks to Amir, Yann, and Saining for their invaluable mentorship and guidance on the project direction! Special thanks to Mike, Koustuv, and Nicolas for supporting me to work on this side project while balancing my day-to-day responsibilities. On a personal note, this is my first first-author paper while working at Meta FAIR, and I hope to continue contributing foundational research!
 
Scaling Language-Free Visual Representation Learning  
Paper: [https://lnkd.in/gjR3pehS](https://lnkd.in/gjR3pehS)  
Website: [https://lnkd.in/gWYDPanZ](https://lnkd.in/gWYDPanZ)
 \> From \<[https://www.linkedin.com/feed/update/urn:li:activity:7313404156721909761/](https://www.linkedin.com/feed/update/urn:li:activity:7313404156721909761/)\>