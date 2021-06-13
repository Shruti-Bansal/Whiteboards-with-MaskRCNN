# Whiteboards-with-MaskRCNN

### *Problem statement:*

Detection and segmentation of whiteboards present in an image using [Mask-RCNN](https://arxiv.org/abs/1703.06870)

### *Use case:*

Whiteboard detection is a long standing problem that has application in domains like digitalization of education and video conferencing.


### *Challenges:*

The challenges in the problem arise from:
- Effects of lighting 
- Occlusions in the front of whiteboard
- Writings on the whiteboard

Traditional computer vision has relied on line/polygon detection and fiducial markers for detection of whiteboards.
It is hard to isolate whiteboards in images with multiple rectangular objects some of which, like doors, are often white in color.

![traditional CV](./whiteboard_with_lines.png)

### *Solution:*

This work is an attempt to use Mask R-CNN for detection of whiteboard and evaluate how well it does under different conditions of light and occlusion.
The code from [tensorflow implementation of Mask-RCNN by Matterport](https://github.com/matterport/Mask_RCNN)
has been used to train a dataset of whiteboard images

Steps:
1. Create dataset of whiteboard images.
2. Generate annotations for the dataset and divide into training , validation and test datasets. 
3. Transfer learning is used to train the network on the training and validation datasets , starting from pretrained COCO weights.
4. Generate masks and results on the test dataset.

### *Results:*

![Image1](Results/image6.jpg) ![Image1_colored_whiteboard](Results/colored_wb_image6.png) ![Image1_mask](Results/mask_image6.png)
![Image2](Results/image13.jpg) ![Image2_colored_whiteboard](Results/colored_wb_image13.png) ![Image2_mask](Results/mask_image13.png)
![Image3](Results/image14.jpg) ![Image3_colored_whiteboard](Results/colored_wb_image14.png) ![Image3_mask](Results/mask_image14.png)
![Image4](Results/image17.jpg) ![Image4_colored_whiteboard](Results/colored_image17.png) ![Image4_mask](Results/mask_image7.png)