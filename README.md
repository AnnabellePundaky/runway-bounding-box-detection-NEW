YOLOv8 Runway Detection Project

📑 Project Overview
This project fine-tunes a YOLOv8 model to detect runways in aerial images. Using the LARD dataset with annotated runway images (https://github.com/deel-ai/LARD/tree/main), 
the model learns to identify runways and predict their bounding boxes with high accuracy. This repository includes the data preparation, 
training, and testing processes necessary to achieve effective runway detection.

This is a very lean model that is trained and validated on a subset of 150 photos from the LARD data set (which contains 17k photos).
This allows anyone to be able to run this on their computer at home without needing any GPU's.

🛠️ Features
- YOLOv8 fine-tuning using the LARD dataset.
- Detects and draws bounding boxes around runways in aerial images.
- Achieved high confidence on test data with mAP50 scores up to 0.983.
- Includes visualization tools to display bounding boxes on training, validation, and test images.

📂 Project Structure
runway-bounding-box-detection/
│
├── dataset_demo/           # Subset of images and labels used for training/validation
│   ├── images/             # Train and validation images
│   │   ├── train/
│   │   └── val/
│   ├── labels/             # YOLO labels (bounding boxes in .txt format)
│   │   ├── train/
│   │   └── val/
│   └── runway.yaml         # Configuration file for YOLOv8 training
├── runs/                   # YOLOv8 training results and weights after fine tuning
├── test_image_resized.jpeg # Test image used to evaluate the model
├── yolo_demo.ipynb         # Main script (.ipynb) to train, test, and visualize results
└── README.md               # Project README (this file)
