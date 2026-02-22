🚀 Introducing GraspMolmo: Generalizable Task-Oriented Grasping via Large-Scale Synthetic Data
 
How should a robot grasp a knife? Well, it depends—to chop or to hand it over?
 
GraspMolmo bridges that semantic gap by fusing spatial reasoning and language understanding to predict task-appropriate grasps from natural language and a single RGB-D frame.
 
🛠 How to Use GraspMolmo
 
1️⃣ Build PRISM  
• 379k samples, 2,356 objects, 10k scenes  
• Uses ShapeNet-Sem + ACRONYM grasps  
• Tasks paired via GPT-4o + human filtering
 
2️⃣ Fine-Tune Molmo  
• Trained on PRISM + TaskGrasp-Image  
• Grasp described using natural language + pixel-level grounding
 
3️⃣ Run Inference  
• Input: RGB-D image + task prompt  
• Output: Task-aware pixel → 6-DoF grasp proposal
 
4️⃣ Deploy in Real World  
• Example: “dump flowers out” → correctly grasps vase edge, not body
 
Project: [https://lnkd.in/g94nsd2a](https://lnkd.in/g94nsd2a)