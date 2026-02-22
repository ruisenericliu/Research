This week I was working with NVIDIA Isaac GR00T 🤖 and I realised that most of the robots don't have their data in groot_lerobot format 🤔 which is needed to finetune the model.
 
So I fixed that problem (kind of) ✅, I made a new repository to quickly convert any ROS2 robot's ROS2 bags into groot_lerobot dataset! 📂➡️📊
 
All you need now is to have ROS2 topics for the following:  
1️⃣ Image topic with RGB image 📸  
2️⃣ Joint states topic of the robot 🦾  
3️⃣ Joint command topic, which sends actions to the robot 🕹️  
4️⃣ Task description topic, which defines what task to perform 📝
 
Now quickly record ROS2 bags of your robot doing some cool things 😎 and convert them to groot_lerobot and train! With a good enough GPU you can train it in a day! 🚀💨
 
I don't have a big VRAM GPU so I had to train it on my laptop GPU which can use the system RAM and VRAM 💻 and it took me 3 whole days to get some good results. 👍⏳
 
OH! And I also made a basic Isaac Sim connector so that I can make my simulated robots run with GR00T 🎮🔗. I get it for so-arm100 robot by LeRobot ( awesome repo! 🙌 ) but it can be adopted to any robot.
   

I hope this makes adding GR00T to your project a little easier! 😊🎉
    
ros2bag_lerobot: [https://lnkd.in/gsixTpxR](https://lnkd.in/gsixTpxR)  
Isaac_Groot: [https://lnkd.in/g5_E6-WZ](https://lnkd.in/g5_E6-WZ)  
lerobot: [https://lnkd.in/gdB7JyuU](https://lnkd.in/gdB7JyuU)
 
#Nvidia #Groot #ros2 #robotics #lerobot #huggingface  
NVIDIA Hugging Face
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>