# Face Pose Estimation

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

## 5️⃣ Models
- **Support Vector Regression (SVR):**  
  Trained separately for each angle (Yaw, Pitch, Roll) with different hyperparameters.  

- **MultiOutputRegressor (SVR):**  
  Wraps around SVR to predict all three angles simultaneously.  

- **Random Forest Regressor:**  
  Used as a baseline for comparison with traditional ensemble learning.  

**Evaluation Metrics:**  
- **Mean Squared Error (MSE):** Measures prediction error.  
- **R² Score:** Explains how well the model fits the data.  

---

## 6️⃣ Visualization
- **Landmarks:**  
  Extracted using **Mediapipe** and drawn in **green** on the detected face.  

- **3D Axes:**  
  Drawn on the nose tip to show head orientation:  
  - **Red → X-axis (Yaw → left/right rotation)**  
  - **Green → Y-axis (Pitch → up/down rotation)**  
  - **Blue → Z-axis (Roll → head tilt)**  

- Works for both **images** and **videos** in real-time.  

---

## 7️⃣ Results
- **Yaw**: Achieved highest accuracy with **Random Forest**.  
- **Pitch & Roll**: Improved with **SVR** after proper preprocessing.  
- Visual overlays confirm the head pose prediction matches the ground truth visually.  

---

## 8️⃣ Future Work
- Improve **Pitch** angle estimation with advanced preprocessing.  
- Experiment with **deep learning** models (CNNs, ResNet, Vision Transformers).  
- Develop a **real-time application** with webcam integration.  
- Train and evaluate on **larger datasets** for robustness.  

---

## 9️⃣ Project Structure

