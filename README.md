# Caltech-101 Image Classification

This project implements and evaluates multiple image classification methods on the Caltech-101 dataset. We compare 2 deep learning methods and 1 classical machine learning method, with comprehensive evaluation metrics and ablation studies.

## Overview

The project compares three different classification approaches:
1. **HOG + SVM** (Classical ML) - Test Accuracy: 66.47%
2. **EfficientNet** (Deep Learning - Transfer Learning) - Test Accuracy: 94.97%
3. **ResNet18** (Deep Learning - Transfer Learning) - Test Accuracy: 93.22%

## Dataset

- **Dataset**: Caltech-101
- **Categories**: 102 object categories (101 object classes + 1 background class)
- **Total Images**: 9,144 images
- **Split**: 70% train, 15% validation, 15% test (stratified)

## Models

### 1. HOG + SVM (Classical ML)
- Extracts Histogram of Oriented Gradients (HOG) features
- Uses Support Vector Machine (SVM) with linear kernel
- Image size: 64×64 for feature extraction

### 2. EfficientNet-B0
- Pretrained EfficientNet-B0 model from torchvision
- Fine-tuned on Caltech-101 dataset
- Transfer learning approach

### 3. ResNet18
- Pretrained ResNet18 model from torchvision
- Fine-tuned on Caltech-101 dataset
- Transfer learning approach

## Ablation Studies

### Image Size Experiment
- Compared 64×64 vs 128×128 image sizes
- Results show significant improvement with larger image sizes

### Data Augmentation Experiment
- Compared training with vs without data augmentation
- Evaluated impact on model performance

## Requirements

- Python 3.x
- PyTorch
- torchvision
- scikit-learn
- scikit-image
- numpy
- matplotlib
- seaborn
- PIL (Pillow)
- tqdm

## Usage

This project was developed in Google Colab. To run:

1. Upload the notebook to Google Colab
2. Mount your Google Drive
3. Ensure the Caltech-101 dataset is available in your Drive
4. Run the notebook cells sequentially

## Results

The project includes comprehensive evaluation metrics:
- Overall accuracy
- Per-class accuracy
- Confusion matrices
- Precision, Recall, F1-Score (macro and weighted)
- Top-5 accuracy
- Training/validation curves
- Visualization plots

## Files

- `mini_project_1_colab.ipynb`: Main Jupyter notebook with all experiments

## License

This project is open source and available for educational purposes.
