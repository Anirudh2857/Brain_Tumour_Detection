# Brain Tumor Detection Using MRI Scans

## Overview
This project focuses on detecting brain tumors using MRI scan images. It employs deep learning techniques, specifically transfer learning with **ResNet50**, to classify and segment brain tumor regions accurately.

## Features
- Loads and processes brain MRI images along with segmentation masks.
- Uses **TensorFlow's ImageDataGenerator** for data augmentation and normalization.
- Implements **ResNet50** as a feature extractor with a custom classification head.
- Utilizes **early stopping** and **model checkpointing** to optimize performance.
- Provides visualizations of MRI scans, segmentation masks, and detected tumor regions.

## Requirements
Install the necessary dependencies using:
```bash
pip install numpy pandas seaborn matplotlib tensorflow keras opencv-python scikit-image plotly
```

## Dataset
- The dataset contains MRI scan images and their corresponding segmentation masks.
- Data is stored in CSV format with image paths and mask labels.
- Images are preprocessed and split into training and test sets using **train_test_split**.

## How to Run
1. Mount Google Drive and set the dataset path.
2. Load and preprocess MRI scan images.
3. Train the **ResNet50-based** model with early stopping and checkpointing.
4. Evaluate the model using test data.
5. Visualize segmentation results and performance metrics.

## Model Training
- Uses **ResNet50** as the base model, freezing its initial layers.
- Adds fully connected layers for classification.
- Trains with **Adam optimizer** and categorical cross-entropy loss.
- Saves the best model based on validation loss.

## Evaluation
- Computes accuracy on the test dataset.
- Generates a confusion matrix for classification analysis.
- Produces a classification report with precision, recall, and F1-score.
- Displays sample MRI scans with predicted tumor regions.

## Output
- Trained model for brain tumor detection.
- Performance plots for accuracy and loss during training.
- MRI scan visualizations with predicted tumor segmentation.

## License
This project is open-source and intended for educational and research purposes.

