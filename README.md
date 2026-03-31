# AI Infrastructure Inspection (YOLOv5)

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/github/Chouikh-Ghassen/ai-infrastructure-inspection/blob/main/notebooks/inference_colab.ipynb)

## Overview

This project demonstrates an AI-based road infrastructure inspection system using YOLOv5 object detection.

It automatically detects and classifies road surface damage from images, enabling scalable, fast, and consistent infrastructure monitoring.

The system was trained using Google Colab GPU (PyTorch) on the RDD-2022 dataset.

## Problem Statement

Traditional road inspection is:
- Manual and time-consuming  
- Expensive and labor-intensive  
- Inconsistent due to human judgment  
- Difficult to scale across large areas  

This project explores how deep learning can automate this process.

## Solution

We use YOLOv5 (You Only Look Once) for real-time object detection to:
- Detect road damage automatically  
- Classify multiple types of cracks and defects  
- Provide bounding boxes with confidence scores  
- Enable scalable infrastructure analysis  

## Damage Classes

- Longitudinal crack  
- Transverse crack  
- Alligator crack  
- Other corruption  
- Pothole  

## Model Details

- Architecture: YOLOv5s  
- Framework: PyTorch  
- Training: Google Colab GPU  
- Dataset: RDD-2022  
- Image size: 640x640  

## Run in Google Colab

Click the Colab button above.

Steps:
1. Open notebook  
2. Run setup cells  
3. Upload image  
4. Run detection  
5. View results  

## Inference (Colab)

```python
from google.colab import files
uploaded = files.upload()
```

```bash
python detect.py --weights best.pt --source input.jpg --img 640 --conf 0.25
```

## Project Structure

```
ai-infrastructure-inspection/
├── notebooks/
├── models/
│   └── best.pt
├── data/
├── images/
├── yolov5/
├── requirements.txt
└── README.md
```

## Results

- mAP@0.5 ~ 0.55 (prototype)
- Good crack detection performance
- Potholes need more data

## Future Work

- Improve dataset balance  
- Add real-time video detection  
- Deploy API (FastAPI / Streamlit)  
- GIS integration for mapping  

## Author

Ghassen Chouikh
AI & Software Engineer
