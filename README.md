# 🪖 Helmet Safety Detection with YOLOv10

This project demonstrates how to fine-tune the **YOLOv10** object detection model to detect whether motorbike riders are wearing helmets, using a custom dataset.

## 📁 Project Structure

- `fine_tuning_yolov10.ipynb`: Main notebook for training, validation, and evaluation of the YOLOv10 model on the helmet dataset.
- `datasets/`: Folder containing the annotated helmet dataset (in YOLO format).
- `runs/`: Output folder for saving training logs and results.
- `weights/`: Pretrained and fine-tuned model weights.

## 🧠 Model

- **Backbone**: YOLOv10n (Nano variant)
- **Training mode**: Fine-tuning with a pretrained YOLOv10 checkpoint
- **Framework**: Ultralytics YOLOv10 (PyTorch-based)

## ✅ Dataset

- Format: YOLO format (images + `.txt` label files)
- Classes:
  - `0`: Head
  - `1`: Helmet
  - `2`: Person
- Includes train/val split, augmentation, and preprocessing handled automatically by Ultralytics pipeline.

## 🚀 How to Run

> 🛠️ **No need to install requirements manually.**  
Just clone the repo and run the notebook.

```bash
git clone https://github.com/Phatban/Helmet-Safety-Detection.git
cd Helmet-Safety-Detection
```

Then open and run `fine_tuning_yolov10.ipynb` step-by-step.

## 📊 Results

The fine-tuned YOLOv10n model achieved the following performance on the validation set:

| Metric               | Value  |
|----------------------|--------|
| **Precision**        | 0.820  |
| **Recall**           | 0.784  |
| **mAP@0.5**          | 0.847  |
| **mAP@0.5:0.95**     | 0.432  |

### 🧠 Per-class metrics:

| Class   | Precision | Recall | mAP@0.5 | mAP@0.5:0.95 |
|---------|-----------|--------|---------|--------------|
| Head    | 0.858     | 0.674  | 0.788   | 0.375        |
| Helmet  | 0.811     | 0.873  | 0.905   | 0.452        |
| Person  | 0.792     | 0.804  | 0.848   | 0.470        |

## 📌 Conclusion

- YOLOv10n (Nano) provides a great balance between speed and accuracy for helmet safety detection.
- The model is suitable for real-time deployment in smart city traffic systems.

## ✍️ Author

- [Tấn Phát Nguyễn](https://github.com/Phatban)