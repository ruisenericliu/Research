For robot dexterity, a missing piece is general, robust perception. Our new Science Robotics article combines multimodal sensing with neural representations to perceive novel objects in-hand. See it on the cover of the November issue! [https://lnkd.in/ezZRs5dN](https://lnkd.in/ezZRs5dN)
 
We estimate pose and shape by learning neural field models online from a stream of vision, touch, and proprioception. The frontend achieves robust segmentation and depth prediction for vision and touch. The backend combines this information into a neural field, while also optimizing for pose.
   

Vision-based touch ([digit.ml/digit](http://digit.ml/digit)) perceives contact geometries as images, and we train an image-to-depth tactile transformer in simulation.
 
For visual segmentation, we combine powerful foundation models (SAMv1) with robot kinematics.
 
It doubles up as a multimodal pose tracker, when provided CAD models of the objects at runtime.
 
For different levels of occlusion, we find that “touch, at the very least, refines and, at the very best, disambiguates visual estimates during in-hand manipulation."
 
We release a large dataset of real-world and simulated visuo-tactile interactions and tactile transformer models on Hugging Face: [bit.ly/hf-neuralfeels](http://bit.ly/hf-neuralfeels)
 
This has been in the pipeline for a while, thanks to my amazing collaborators from [AI at Meta](https://www.linkedin.com/company/aiatmeta/), [Carnegie Mellon University](https://www.linkedin.com/company/carnegie-mellon-university/), [University of California, Berkeley](https://www.linkedin.com/company/uc-berkeley/), [Technische Universität Dresden](https://www.linkedin.com/company/tu-dresden/), and [CeTI](https://www.linkedin.com/company/centrefortactileinternet/): [Haozhi Qi](https://www.linkedin.com/in/haozhi-qi-24031491/), [Tingfan Wu](https://www.linkedin.com/in/tingfan-wu-5359669/), [Taosha F.](https://www.linkedin.com/in/taosha-f-1b4090161/), [Luis Pineda](https://www.linkedin.com/in/lpineda-fb/), [Mike Maroje Lambeta](https://www.linkedin.com/in/mike-maroje-lambeta/), [Jitendra MALIK](https://www.linkedin.com/in/jitendra-malik-60b55823b/), [Mrinal Kalakrishnan](https://www.linkedin.com/in/mrinalkalakrishnan/), [Roberto Calandra](https://www.linkedin.com/in/rcalandra/), [Michael Kaess](https://www.linkedin.com/in/michaelkaess/), [Joseph Ortiz](https://www.linkedin.com/in/joseph-ortiz-620709130/), and [Mustafa Mukadam](https://www.linkedin.com/in/mhmukadam/)
 
Paper: [https://lnkd.in/ezZRs5dN](https://lnkd.in/ezZRs5dN)  
Project page: [https://lnkd.in/dCPCs4jQ](https://lnkd.in/dCPCs4jQ)
 \> From \<[https://www.linkedin.com/feed/update/urn:li:activity:7262549149726732289/](https://www.linkedin.com/feed/update/urn:li:activity:7262549149726732289/)\>