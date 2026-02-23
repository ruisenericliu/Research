1. Input: Audio + RGB-D:
2. RGB-D to World – Camera Calibration, Management
3. Dialogue: Fast Whisper:
    1. [https://github.com/KoljaB/RealtimeSTT](https://github.com/KoljaB/RealtimeSTT)

4. OpenVLA, RT2 

5. GTP to Query - (GPT to PDDL)
    1. [https://huggingface.co/HuggingFaceTB/SmolLM-1.7B](https://huggingface.co/HuggingFaceTB/SmolLM-1.7B) ?
    2. [https://huggingface.co/docs/transformers/en/model_doc/llama3](https://huggingface.co/docs/transformers/en/model_doc/llama3)
6. Query to Detection – GroundedDINO: Owl-ViT
    1. [https://github.com/IDEA-Research/GroundingDINO](https://github.com/IDEA-Research/GroundingDINO)
7. Detection to Segmentation (SAM, nanoSAM?)
    1. [https://github.com/IDEA-Research/GroundingDINO](https://github.com/IDEA-Research/GroundingDINO);
8. Segmentation to Validation - (CLIP)
    1. [https://huggingface.co/docs/transformers/en/model_doc/clip](https://huggingface.co/docs/transformers/en/model_doc/clip)
9. Validation to Human Feedback
    1. TBD
10. Detection to Grasp – Logic + GrConvNet
    1. [https://github.com/skumra/robotic-grasping](https://github.com/skumra/robotic-grasping)
    2. [https://nvlabs.github.io/FoundationPose/](https://nvlabs.github.io/FoundationPose/)
11. Grasp to Motion Planning – MoveIT + CuMotion
12. Adaptive behavior + Safety – nvblox
13. Robot Improvement – LFD (ACT or Diffusion Policy – Hugging Face; 16 demos)
    1. LeRobot: [https://github.com/huggingface/lerobot](https://github.com/huggingface/lerobot)    
𝐌𝐚𝐣𝐨𝐫 release of NVIDIA Robotics Isaac ROS 3.0, only 6 months after their 2.0 release, this is a very large update to the public. Lot's of GPU accelerated tools for real-time robotics use cases. My top pics:
 
✅ Multi-camera support for: nvBlox (first video), the Nova Orin Dev Kit with visual odometry (picture) 📷
 
✅ Release of Isaac Manipulator stack, includes real-time motion planner(cuMution), nvblox and a DNN Stereo depth model. 🦾
 
✅ A BUNCH of documentation updates, it's incredible high quality, both in the repositories as in a separate github.io read-the-docs website. 📖
 
✅ Open Source release of FoundationPose, running at 14FPS tracking on a Orin Nano 8GB 😮 (last video)
 
The extent to which NVIDIA is creating & open sourcing its software for vision guided robotics is huge, may I say, the largest I know of.
 
Announcement: [https://lnkd.in/ev6EWGq8](https://lnkd.in/ev6EWGq8)