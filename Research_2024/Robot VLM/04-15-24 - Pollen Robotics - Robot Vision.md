Last week we released our open-source library pollen-vision on [Hugging Face](https://www.linkedin.com/company/huggingface/). It is a collection of zero-shot computer vision models we chose for their applicability in robotics. With just an RGBD camera and pollen-vision, you can estimate the 3D position of unknown objects only needing very few lines of code.
 
Check out this demo of a grasping behavior we built using pollen-vision. How did it work?
 
- we prompted the cv models using text, like "mug", or "blue plate".
 
- out of the pipeline, we got segmentation masks of the detected objets, which allows us to segment the depth map too  
- averaging the depth in the mask yields an accurate z position of the object
 
combined with the camera's intrinsic parameters, we compute the (x, y, z) position of the object in camera space, and…
 
Voilà, Reachy grasps the objects 🙂
 
[Pollen Robotics](https://www.linkedin.com/company/pollen-robotics/) [hashtag#opensource](https://www.linkedin.com/feed/hashtag/?keywords=opensource&highlightedUpdateUrns=urn%3Ali%3Aactivity%3A7181234800102383617)