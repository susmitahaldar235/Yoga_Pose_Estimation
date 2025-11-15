# 🧘‍♀️Yoga Pose Estimation using Heatmaps + EfficientNet + MLP (Real-Time)

A complete Computer Vision + Deep Learning project that performs **real-time yoga pose classification** using:
- MediaPipe Pose for landmark extraction  
- Gaussian Heatmaps for pose encoding  
- EfficientNet-B0 as CNN feature extractor  
- MLP Classifier for pose prediction  
- Real-time feedback system for posture correction  

---

## Features

- Real-time yoga pose detection  
- Heatmap-based feature extraction  
- EfficientNet-B0 (ImageNet pretrained)  
- MLP classifier trained on heatmap features  
- Posture correction feedback  
- Supports 6+ yoga poses  
- CPU-friendly and lightweight  
- Clean and modular code  

---

## Model Pipeline

Webcam → MediaPipe Pose → Heatmap Generation → EfficientNet-B0 → Feature Vector → MLP → Yoga Pose + Feedback
---

##  Project Structure
<img width="591" height="686" alt="image" src="https://github.com/user-attachments/assets/8b610dc4-dbae-4fd6-a66a-04e396c682f4" />

---

## 📸 Heatmap Example

Keypoints → Gaussian heatmaps → Jet color map.

This improves generalization and removes dependency on raw landmark coordinates.

---

## Supported Yoga Poses

- Tree Pose  
- Downdog  
- Goddess  
- Plank  
- Side Plank  
- Warrior  

(Add more by training.)

---

##  Installation

### 1️. Create Virtual Environment
```bash
python -m venv .venv
.\.venv\Scripts\activate 
```
### 2. Install Dependencies
```
pip install -r requirements.txt
```
### 3️. Download Model Files
- mlp_model.pkl
- class_names.json
- scaler.pkl

---
### Training the Model
```
 notebooks/train2.ipynb
```
### Training pipeline:
- Generate heatmaps
- Extract features using EfficientNet-B0
- Train MLP (or SVM / Random Forest)
- Save model + scaler + class names

### Run Real-Time Yoga Pose Detection
The system will:
- Detect your pose
- Display confidence
- Provide posture feedback
- Show live heatmap
---
## Posture Feedback System
The system checks:
- Body alignment
- Keypoint heights
- Limb positions
- Confidence threshold

Feedback examples:
- "Straighten your back"
- "Stand up — you seem to be sitting"
- "Open your hips wider"
- "Raise your arms higher"
---
## Results
Model	Accuracy
- CNN(EfficientNetb0) + MLP	-- 98%
- Only CNN -- 75%
- EfficientNet (direct) -- 80%
- Keypoint(using angles/distances) ML models	-- 85–95%
---
## Future Improvements

- Add temporal modeling (LSTM / Transformer)
- Repetition counting (squats / planks)
- increase number of yoga poses in dataset
- Mobile version using TFLite
- GUI for usability
