# 🥤 YOLOv5 Custom Training: Beverages Prediction

This repository documents my journey in learning how to custom-train **YOLOv5** for **beverage object detection** using a custom-annotated dataset. I also experimented with dataset preparation and annotation using **Roboflow**.

---

## 🚀 What I Learned
- How to custom-train the YOLOv5 object detection model on my own data.  
- Using Roboflow for dataset annotation, augmentation, and export.  
- The end-to-end pipeline: data collection, annotation, preprocessing, training, and evaluation with YOLOv5.  
- Best practices for project organization and reproducibility.  

---


---

## 🖼️ Data Collection & Annotation
### 1. Data Collection
- Collected images of beverages from various sources.  
- Focused on different beverage types, lighting conditions, and angles.  
- Ensured dataset diversity for better generalization.  

### 2. Annotation using Roboflow
- Annotated beverage objects with bounding boxes.  
- Created **custom classes** for different beverage types.  
- Applied consistent labeling standards.  
- Exported dataset in **YOLOv5 format** (images + `.txt` labels).  

### 3. Dataset Organization
- Split dataset into **train/valid/test** (70/20/10).  
- YOLO format labels:
  
## Prepare Dataset
# Example: Download via Roboflow
curl -L "YOUR_ROBOFLOW_DOWNLOAD_LINK" > roboflow.zip
unzip roboflow.zip
train: ../train/images
val: ../valid/images
test: ../test/images



## Train Model
python train.py --img 640 --batch 16 --epochs 100 \
--data ../data.yaml --cfg yolov5s.yaml \
--weights yolov5s.pt --cache



