SAM: [https://arxiv.org/abs/2304.02643](https://arxiv.org/abs/2304.02643)￼Blog: [https://segment-anything.com/](https://segment-anything.com/)
 
Note: SAM-HQ here: [https://paperswithcode.com/paper/segment-anything-in-high-quality](https://paperswithcode.com/paper/segment-anything-in-high-quality)
 ![Exported image](Exported%20image%2020260222122739-0.png)   
In this work, our goal is to build a foundation model for  
image segmentation. That is, we seek to develop a prompt-  
able model and pre-train it on a broad dataset using a task  
that enables powerful generalization
 
The success of this plan hinges on three components:  
task, model, and data. To develop them, we address the  
following questions about image segmentation:
 
1. What task will enable zero-shot generalization?  
2. What is the corresponding model architecture?  
3. What data can power this task and model?
 
SAM is more about data engine building than anything :  
assisted-manual, semi-automatic, and fully automatic
 ![Exported image](Exported%20image%2020260222122741-1.png)  

Image encoder. Motivated by scalability and powerful pre-  
training methods, we use an MAE [47] pre-trained Vision  
Transformer (ViT) [33] minimally adapted to process high  
resolution inputs [62]. The image encoder runs once per  
image and can be applied prior to prompting the model.
 
Prompt encoder. We consider two sets of prompts: sparse  
(points, boxes, text) and dense (masks). We represent  
points and boxes by positional encodings [95] summed with  
learned embeddings for each prompt type and free-form text  
with an off-the-shelf text encoder from CLIP [82]
 
Mask decoder. The mask decoder efficiently maps the im-  
age embedding, prompt embeddings, and an output token  
to a mask. This design, inspired by [14, 20], employs a  
modification of a Transformer decoder block [103] followed  
by a dynamic mask prediction head. Our modified decoder  
block uses prompt self-attention and cross-attention in two  
directions (prompt-to-image embedding and vice-versa) to  
update all embedding
 
Resolving ambiguity. With one output, the model will av-  
erage multiple valid masks if given an ambiguous prompt.  
To address this, we modify the model to predict multiple  
output masks for a single prompt (see Fig. 3). We found  
**3 mask outputs is sufficient to address most common cases**  
**(nested masks are often at most three deep: whole, part, and**  
**subpart**