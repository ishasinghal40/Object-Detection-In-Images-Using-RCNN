# Object-Detection-In-Images-Using-RCNN

**1.1 Introduction to domain**

The task of object detection and localization is to find all the objects of interest in the image, and determine their location and size. Because various objects have different appearances, shapes, poses, interference of illumination and occlusion, object detection and localization have always been the challenging issue in machine vision. 

In the field of computer vision, the deep learning method represented by convolutional neural networks has made breakthroughs in tasks such as image classification, object detection, image segmentation and object tracking. Compared with traditional methods, convolutional neural networks can learn richer semantic information and high-level image feature representation, which can better describe the differences between different objects in big data. More importantly, the convolutional neural network is an end-to-end model structure. The original image is used as the input of the whole network. And it gets the final result directly through layer-by-layer calculation, which reduces the complicated data preprocessing, feature extraction and other manual operations. 

R-CNN, fast R-CNN, and faster R-CNN are algorithms developed for object detection based on CNN. These algorithms need a separate region proposal to detect and classify objects from an image. Faster R-CNN is an efficient object detection method for images. Its application is on the rise for fast models, especially in robotics, autonomous cars, and real-time systems. Moreover, in the medical field, it is used for detecting objects in X-rays and microscopic images, and has led to a faster response time regarding medical matters. The main factors to consider when detecting objects are precision and computation time.

A Region Proposal Network (RPN) is a fully-convolutional network that simultaneously predicts object bounds and objectness scores at each position. RPNs are trained end-to-end to generate high quality region proposals, which are used by Fast R-CNN for detection. With a simple alternating optimization, RPN and Fast R-CNN can be trained to share convolutional features.

**1.2 Problem Definition**

In this project, objects will be detected using the Open Images V6 Dataset implementing Faster R-CNN. Open Images is a dataset of ~9M images annotated with image-level labels, object bounding boxes, object segmentation masks, visual relationships, and localized narratives. It contains a total of 16M bounding boxes for 600 object classes on 1.9M images, making it the largest existing dataset with object location annotations. The boxes have been largely manually drawn by professional annotators to ensure accuracy and consistency. The images are very diverse and often contain complex scenes with several objects.

**1.3 Objective **

We show that an algorithmic change - computing proposals with a deep net - leads to an elegant and effective solution, where proposal computation is nearly cost-free given the detection network’s computation. To this end, we utilize Region Proposal Networks (RPNs) that share convolutional layers with state-of-the-art object detection networks. By sharing convolutions at test-time, the marginal cost for computing proposals is small (e.g., 10ms per image).
