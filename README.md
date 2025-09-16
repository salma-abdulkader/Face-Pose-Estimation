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

## 2️⃣ What the Notebook Does ?!
- Load face images and their corresponding pose parameters from **.mat** files (e.g., AFLW2000-3D dataset).
- Extract facial landmarks using **MediaPipe FaceMesh**.
- Preprocess landmarks into feature vectors.
- Build a DataFrame linking image IDs, features, and target angles.
- Split data into training/testing sets.
- Train and evaluate a multi-output regression model **(SVR)**.
- Save the trained model for reuse.
- Visualize landmarks and draw 3D axes (head pose) on faces.
- Run live demo via webcam or video, overlaying pose axes in real time.

---

## 3️⃣ Requirements (Libraries Used)
- Python 3.8+ (recommended)
- numpy
- pandas
- scipy
- matplotlib
- seaborn
- scikit-learn
- opencv-python (cv2)
- mediapipe (FaceMesh)
- h5py / scipy.io (for reading .mat files)
- pickle (for saving/loading models)
- (Optional in Google Colab): from google.colab import files, cv2_imshow

In the notebook, mediapipe was sometimes pinned to a specific version (e.g., mediapipe==0.10.18) to avoid compatibility issues.
---

## 2️⃣ Dataset Structure
Expected directory layout (example using AFLW2000-3D):

... 
aflw2000-3d/
  AFLW2000/
    image00001.jpg
    image00001.mat
    image00002.jpg
    image00002.mat
    ...
    
- Each .mat file contains a variable Pose_Para that stores Pitch, Yaw, Roll.
---

## 2️⃣ What the Notebook Does ?!
- Load face images and their corresponding pose parameters from **.mat** files (e.g., AFLW2000-3D dataset).
- Extract facial landmarks using **MediaPipe FaceMesh**.
- Preprocess landmarks into feature vectors.
- Build a DataFrame linking image IDs, features, and target angles.
- Split data into training/testing sets.
- Train and evaluate a multi-output regression model **(SVR)**.
- Save the trained model for reuse.
- Visualize landmarks and draw 3D axes (head pose) on faces.
- Run live demo via webcam or video, overlaying pose axes in real time.

---

## 2️⃣ What the Notebook Does ?!
- Load face images and their corresponding pose parameters from **.mat** files (e.g., AFLW2000-3D dataset).
- Extract facial landmarks using **MediaPipe FaceMesh**.
- Preprocess landmarks into feature vectors.
- Build a DataFrame linking image IDs, features, and target angles.
- Split data into training/testing sets.
- Train and evaluate a multi-output regression model **(SVR)**.
- Save the trained model for reuse.
- Visualize landmarks and draw 3D axes (head pose) on faces.
- Run live demo via webcam or video, overlaying pose axes in real time.

---

## 2️⃣ What the Notebook Does ?!
- Load face images and their corresponding pose parameters from **.mat** files (e.g., AFLW2000-3D dataset).
- Extract facial landmarks using **MediaPipe FaceMesh**.
- Preprocess landmarks into feature vectors.
- Build a DataFrame linking image IDs, features, and target angles.
- Split data into training/testing sets.
- Train and evaluate a multi-output regression model **(SVR)**.
- Save the trained model for reuse.
- Visualize landmarks and draw 3D axes (head pose) on faces.
- Run live demo via webcam or video, overlaying pose axes in real time.

---

## 2️⃣ What the Notebook Does ?!
- Load face images and their corresponding pose parameters from **.mat** files (e.g., AFLW2000-3D dataset).
- Extract facial landmarks using **MediaPipe FaceMesh**.
- Preprocess landmarks into feature vectors.
- Build a DataFrame linking image IDs, features, and target angles.
- Split data into training/testing sets.
- Train and evaluate a multi-output regression model **(SVR)**.
- Save the trained model for reuse.
- Visualize landmarks and draw 3D axes (head pose) on faces.
- Run live demo via webcam or video, overlaying pose axes in real time.

---


















