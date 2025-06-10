# Helmet Safety Detection with YOLOv10

This project is part of the AIO2024 Course and aims to build an object detection system using **YOLOv10** to detect whether construction workers are wearing helmets on site.

## 📌 Project Overview

Helmet Safety Detection is a real-world application of object detection in Computer Vision. Given an input image, the system outputs bounding boxes for:

- Workers (`person`)
- Heads (`head`)
- Helmets (`helmet`)

We utilize **YOLOv10**, the latest YOLO version from THU-MIG Lab, and fine-tune it on the **Helmet Safety Dataset**.

---

## 🔧 Setup Instructions

### 1. Clone YOLOv10 Repository
```bash
git clone https://github.com/THU-MIG/yolov10.git
cd yolov10
```

### 2. Install Dependencies
```bash
pip install -r requirements.txt
pip install -e .
```

### 3. Download Pretrained Weights
```bash
wget https://github.com/THU-MIG/yolov10/releases/download/v1.1/yolov10n.pt
```

---

## 📂 Dataset

We use the **Safety Helmet Detection Dataset**, which includes labeled images with three classes: `person`, `helmet`, and `head`.

### Download and Extract:
```bash
gdown '1twdtZEfcw4ghSZIiPDypJurZnNXzMO7R'
mkdir safety_helmet_dataset
unzip Safety_Helmet_Dataset.zip -d safety_helmet_dataset
```

---

## 🧠 Training the Model

Using the YOLOv10n variant and training on the dataset:

```python
from ultralytics import YOLOv10

model = YOLOv10('yolov10n.pt')
model.train(
    data='../safety_helmet_dataset/data.yaml',
    epochs=50,
    imgsz=640,
    batch=256
)
```

---

## 📊 Evaluating the Model

After training, evaluate the model on the test set:

```python
model = YOLOv10('runs/detect/train/weights/best.pt')
model.val(data='../safety_helmet_dataset/data.yaml', imgsz=640, split='test')
```

---

## 📸 Inference

You can use an image or video (including YouTube URLs) as input:

```python
model = YOLOv10('yolov10n.pt')
result = model(source='images/HCMC_Street.jpg')[0]
result.save('./images/predict.png')
```

---

## 🏷️ Optional: Manual Labeling

If you wish to create your own dataset, consider using [labelImg](https://github.com/heartexlabs/labelImg) for annotation. Make sure to export labels in **YOLO format**.

---

## 📚 References

- [YOLOv10 GitHub](https://github.com/THU-MIG/yolov10)
- [labelImg Tool](https://github.com/heartexlabs/labelImg)
- Helmet Dataset from AIO2024 Course

---

## ✍️ Authors

- Tan-Phat NguyenNguyen
- AIO Vietnam – AI Course 2024