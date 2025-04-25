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

## Usage

1. **Clone and install dependencies:**
    ```
    git clone <repo-url>
    cd <repo-folder>
    pip install -r requirements.txt
    ```
2. **Prepare datasets:** Place FER-2013, YoungAffectNet HQ, and RAF-DB in the `data/` directory.
3. **Train the model:**
    ```
    python train.py
    ```
4. **Run emotion detection and get music recommendations:**
    ```
    python recommend_music.py --image path_to_face_image.jpg
    ```

---

## Findings

- Addressing class imbalance significantly reduces overfitting and improves generalization.
- Increasing dataset size and using regularization techniques (Dropout, BatchNorm) enhance model performance.
- Adding Conv layers in later stages can boost accuracy.

---

## Future Directions

- Integrate real-time webcam emotion detection.
- Enhance music matching logic.
- Deploy as a web or mobile application.

---

**Note:** For academic use only.
