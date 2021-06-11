# Whiteboards-with-MaskRCNN

### *Problem statement:*

Detection and segmentation of whiteboards present in an image.


### *Use case:*

Whiteboard detection is a long standing problem that has application in domains like digitalization of education and video conferencing.


### *Challenges:*

The challenges in the problem arise from:
- Effects of lighting 
- Occlusions in the front of whiteboard
- Writings on the whiteboard

Traditional computer vision has relied on line/polygon detection and fiducial markers for detection of whiteboards.
It is hard to isolate whiteboards in images with multiple rectangular objects some of which, like doors, are often white in color.


### *Solution:*

This work is an attempt to use Mask R-CNN for detection of whiteboard and evaluate how well it does under different lighting conditions as well as in cluttered class rooms or conference rooms.
