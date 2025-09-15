# Face Pose Estimation

Predict face angles (Yaw, Pitch, Roll) from images and visualize landmarks and head pose axes.

---

## 1️⃣ Project Overview
This project uses a combination of **Mediapipe** and **SVR / MultiOutputRegressor** to estimate facial pose angles from images. It draws both the face landmarks and the 3D axes on the nose.

---

## 2️⃣ Features
- **Predict Yaw, Pitch, Roll** for any input image.
- **Draw face landmarks** on the detected face.
- **Draw axes** at the nose to visualize head orientation.
- **Preprocessing** of landmarks for normalization and centering.
- Handles **single image prediction** and dataset-based training.

---

## 3️⃣ Dataset
- AFLW2000-3D dataset used for training and evaluation.
- Data includes 68 facial landmarks and 3D pose annotations.
- Preprocessing includes:
  - Centering landmarks around the nose
  - Normalizing based on face dimensions
  - Computing extra geometric features

---

## 4️⃣ Installation
```bash
pip install -r requirements.txt
# Python 3.9+ recommended
pip install numpy pandas matplotlib seaborn scikit-learn opencv-python mediapipe h5py

---

## 5️⃣ Usage
1. **Load and preprocess image**
```python
from face_module import FaceMeshModule, preprocess
image_path = "path_to_image.jpg"
image = cv2.imread(image_path)
landmarks = FaceMeshModule(image)
X_img = preprocess(landmarks).reshape(1, -1)

2. **Predict head pose angles**
pred = multi_output_regressor.predict(X_img)[0]
print(f"Yaw: {pred[0]:.4f}, Pitch: {pred[1]:.4f}, Roll: {pred[2]:.4f}")

3. **Vsualize landmarks and axes**
image_rgb = draw_landmarks(image, landmarks)
tdx = int(landmarks.landmark[1].x * image.shape[1])
tdy = int(landmarks.landmark[1].y * image.shape[0])
image_rgb = draw_axis(image_rgb, pred[1], pred[0], pred[2], tdx, tdy)
plt.imshow(image_rgb)
plt.axis('off')
plt.show()










