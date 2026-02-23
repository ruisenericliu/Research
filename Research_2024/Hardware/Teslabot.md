The latest Tesla Optimus video gives us a peek at their human data collection farm, which I believe is Optimus' biggest lead. What does it take to build such a pipeline? Optimus nailed all of the following:
 
1. Optimus hands are among the best 5-finger, dexterous robot hands in the world. It's got tactile sensing, 11 degrees of freedom (DOF) compared to many competitors with only 6-7 DOF, and robustness to withstand lots of object interactions without constant maintenance.
 
2. Teleoperation software: we can see that the human operators are wearing VR goggles and gloves. It is very non-trivial to set up the software to have first-person video streamed in and precise control streamed out, while maintaining extremely low latency. Humans are highly sensitive to even the smallest delay between their own motions and the robot's. Optimus has a fluid whole body controller that enacts the human poses in real-time.
 
3. Sizeable fleet: you need more than one robot to collect data in parallel, well-trained human contractors taking multiple shifts per day (preferably 24/7), and an on-call maintenance crew to make sure that the robots are always busy. That's a ton of operational complexity that academic research labs don't even think of.
 
4. Tasks & environments: it's equally important to figure out *what* to teleoperate. Currently, most such efforts are demo-driven: collect data on the tasks that you want to put into a social media video. But solving general-purpose robots requires us to think carefully about the distribution of tasks and environments. From 43"-51" in the video, we can see factory & household settings like moving batteries, handling laundry, sorting daily objects into shelves.
 
It's an open-ended research question: if you only have the budget to collect training data for 1,000 tasks, what would you pick to maximize skill transfer and generalization?
 
Closing thought: teleoperation is a necessary but insufficient condition to solve humanoid robotics. It fundamentally does not scale. More about this later.
 \> From \<[https://www.linkedin.com/feed/](https://www.linkedin.com/feed/)\>