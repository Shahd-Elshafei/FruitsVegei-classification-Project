# FuitsVegei-classification-Project
# 🥦🍎 Fruits & Vegetables Classification and Detection

## 📌 Overview
This project focuses on **image-based recognition of fruits and vegetables**.  
It includes two main tasks:
1. **Classification** of images into fruit or vegetable categories using **Transfer Learning (VGG16)**.  
2. **Detection** of fruits and vegetables in images using the **YOLOv8 model**.  

Both approaches are compared and discussed in the included report.

---

## 📂 Project Structure
- `notebooks/`
  - `classification_vgg16.ipynb` → Transfer learning with VGG16 for classification  
  - `detection_yolov8.ipynb` → YOLOv8 for object detection  
- `models/`
  - `fruits_recognition_model.h5` → Trained VGG16 classification model  
  - `yolov8m.pt` → Trained YOLOv8 detection model  
- `report.pdf` → Report with model comparison, summaries, and requirements list  
- `README.md` → Project documentation  

---

## 🚀 Methods

### 🔹 Classification with VGG16
- Implemented transfer learning using **VGG16**.  
- Training strategy:
  - **First 3 epochs** → froze all base layers, trained only the added classifier head.  
  - **Next 3 epochs** → unfroze the 5th block of VGG16, trained with a smaller learning rate.  

### 🔹 Detection with YOLOv8
- Annotated a subset of training images using **Roboflow**.  
- Trained the **YOLOv8m** model on annotated data.  
- Evaluated on a separate test directory.  

---

## 📊 Results
- **VGG16** achieved strong classification accuracy after fine-tuning.  
- **YOLOv8** successfully detected and localized fruits and vegetables in images.  
- The **report.pdf** provides a side-by-side comparison of the two approaches, discussing their goals, strengths, and limitations.  

---

## ⚙️ Requirements
The required libraries and dependencies are listed in the **report.pdf**.  
Key tools used include:
- Python  
- TensorFlow / Keras (for VGG16)  
- PyTorch & Ultralytics YOLO (for YOLOv8)  
- Roboflow (for annotation)  

---

## 📌 How to Run
1. Clone this repository:
   ```bash
   git clone https://github.com/YOUR-USERNAME/fruit-veg-recognition.git
   cd fruit-veg-recognition
