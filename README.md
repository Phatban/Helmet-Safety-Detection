# Helmet Safety Detection with YOLOv10

This project implements a helmet safety detection system using YOLOv10, capable of identifying whether workers are wearing safety helmets in construction sites or industrial environments.

## Project Overview

The Helmet Safety Detection system uses the YOLOv10 object detection model to identify and localize both workers and safety helmets in images and videos. This can be used to enhance workplace safety by automatically monitoring helmet usage.

## Features

- Detect workers and safety helmets in images and videos using a pre-trained YOLOv10 model
- Train YOLOv10 model on custom helmet safety dataset
- Evaluate model performance
- Real-time detection capabilities

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/Phatban/Helmet-Safety-Detection.git
   cd helmet-safety-detection
2. Install the required packages:
   ```bash
   pip install -r requirements.txt
3. Download the Helmet Safety Dataset and place it in the `data/` directory.

## Usage

This project is split into two main parts, each implemented in a separate Google Colab notebook:

### 1. Pre-trained Model Inference

Use the `./pretrained_model_inference.ipynb` notebook to:
- Set up the YOLOv10 environment
- Download and use a pre-trained YOLOv10 model
- Perform inference on sample images and videos

### 2. Custom Training and Evaluation

Use the `./train_and_evaluate.ipynb` notebook to:
- Prepare the Helmet Safety Dataset
- Fine-tune YOLOv10 on the custom dataset
- Evaluate the trained model
- Perform inference with the custom-trained model

## Dataset

This project uses the Helmet Safety Dataset, which includes images of workers with and without safety helmets. The dataset is organized in the YOLO format.

## Model

We use YOLOv10, a state-of-the-art object detection model, first with pre-trained weights and then fine-tuned on our specific helmet safety detection task.

## Contributing

Contributions to improve the project are welcome. Please follow these steps:

1. Fork the repository
2. Create a new branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## Contact

Nguyen Tan Phat - phatban2308@gmail.com

Project Link: [https://github.com/Phatban/Helmet-Safety-Detection](https://github.com/Phatban/Helmet-Safety-Detection)

## Acknowledgements

- [YOLOv10](https://github.com/THU-MIG/yolov10)
- [Ultralytics](https://github.com/ultralytics/ultralytics)
- [Helmet Safety Dataset](https://drive.google.com/file/d/1twdtZEfcw4ghSZIiPDypJurZnNXzMO7R/view)
