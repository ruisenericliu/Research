![Exported image](Exported%20image%2020260222122710-0.png)   
[https://docs.google.com/presentation/d/1owkm5zu-M3rPk5DuRhSmIocpuYKlCG5vNa8GQPfdrx8/edit?slide=id.g35cdb022ec8_0_87#slide=id.g35cdb022ec8_0_87](https://docs.google.com/presentation/d/1owkm5zu-M3rPk5DuRhSmIocpuYKlCG5vNa8GQPfdrx8/edit?slide=id.g35cdb022ec8_0_87#slide=id.g35cdb022ec8_0_87)
   

Annotating image has never easier nor faster ⚡. Checkout the new Open-source labelling tool VisioFirm, Install it via a simple `pip install visiofirm` and run `visiofirm` in your terminal.
 
VisioFirm is an AI-powered image annotation tool designed to accelerate labeling for computer vision tasks like object detection, oriented bounding boxes (OBB), and segmentation. Built for speed and simplicity, it leverages state-of-the-art models (YOLO series from Ultralytics and GroundingDINO from IDEA-Research) for semi-automated pre-annotations, allowing you to focus on refining rather than starting from scratch therefore reducing human-in-the-loop effort. Whether you're preparing datasets for detection or segmentation, VisioFirm can help streamlining the workflow and speedup the labelling up to 80% or even more depending on the complexity of the dataset.
 
For the backend, we have implemented a new post-processing that uses CLIP for label disambiguation and graph-based clustering for label redundancy management. In the frontend, you get all the options already given by the other tools, in addition to single click SAM-based mask generation accelerated via webgpu.
 
For integration easiness, we have options such as importing partially labelled data if have started with another tool already. You can import a zip or a folder to the app with the COCO / YOLO formats and the VisioFirm manages to pre-consider the already labelled images.
 
MORE TO COME:  
The Github will be maintained and will include new options further down. So stay in touch.
 
Test by yourself the app and get more details in the arxiv report.
 
Arxiv: [https://lnkd.in/eHf62ATv](https://lnkd.in/eHf62ATv)  
Github: [https://lnkd.in/ebxrn9hj](https://lnkd.in/ebxrn9hj)
 
#ImageAnnotation #DataLabeling #ComputerVision #AI #ObjectDetection #InstanceSegmentation #OrientedBoundingBoxes  
#VisioFirm #YOLO #GroundingDINO #SegmentAnything #SAM
   

FineVision: [https://huggingface.co/spaces/HuggingFaceM4/FineVision](https://huggingface.co/spaces/HuggingFaceM4/FineVision)