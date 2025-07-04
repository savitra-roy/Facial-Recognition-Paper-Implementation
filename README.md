# Facial-Recognition-Paper-Implementation

A deep learning project that detects emotions from facial expressions and recommends music to match the user's mood.

---

## Overview

- Utilizes a Convolutional Neural Network (CNN) for facial emotion recognition, based on the architecture from "Facial emotion recognition using CNNs".
- Trained on FER-2013 and additional datasets (YoungAffectNet HQ, RAF-DB) to address class imbalance.
- Maps detected emotions (angry, disgusted, fearful, happy, sad, neutral, surprised) to music recommendations.

---

## Model Highlights

- **Architecture:** 7 Conv layers, MaxPooling, Dropout, BatchNorm, Dense(1024, L2 regularization), Softmax output.
- **Regularization:** Dropout and L2; BatchNorm for faster convergence.
- **Dataset:** FER-2013 (35,000+ images), augmented with external datasets for class balance.
- **Best Results:**  
  - Validation Accuracy: 70.29%  
  - Training Accuracy: 77.87%  
  - Achieved after data augmentation, architecture tuning, and 30 epochs of training.

---

## Key Experiments

- Data augmentation for under-represented classes using Keras.
- Added more images from RAF-DB and YoungAffectNet HQ.
- Introduced Batch Normalization and additional Conv layers.
- Adjusted strides, increased Dropout, and extended training epochs.

---



**Note:** For academic use only.
