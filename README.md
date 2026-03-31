# 🚧 AI Infrastructure Inspection (YOLOv5)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)]
(https://colab.research.google.com/github/Chouikh-Ghassen/ai-infrastructure-inspection/blob/main/notebooks/inference_colab.ipynb)

# AI Infrastructure Inspection Prototype

### Computer Vision-based Road Damage Detection using YOLOv5

---

## 📖 Overview

This project demonstrates an AI-based infrastructure inspection system using **deep learning object detection (YOLOv5)**.

The system automatically detects and classifies road damage from images, supporting digital infrastructure monitoring and Geo-IT asset management workflows.

The prototype was developed using **Google Colab GPU training** and a public road damage dataset.

---

## Motivation

Infrastructure inspection is traditionally:

- Time-consuming  
- Expensive  
- Dependent on manual labor  
- Prone to human error  

This project explores how **computer vision and deep learning** can improve this process by:

- Automatically detecting road damage  
- Standardizing inspection results  
- Enabling scalable infrastructure monitoring  
- Supporting data-driven maintenance decisions  

---

## Approach

### 1. Object Detection Model
- YOLOv5 (PyTorch-based)
- Pretrained weights fine-tuned on road damage dataset

### 2. Training Environment
- Google Colab (GPU: NVIDIA Tesla T4)
- PyTorch
- Ultralytics YOLOv5 implementation

### 3. Dataset
- Dataset: RDD-2022 (Road Damage Dataset)
- Source: Kaggle
- Format: YOLO annotation format (bounding boxes)

### 4. Damage Classes (5 classes)

- longitudinal crack  
- transverse crack  
- alligator crack  
- other corruption  
- pothole  

---

## Training Setup

- Image size: 640×640  
- Model: YOLOv5s  
- Epochs: 50 (prototype stage)  
- Batch size: 16  
- Optimizer: SGD  

---

## 📊 Results (Prototype)

Initial training results on subset of dataset:

- Best class mAP50: ~0.55  
- Crack detection: Good performance  
- Pothole detection: Lower accuracy (~0.25 mAP)  

### Observations

- Class imbalance affects performance  
- Crack-related classes are easier to learn  
- Potholes require more data and augmentation  

---

## Inference Examples

The trained model outputs:

- Bounding boxes around detected damage  
- Class labels for each damage type  
- Confidence scores  

Example outputs:

```
runs/detect/exp/
```

---

## How to Run

### 1. Clone repository

```bash
git clone https://github.com/Chouikh-Ghassen/ai-infrastructure-inspection
cd ai-infrastructure-inspection
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Run inference

```bash
python yolov5/detect.py --weights best.pt --source images/
```

---

## Project Structure

```
ai-infrastructure-inspection/
│
├── yolov5/
├── images/
├── results/
├── data.yaml
├── best.pt
├── requirements.txt
└── README.md
```

---

## Relevance for Geo-IT Systems

This project can be extended for:

- Infrastructure digital twins  
- GIS-based damage mapping  
- Automated road inspection systems  
- Smart city maintenance planning  
- Edge AI deployment for real-time inspection  

---

## Future Work

- Improve dataset balance  
- Train on full dataset  
- GIS integration  
- Real-time video detection  
- API deployment (FastAPI / Streamlit)  
- Edge AI deployment  

---

## Tech Stack

- Python  
- PyTorch  
- YOLOv5  
- OpenCV  
- Google Colab  

---

## Author

**Ghassen Chouikh**

AI & Software Engineer
