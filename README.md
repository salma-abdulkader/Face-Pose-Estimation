# 3D Face Pose Studio -- README

Predict face angles (Yaw, Pitch, Roll) from images and visualize landmarks and head pose axes.

---

## 1️⃣ Project Overview
This project uses a combination of **Mediapipe** and **SVR / MultiOutputRegressor** to estimate facial pose angles from images. It draws both the face landmarks and the 3D axes on the nose.

This project estimates head pose (Yaw, Pitch, Roll) from facial images using:

- **Mediapipe** → for landmark extraction and visualization.  
- **SVR / MultiOutputRegressor** → for regression-based angle prediction.  

It visualizes the 468 facial landmarks and overlays 3D axes on the nose to show orientation.

---

## 2️⃣ Features
- **Predict Yaw, Pitch, Roll** for any input image.
- **Draw face landmarks** on the detected face.
- **Draw axes** at the nose to visualize head orientation.
- **Preprocessing** of landmarks for normalization and centering.
- Handles **single image prediction** and dataset-based training.

---

## 3️⃣ Dataset
- **AFLW2000-3D dataset** used for training and evaluation.  
- Data includes **68 facial landmarks** and **3D pose annotations**.  
- Preprocessing includes:
  - Centering landmarks around the nose.
  - Normalizing based on face dimensions.
  - Computing extra geometric features.

---

## 4️⃣ Installation
```bash
pip install -r requirements.txt
# Python 3.9+ recommended
pip install numpy pandas matplotlib seaborn scikit-learn opencv-python mediapipe h5py

---
