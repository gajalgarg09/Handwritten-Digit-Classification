# Handwritten-Digit-Classification-using CNN (MNIST Dataset)
This project implements a Convolutional Neural Network (CNN) to accurately classify handwritten digits from the MNIST dataset. 
The model leverages deep learning to mimic the way the human visual system processes and recognizes patterns.

##  Overview
Humans are exceptionally good at interpreting visual patterns—like handwritten digits—instantly. 
But teaching a machine to do the same is a challenging task due to variations in writing styles, sizes, smudges, and tilts.
In this project, we train a CNN that learns features from raw pixel data, enabling it to automatically detect important visual cues for digit classification without manual feature engineering.

## Dataset

- **Source:** Automatically loaded via:
from tensorflow.keras.datasets import mnist

- **Size:** 60,000 training images, 10,000 test images
- **Image Size:** 28 x 28 pixels, grayscale
- **Classes:** Digits from 0 to 9 (10 classes)

##  Model Architecture
The CNN model is built using the following layers:
- Convolutional Layers
- MaxPooling Layers
- Dropout for regularization
- Flatten and Dense Layers
- Output Layer with Softmax Activation

##  Training Details
- **Optimizer:** Adam  
- **Loss Function:** Categorical Crossentropy  
- **Metrics:** Accuracy  
- **Batch Size:** 64  
- **Epochs:** 15  
- **EarlyStopping:** Used with `patience=3` and `restore_best_weights=True` to prevent overfitting and save training resources  
- **Data Augmentation:** Applied using `ImageDataGenerator` to improve model generalization

## Results
- **Training Accuracy:** ~99.35%
- **Validation Accuracy:** **99.41%**
- The model converged quickly with minimal signs of overfitting thanks to early stopping and data augmentation.

