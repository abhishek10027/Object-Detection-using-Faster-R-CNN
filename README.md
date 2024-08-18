# Object Detection using Faster R-CNN

## Introduction

Object detection is a crucial computer vision task that involves identifying and localizing objects within images. It serves as a foundation for various applications, such as object tracking, event detection, and more. Unlike image classification, object detection requires accurate computation of object locations and sizes. Recent advancements in machine learning, particularly in convolutional neural networks (CNNs), have significantly enhanced object detection capabilities.

This project focuses on the Faster R-CNN model, a prominent method in object detection. The model builds on the strengths of earlier models like R-CNN and Fast R-CNN, offering a more efficient and accurate approach by eliminating the need for selective search for region proposals.

## Methodology

The proposed method for object detection leverages the Faster R-CNN architecture, which uses a ResNet-101 backbone for feature extraction. Key components include:

- **Region Proposal Network (RPN):** Generates region proposals by classifying and regressing bounding box positions.
- **ROI Align:** Ensures precise handling of regions of interest, improving detection accuracy.
- **Anchors:** Pre-defined bounding boxes used for object classification and localization.

The architecture diagram for the proposed methodology is illustrated in Figure 1.

## Dataset

This project utilizes the Microsoft COCO dataset, a widely-used resource in computer vision with over 330,000 images labeled with 80 different categories. The COCO dataset is essential for training and evaluating object detection models.

## System Requirements

### Hardware Configuration

| Item               | Parameters    |
|--------------------|---------------|
| Operating System   | Windows 10    |
| CPU                | Intel Core i3 |
| RAM                | 8 GB          |
| Memory             | 1 TB HDD      |

### Software Configuration

| Item               | Parameters                     |
|--------------------|--------------------------------|
| Language           | Python 3.8.1                   |
| Coding Platform    | Google Colab                   |
| Libraries          | OpenCV, torchvision, torch, Matplotlib, numpy |
| Model              | CNN, RCNN, DNN                 |

### Training Details

The training process utilizes a pre-trained Faster R-CNN model for object detection. The model is set to evaluation mode, and only high-confidence predictions are retained for visualization. The process involves:

- Preprocessing input images.
- Extracting predictions based on confidence thresholds.
- Visualizing results with bounding boxes and labels.

### Testing Details

During testing, images are resized and passed through the model, with a confidence threshold of 0.8 applied to retain high-confidence predictions. The results are visualized, showcasing the model's detection capabilities.

### Results Description

Four images were randomly selected from the COCO dataset for testing. The confidence scores for detected objects are as follows:

- **Figure (a):** Laptop - 86.07%
  ![image](https://github.com/user-attachments/assets/187d2c89-20e6-4839-aec7-2a452fa84063)

- **Figure (b):** Car - 93.5%
  ![image](https://github.com/user-attachments/assets/b132c9e4-8de0-4b80-9b9b-bf3097c33d87)

- **Figure (c):** Traffic Light - 99.69%
  ![image](https://github.com/user-attachments/assets/2a88a4b4-38f6-4938-8ebd-22d8af65c4ce)

- **Figure (d):** Person 1 - 99.53%, Person 2 - 99.39%
  
  ![image](https://github.com/user-attachments/assets/5d2f2881-b88d-4069-abef-20e4b8105c66)



# The results indicate that the proposed model performs well for detecting larger objects with higher confidence scores.

## Conclusion

This project presents an in-depth exploration of CNN, RCNN, Fast R-CNN, and primarily focuses on the Faster R-CNN network. We propose a method using CARPN for generating high-quality region proposals. By sharing convolutional features with the detection network, our approach enhances object detection accuracy while maintaining near real-time performance. Future work could explore network structure optimization based on specific detection objects or test the methodology on other advanced detection methods like YOLO V4, Mask R-CNN, and Cascade R-CNN.
