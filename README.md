# Strawberry Detection Mobile App (YOLOv8 + TFLite + Android)

![picture](https://storage.googleapis.com/kaggle-datasets-images/9512492/14869701/3bd0f2f52b648290da58a284d147a05e/dataset-cover.png?t=2026-02-17-15-14-50)

This project demonstrates an end-to-end computer vision pipeline for real-time strawberry detection.
A YOLOv8 model was trained on a [Kaggle dataset](https://www.kaggle.com/datasets/mahyeks/multi-class-strawberry-ripeness-detection-dataset), optimized and converted to TensorFlow Lite, and deployed in an Android application for on-device inference using the phone camera.


## Demo

![demo](demo.gif)


## Problem

The goal of the project was to build a real-time object detection system capable of running on a mobile device.
The model should detect strawberries in camera input while maintaining good accuracy and high performance.


## Dataset

Dataset from Kaggle containing labeled images of strawberries.

Steps:

* Converted annotations to YOLO format
* Split into train / validation / test
* Applied data augmentation


## Model Training

Model: YOLOv8n
Framework: PyTorch / Ultralytics

Training parameters:

* epochs: 30
* image size: 640
* batch size: 16

Results:

* mAP50: 0.87
* mAP50-95: 0.62

## Model Optimization

The trained model was exported to TensorFlow Lite for mobile deployment.

Steps:

* Export YOLOv8 → ONNX
* Convert to TFLite
* Quantization for smaller size
* Performance benchmarking

Results:

* Model size reduced from 22MB → 6MB
* Real-time inference on mobile device

