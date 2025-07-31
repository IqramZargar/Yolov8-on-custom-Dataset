# 🚀 YOLOv8 Custom Object Detection (Colab Project)

This project showcases training a YOLOv8 object detection model on a **custom dataset** using Google Colab and Google Drive. It's built to work entirely on Colab, perfect for low-end hardware, and includes training, evaluation, and visual results.

---

## 📌 Project Overview

- **Model**: YOLOv8s (`yolov8s.pt`)
- **Task**: Object Detection
- **Dataset**: Custom-labeled dataset (stored in Google Drive)
- **Training Environment**: Google Colab
- **Epochs**: 25  
- **Image Size**: 224x224  
- **Framework**: [`ultralytics`](https://github.com/ultralytics/ultralytics)

---

## 🧠 Features

- Mounts Google Drive and loads dataset
- Installs YOLOv8 and trains on custom data
- Automatically generates:
  - Confusion Matrix
  - Training Results Plot
  - Predicted Bounding Boxes

---

## 🖼️ Sample Results

Results after training are shown below:

<p align="center">
  <img src="runs/detect/train2/confusion_matrix.png" width="500"/>
  <img src="runs/detect/train2/results.png" width="500"/>
  <img src="runs/detect/train2/val_batch0_pred.jpg" width="500"/>
</p>

---

## 📂 Project Structure

/content/drive/MyDrive/YOLOv8/
├── data.yaml
├── images/
│ ├── train/
│ └── val/
└── runs/
└── detect/
└── train2/


## ⚙️ How to Run This Project

To run this notebook on Google Colab:

1. **Mount Google Drive**:
   ```python
   from google.colab import drive
   drive.mount('/content/drive')

2. Navigate to dataset directory:


  %cd /content/drive/MyDrive/YOLOv8

3. Install YOLOv8:


  !pip install ultralytics  

4. Train the Model:

  !yolo task=detect mode=train model=yolov8s.pt data=data.yaml epochs=25 imgsz=224 plots=True

📝 Make sure your dataset is correctly placed and data.yaml is configured.  

⚠️ Notes
This notebook includes all output cells so results are visible even without re-running.

If you're re-running the notebook:

Mount Drive manually

Ensure dataset path matches

Dataset is not public here — please upload your own or request access.

✅ Requirements

Google Colab (no local GPU required)

Google Drive

Python 3.x

ultralytics package

🔗 Useful Links

YOLOv8 Documentation

Ultralytics GitHub

# Yolov8-on-custom-Dataset
