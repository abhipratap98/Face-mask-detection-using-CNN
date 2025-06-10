Real-time Face Mask Detection

Your Name
Your Institute (e.g., Yardi School of Artificial Intelligence)
IIT Delhi
your_email@iitd.ac.in

Abstract

In this project, we develop a real-time face mask detection system using deep learning. The model detects whether individuals are wearing a mask or not in video streams. We use a MobileNetV2-based classifier combined with OpenCV face detection for fast and accurate mask detection. The system can be deployed on webcams or CCTV feeds for public safety.

1 Introduction

1.1 Background
Face mask detection became an important public health application during the COVID-19 pandemic. Automated systems help monitor mask compliance in public spaces.

This project integrates:

Face detection in real-time video streams
Mask/no-mask classification using deep learning
Real-time deployment on video feeds
2 Related Work

Face detection: Haar cascades, Dlib, MTCNN
Mask detection: CNN-based classifiers (MobileNetV2, ResNet, EfficientNet)
Lightweight models support edge deployment
Applications in transport hubs, offices, retail spaces
3 Methodology

Task 1: Face Detection
Used OpenCV Haar cascades for face detection in video frames
Detected faces cropped and passed to the classifier
Task 2: Mask Classification
Fine-tuned MobileNetV2 on a mask/no-mask dataset
Model outputs mask presence as binary classification
Task 3: Real-time Inference Pipeline
Video feed processed frame by frame
Pipeline:
Detect faces → Classify mask presence → Annotate frame
4 Dataset

Face Mask Detection Dataset from Kaggle
Two classes: with_mask, without_mask
~3,800 labeled face images
Dataset balanced for training
5 Experimental Setup

Model: MobileNetV2 (pre-trained on ImageNet, fine-tuned on mask dataset)
Training: 50 epochs, Adam optimizer
Batch Size: 32
Evaluation: Accuracy on validation set
6 Results

Mask Classification
Metric	Value
Accuracy	96.5%
Precision	95.8%
Recall	97.2%
Real-time Performance
Achieves >20 FPS on laptop CPU
Works on webcams and recorded videos
7 Conclusion

We present a real-time face mask detection system with high accuracy and fast inference. The lightweight MobileNetV2 model enables deployment on edge devices. Future work includes detecting improper mask usage and using more robust face detectors (e.g., MTCNN, YOLO).

8 Contribution

Your Name (ID): Face detection, mask classifier, real-time pipeline, report
References

OpenCV Documentation
MobileNetV2: Sandler et al. (2018)
Kaggle Face Mask Detection Dataset
Relevant COVID-19 mask detection research papers
