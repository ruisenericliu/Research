[https://ai.meta.com/sam2/](https://ai.meta.com/sam2/)
 
[https://arxiv.org/abs/2408.00714](https://arxiv.org/abs/2408.00714)
 ![Exported image](Exported%20image%2020260222122735-0.png)   
While SA successfully addresses segmentation in images, existing video segmentation models  
and datasets fall short in providing a comparable capability to “segment anything in videos
 
When applied to images, the memory is empty and the model behaves like SAM  
￼Data engine: targeted to provide training data for segmenting any object with a valid boundary, including parts and subparts.
 
Data set: Our final Segment Anything Video (SA-V) dataset (§5.2) consists of 35.5M masks across 50.9K videos, 53× more  
masks than any existing video segmentation datas
 
Spatially, the model behaves similarly to SAM. **A promptable and light-weight mask**  
**decoder takes an image embedding and prompts (if any) and outputs a segmentation mask for the frame**.  
Prompts can be iteratively added on a frame in order to refine the masks.
 
The frame embedding used by the SAM 2 decoder is not directly from an image encoder and is instead  
conditioned on memories of past predictions and prompted frames. It is possible for prompted frames to also  
come “from the future” relative to the current frame. Memories of frames are created by the memory encoder  
based on the current prediction and placed in a memory bank for use in subsequent frames. The memory  
attention operation takes the per-frame embedding from the image encoder and conditions it on the memory  
bank, before the mask decoder ingests it to form a prediction
 ![Exported image](Exported%20image%2020260222122736-1.png)  

Memory attention: We stack L transformer blocks, the first one taking the image encoding from the current frame as input
 
Our decoder design largely follows SAM. We stack “two-way” transformer blocks that update prompt and  
frame embeddings. As in SAM, for ambiguous prompts (i.e., a single click) where there may be multiple  
compatible target masks, we predict multiple masks. This design is important to ensure that the model  
outputs valid masks. In video, where ambiguity can extend across video frames, the model predicts multiple  
masks on each frame. If no follow-up prompts resolve the ambiguity, the model only propagates the mask  
with the highest predicted IoU for the current frame.
 
Unlike SAM where there is always a valid object to segment given a positive prompt, in the PVS task it is  
possible for no valid object to exist on some frames (e.g. due to occlusion). **To support this new output**  
**mode, we add an additional head** that predicts whether the object of interest is present on the current frame.  
Another **novelty are skip connections from our hierarchical image encoder** (bypassing the memory attention)  
to incorporate high-resolution embeddings for mask decoding (see §D).
 
e memory encoder generates a memory by downsampling the output mask using  
a convolutional module and summing it element-wise with the unconditioned frame embedding from the  
image-encoder (not shown in Fig. 3)
   

Memory bank. maintaining a FIFO queue of memories of up to N recent frames and stores information from prompts  
For instance, in the VOS task where the initial mask is the  
only prompt, the memory bank consistently retains the first frame’s memory along with memories of up to N  
recent (unprompted) frames.
 
In addition to the spatial memory, we store a list of object pointers as lightweight vectors for high-level  
semantic information of the object to segment, based on mask decoder output tokens of each frame.
 
Our memory attention cross-attends to both spatial memory features and these object pointers.
   

Data engine:  
Phase 1: SAM per frame  
Phase 2: SAM + SAM2 Mask --- SAM2 only accepts mask as prompts - temporarily propagate masklets  
Phase 3: SAM2 - fully utilize SAM2 refinement
 ![Exported image](Exported%20image%2020260222122737-2.png)  

Automated masklets:  
To generate auto masklets, we prompt  
SAM 2 with a regular grid of points in the first frame and generate candidate masklets. These are then sent  
to the masklet verification step for filtering. Automatic masklets tagged as “satisfactory” are added to the  
SA-V dataset. Masklets identified as “unsatisfactory” (i.e., model failure cases) are sampled and presented to  
annotators to refine with SAM 2 in the loop (Phase 3 of the data engine)