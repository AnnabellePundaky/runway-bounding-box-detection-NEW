  **YOLOv8 Runway Detection Project**

****📑 Project Overview****
This project fine-tunes a YOLOv8 model to detect runways in aerial images. Using the LARD dataset with annotated runway images (https://github.com/deel-ai/LARD/tree/main), 
the model learns to identify runways and predict their bounding boxes with high accuracy. This repository includes the data preparation, 
training, and testing processes necessary to achieve effective runway detection.

This is a very lean model that is trained and validated on a subset of 150 photos from the LARD data set (which contains 17k photos).
This allows anyone to be able to run this on their computer at home without needing any GPU's.

**🛠️ Features**
- YOLOv8 fine-tuning using the LARD dataset.
- Detects and draws bounding boxes around runways in aerial images.
- Achieved high confidence on test data with mAP50 scores up to 0.983.
- Includes visualization tools to display bounding boxes on training, validation, and test images.

**🛠️ How it Works**
1. Dataset Preparation:
- The script samples a subset from the LARD dataset, more specifically from the LARD_train_BIRK_LFST folder
(https://entrepot.recherche.data.gouv.fr/dataset.xhtml?persistentId=doi:10.57745/MZSH2Y), to create train and validation sets.
NOTE: It should not matter which data set folder you take from LARD data set download list. I chose LARD_train_BIRK_LFST randomly
- Bounding box coordinates from the metadata are converted to YOLO format and adjusted for image resizing.

2. Model Training:
- The YOLOv8 model is fine-tuned using the prepared train/val datasets.
- Training runs for 50 epochs with logs of precision, recall, and mAP scores for each epoch.

3. Inference on Test Image:
- After training, the model is tested on new, unseen aerial image to validate performance.
- Bounding boxes are drawn on the test image with confidence scores displayed.

**📂 Project Structure**




![image](https://github.com/user-attachments/assets/4b001172-b908-4d86-84fb-72b0c490c370)


**🎯 Results**
Training Performance:
- mAP50: 0.983
- Precision: 0.986
- Recall: 0.96

Test Image: The test image successfully detected a runway with a confidence score of 0.98.

**🚀 Future Improvements**
- Use a GPU for faster training (e.g., on Google Colab).
- Experiment with data augmentation to increase model robustness.
- Test on many images
- Deploy the model for real-time runway detection with live image streams.
  
**📜 License**
This project is open-source and available under the MIT License.

**🤝 Acknowledgments**
- Ultralytics for providing the YOLOv8 framework.
- LARD Dataset for training and validation data.
