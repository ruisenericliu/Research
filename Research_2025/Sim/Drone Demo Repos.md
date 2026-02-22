GPS Denied UAV  
[https://www.andrewbernas.com/docs/tutorials/robots/vslam/setup](https://www.andrewbernas.com/docs/tutorials/robots/vslam/setup)
 
Flight demo of a GPS-denied UAV autonomously navigating using only visual-inertial SLAM, MAVROS, and PX4. There’s no GPS module onboard. Instead, the quadcopter uses Isaac ROS VSLAM to calculate real-time position and orientation through landmark recognition and inertial odometry. In unfamiliar terrain, it builds a new map from scratch, and in known terrain, it locks onto preloaded landmarks to estimate its pose.
 
🔴 Red = recognized landmarks  
🌈 Rainbow = newly mapped features  
⚪ White = refined map
 
Every frame, the drone gets smarter.
 
Credit to Andrew Bernas. He's given us access to his Github repo which provides a complete solution for integrating visual SLAM and VIO with the Jetson Orin Nano on a PX4 UAV, enabling autonomous navigation and mapping capabilities in GPS denied environments.  
➡️ /bandofpv/VSLAM-UAV
   

Recently came across a powerful ROS 2 package that covers the essentials of simulation, sensor integration, physics, and core ROS 2 concepts.
 
I managed to get it up and running locally, and it’s been a great learning experience so far. What makes it even more exciting is that it’s already being used in real-world projects like Drona and chatDrones, which shows its practical value and community trust.
 
This has sparked some ideas, and I’m seriously thinking about building something innovative on top of it, possibly in the industrial drone space.
 
Here is the repo link: [https://lnkd.in/dMA4EQyD](https://lnkd.in/dMA4EQyD)
 
#ROS2 #Robotics #Drones #Simulation #OpenSource #LearningInPublic #ROSDevelopment
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>     

📢 New #Nav2 demo with MVSim simulator (kudos to Inhwan Wee !👏), showing how to launch 6 mobile robots, each running its own instance of Nav2. A great #ROS demo on using namespaces, multiple RViz windows, etc. Observe how each Nav2 instance sees the other robot as an obstacle as they approach and avoid each other. Recall: MVSim enables multi-robot simulation (2D, 3D LiDAR, cameras...) with inexpensive GPUs 🔥 Available for all ROS distributions.  
- Demo repo: [https://lnkd.in/dRCBMmgY](https://lnkd.in/dRCBMmgY)  
- MVSim main repo: [https://lnkd.in/dPe6T59G](https://lnkd.in/dPe6T59G)
 
#ROS2 #ROS #robotics Steve Macenski , Open Robotics
 \> From \<[https://www.linkedin.com/my-items/saved-posts/](https://www.linkedin.com/my-items/saved-posts/)\>