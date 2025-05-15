# 🚗 Fusion of Object Detection and Motion Estimation for Enhanced Autonomous Robotics  🚗

Combining  the spatial information from the object detector and the temporal information from the motion estimator into a powerful approach for dynamic scene understanding

---

## 📌 Overview

This project implements **late fusion** of spatial and temporal cues by combining:

* **YOLOv8** for object detection
* **Optical flow** (Farneback) for motion estimation

The goal is to improve scene understanding in dynamic driving environments using the **KITTI Scene Flow 2015** dataset.

---
## 💡 Late Fusion Logic

Decision based on:

* **Object confidence** (from YOLOv8)
* **Motion magnitude** (from optical flow)

### Rule-based labels:

* ✅ **Accepted**: High confidence + high motion
* ❌ **Rejected**: Low confidence + low motion
* ⚠️ **Flagged**: Disagreement (e.g., high confidence, low motion)

---

## 📁 Dataset: KITTI Scene Flow 2015

Download from the [official KITTI website](http://www.cvlibs.net/datasets/kitti/eval_scene_flow.php?benchmark=flow).

---

## 🧰 Step-by-Step Setup Guide

### 1. 🚀 Run in Google Colab
✅ You can run the full pipeline directly by opening the CS730Project_Fusion.ipynb notebook in Google Colab.

### 2. 🧠 Upload YOLOv8 Weights
⚠️ You must upload the trained best.pt file (YOLOv8 weights) into the Colab runtime manually before running the code.

### 3. 📌 Notes
* The main notebook CS730Project_Fusion.ipynb includes everything: dataset download, model loading, fusion logic, metrics, and visualization.
* YOLOv8 weights (best.pt) are included separately with the YOLOv8 file and must be uploaded.

---


## 👤 Author

* **Alya Monif**
* Project for: *\CS730*

## 📜 License

This project is for academic and research use only.
KITTI dataset © Karlsruhe Institute of Technology and Toyota Technological Institute.
