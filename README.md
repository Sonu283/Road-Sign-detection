# 🛣️ Road Sign Detection and Classification using YOLOv8 and RANSAC

This project focuses on detecting and classifying road signs using an optimized YOLOv8 model, enhanced with RANSAC for geometric validation. It is designed for real-time applications such as Intelligent Transportation Systems and autonomous driving.

---

## 📁 Dataset

- **Format:** Pascal VOC (XML)
- **Images:** PNG format (`road1.png`, `road2.png`, etc.)
- **Annotations:** Stored in `Annotations/` folder
- **Source:** Roboflow or similar curated dataset

---

## 🧠 Model Overview

- **Object Detection:** YOLOv8 (`ultralytics`)
- **Geometric Validation:** RANSAC for robust outlier removal and shape verification
- **Framework:** Python-based pipeline using OpenCV, Ultralytics, NumPy

---

## 📦 Requirements

Install all necessary dependencies via:
- ultralytics==8.0.178
- opencv-python
- matplotlib
- numpy
- scikit-image
- scikit-learn
- lxml

---

## 🚀 Project Structure

Road-Sign-Detection/
│
├── images/                  # Input images
├── Annotations/             # Pascal VOC XML annotation files
├── yolov8x.pt               # Pre-trained YOLOv8 model weights
├── detect.py                # Main detection pipeline
├── ransac_filter.py         # RANSAC validation code
├── requirements.txt         # Python dependencies
└── README.md                # Project description


---

## ⚙️ How to Run

Run YOLOv8 detection:
- python detect.py --source images/ --weights yolov8x.pt

Include RANSAC filtering:
- python detect.py --source images/ --weights yolov8x.pt --use_ransac

---

## 📊 Results 

| Metric     | Value       |
| ---------- | ----------- |
| Precision  | \~94%       |
| Recall     | \~91%       |
| FPS        | \~30+ (GPU) |
| Model Size | \~131 MB    |
| Input Size | 640×640     |

---

## 📸 Output Results

Here are a few sample outputs from the Road Sign Detection system:

<p align="center"> <img src="https://github.com/user-attachments/assets/d6abddde-8eb2-48ab-83a9-280a11069e47" width="300" alt="Detected Output 1" style="margin: 10px;" /> <img src="https://github.com/user-attachments/assets/292e35ea-48c8-4769-ad59-01ba29385b86" width="150" alt="Detected Output 2" style="margin: 10px;" /> <img src="https://github.com/user-attachments/assets/20492224-bb21-49d1-84a3-c026eea9dfe4" width="350" alt="Detected Output 3" style="margin: 10px;" /> <img src="https://github.com/user-attachments/assets/adb8fc7d-cf3f-47f4-b51a-45ef6972ef57" width="250" alt="Detected Output 4" style="margin: 10px;" /> </p>

---
Let me know if you'd like a training section, demo GIFs, or badges (e.g., Python version, license) added to it.

