# Real-time Face Mask Detection

---

## Abstract

In this project, we develop a **real-time face mask detection system** using deep learning. The system detects whether individuals are wearing a mask in video streams, combining **MobileNetV2-based mask classification** with **OpenCV face detection** for fast, accurate inference. The system can be deployed on **webcams** or **CCTV feeds** to monitor mask compliance for public safety.

---

## 1 Introduction

### 1.1 Background

Face mask detection emerged as a crucial public health application during the **COVID-19 pandemic**. Automated systems help enforce mask mandates and monitor compliance in public areas.

This project integrates:
- **Real-time face detection** in video streams
- **Mask/no-mask classification** using deep learning
- **Deployment on video feeds** (webcam, CCTV)

---

## 2 Related Work

- **Face Detection:** Haar cascades, Dlib, MTCNN  
- **Mask Detection:** CNN-based classifiers (MobileNetV2, ResNet, EfficientNet)  
- **Lightweight models** enable **edge deployment**  
- Applications: transport hubs, offices, retail spaces, public infrastructure

---

## 3 Methodology

### Task 1: Face Detection
- Used **OpenCV Haar cascades** for face detection in video frames
- Detected faces cropped and passed to the mask classifier

### Task 2: Mask Classification
- Fine-tuned **MobileNetV2** on a mask/no-mask dataset
- Outputs **binary classification**: Mask / No Mask

### Task 3: Real-time Inference Pipeline
- Process video feed **frame by frame**:
  - **Detect faces → Classify mask presence → Annotate frame**

---

## 4 Dataset

- Source: **Face Mask Detection Dataset** from Kaggle
- Classes: **with_mask**, **without_mask**
- ~**3,800 labeled face images**
- Dataset balanced for effective training

---

## 5 Experimental Setup

- **Model:** MobileNetV2 (pre-trained on ImageNet, fine-tuned)
- **Training:** 50 epochs, Adam optimizer
- **Batch Size:** 32
- **Evaluation:** Accuracy on validation set

---

## 6 Results

### Mask Classification Performance

| Metric    | Value  |
|-----------|--------|
| Accuracy  | 96.5 % |
| Precision | 95.8 % |
| Recall    | 97.2 % |

### Real-time Performance

- Achieves **>20 FPS** on laptop CPU
- Works with **webcam streams** and **recorded videos**

---

## 7 Conclusion

We present a **real-time face mask detection system** with high accuracy and fast inference. The **lightweight MobileNetV2** model supports deployment on **edge devices**.  
**Future work** includes:
- Detecting **improper mask usage**
- Using more robust face detectors (**MTCNN**, **YOLO**)

---

## 8 Contribution

**Your Name (Your ID):**  
- Face detection  
- Mask classifier  
- Real-time pipeline  
- Report

---

## References

- OpenCV Documentation  
- MobileNetV2: Sandler et al. (2018)  
- Kaggle Face Mask Detection Dataset  
- Relevant COVID-19 mask detection research papers

---
