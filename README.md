# Real Time Sheep/Lamb Detection using YoloV3 and OpenCV

## Introduction

Real-Time Object Detection using YoloV3 has been one of the favorites techniques used by researchers and developers working in Computer Vision, reportedly, because it's very fast and accurate compared to other Object Detection Systems such as SSD513, R-FCN, RetinaNet, etc (Fig. 1).

<figure class="image">
  <img src="https://miro.medium.com/max/4800/1*FvKNwDBc6gMSKJJoL3dAhA.png" alt="{{ include.description }}">
  <figcaption>Figure 1: Comparison of Inference time between YOLOv3 with other systems on COCO dataset <a href="https://pjreddie.com/media/files/papers/YOLOv3.pdf">Source</a></figcaption>
</figure>

## Project preparation
### Dataset
A dataset of ≈ 5800 images was prepared to train the model, mostly scraped from Google and Bing, in addition to some frames extracted from video footages.

### Tools

#### Image scraping
* Google: <a href="https://chrome.google.com/webstore/detail/download-all-images/ifipmflagepipjokmbdecpmjbibjnakm?hl=en">Download All Images</a>  Chrome extension 
* Bing:  <a href="https://pypi.org/project/bing-image-downloader/">bing image downloader</a> 
* Video Frame Extractor using openCV.     

#### Image Labeling
I ended up labeling about 60% of the dataset (it took me a serious time to finish that far). 
* <a href="https://github.com/Cartucho/OpenLabeling">OpenLabeling</a> tool was used.

## Model Training
Due to lack of computing resources the model training was executed on Google Colab. Training has been run using a modified version of <a href="https://github.com/AlexeyAB/darknet#how-to-train-to-detect-your-custom-objects">Darknet</a> by AlexeyAB.
The hardware specification provided in Google Colab environment are <a href="https://colab.research.google.com/drive/151805XTDg--dgHb3-AXJCpnWaqRhop_2">(source)</a>

<figure class="image">
  <img src="https://blog.ibanyez.info/download/B20190410T000000072.png" alt="{{ include.description }}">
  <figcaption>Figure 2: YoloV3 configuration files for Darkent on Colab notebook.</figcaption>
</figure>

## Results