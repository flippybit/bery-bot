# Region Based Convolutional Neural Networks
Region-based Convolutional Neural Networks are a family of machine-learning models for computer-vision specifically object detection and segmentation.  

## Overview of Mask R-CNN
Mask R-CNN is a two stage framework: 
1.  The first stage scans the image and generates proposals(areas likely to contain an object).  
2.  Second stage classifies the proposals and generates bounding boxes and masks.

```{figure} ../imgs/cv_imgs/mask-two-stage.png
---
height: 300
width: 500
align: center
---
Mask R-CNN framework. Source: https://arxiv.org/abs/1703.06870

```
## High level overview of main modules.
This algorithm consists of 4 main modules which we will briefly describe,  
for a more in detail description read the [blog post](https://engineering.matterport.com/splash-of-color-instance-segmentation-with-mask-r-cnn-and-tensorflow-7c761e238b46)
of the creator `Walled Abdulla.`

1.  Backbone
2.  Region Proposal Network
3.  Region of Interest & Bounding Box Regressor
4.  Segmentation Masks

### 1. Backbone
```{figure} ../imgs/cv_imgs/backbone.png
---
align: center
---
Simplified illustration of the backbone nework
```
This constitutes a standard convolutional neural network, it serves as a feature extractor.  
the first layers detect low level features (edges and corners) and last layers are able to detect higher level features (car,person,flower)

#### Feature Pyramid Network
```{figure} ../imgs/cv_imgs/feature-pyramid.png
---
align: center
---
Source: Feature Pyramid Networks paper
```

The Feature pyramid network (FPN) is an improvement on the backbone method it resembles a pyramid shape
with the original image as the base extracting features on the way to the top.  
This method uses 2 pyramids.    
This second pyramid feeds the features extracted by the first pyramid who then pass them down to its lower layers.
The goal of this second pyramid is to improve the dectection of objects at multiple scales, by allowing each level to have access to both lower and higher level features.


### 2. Region Proposal Network
```{figure} ../imgs/cv_imgs/rpn-anchors.png
---
align: center
height: 400
width:  400
---
Simplified illustration showing 49 anchor boxes
```

The Region Proposal Network (RPN) is another neural network that scans the image for regions that may contain objects.  
These regions are called `anchors` these are boxes which are distributed all around the image as shown in the simplified view.  
In practice the RPN draws anchor boxes of diferent sizes and shapes,    
also it does this on the feature map returned by the backbone, not on directly on the input image.

RPN returns two ouputs for each anchor:
1.  Anchor Class: foreground or background
2.  Bounding Box Refinement: uses the anchor class to better fit the object within the bounding box


### 3. Region of Interest & Bounding Box Regressor
At this piont we have the regions of interest proprosed by the RPN.
Now just like in the RPN we generate two outputs for each region of interest
1. Class:
2. Bounding Box Refinment:
   

#### Region of interest Pooling

### 4. Segmentation Masks