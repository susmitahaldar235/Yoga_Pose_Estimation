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
Yoga_pose_estimation_CV/
│
├── scripts/
│ ├── realtime_pose_mlp.py ( Real-time webcam system)
│ ├── pose_estimation.py (Heatmap utilities and functions)
│
├── notebooks/
│ ├── train.ipynb  (Main training pipeline)
│ ├── train2.ipynb
│ ├── run.ipynb
│ ├── heatmaps_generated.ipynb
│ ├── keypoints_dataset.ipynb
│
├── models/
│ ├── mlp_model.pkl  (Trained MLP model)
│ ├── scaler.pkl 
│ ├── class_names.json  (Class label mapping)
│
├── data/ 
│
├── requirements.txt
├── README.md
└── .gitignore


