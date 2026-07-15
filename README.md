# FaceCipher

FaceCipher is a deep learning-based face verification system that uses a **Siamese Neural Network** to authenticate users through facial similarity. Instead of classifying faces into predefined identities, the model learns to determine whether two face images belong to the same person, making it suitable for authentication and identity verification tasks.

The project is implemented using **TensorFlow**, **OpenCV**, and **Keras**, with images captured from a webcam and trained using positive, negative, and anchor image pairs.

---

## Overview

Traditional face recognition systems require training on a fixed set of identities. FaceCipher approaches the problem differently by learning a similarity function between two face images using a Siamese Neural Network.

The model extracts feature embeddings from both input images, computes their similarity, and predicts whether they represent the same individual. This approach allows the model to generalize to identities that were not present during training.

---

## Features

### Face Verification

- Real-time webcam-based face verification
- Siamese Neural Network implementation
- Face authentication using similarity scores
- Automatic image preprocessing
- TensorFlow-based inference pipeline

### Dataset Preparation

- Capture anchor images using a webcam
- Capture positive images for the registered user
- Generate negative image pairs using the LFW dataset

### Model Training

- Shared embedding network
- Euclidean distance-based feature comparison
- Binary classification for verification
- Model checkpointing during training

---

## Tech Stack

| Category | Technologies |
|----------|--------------|
| Programming Language | Python |
| Deep Learning | TensorFlow, Keras |
| Computer Vision | OpenCV |
| Numerical Computing | NumPy |
| Data Visualization | Matplotlib |
| Notebook Environment | Jupyter Notebook |
| Dataset | Labeled Faces in the Wild (LFW) |

---

## Requirements

- Python 3.10 or later
- Webcam
- Jupyter Notebook

Install all required dependencies using:

```bash
pip install -r requirements.txt
```

---

## Repository Structure

```text
.
├── FaceCipher_23b1070.ipynb
├── requirements.txt
└── Screen Recording 2025-02-05 013408.mp4
```

---

## System Workflow

```text
Webcam
   │
   ▼
Image Capture
   │
   ▼
Image Preprocessing
   │
   ▼
Embedding Network
   │
   ▼
Feature Extraction
   │
   ▼
Distance Computation
   │
   ▼
Similarity Prediction
   │
   ▼
Verification Decision
```

---

## Installation

Clone the repository.

```bash
git clone https://github.com/<your-username>/FaceCipher.git
```

Navigate to the project directory.

```bash
cd FaceCipher
```

Install the required dependencies.

```bash
pip install -r requirements.txt
```

---

## How to Use

### 1. Prepare the Dataset

- Download the **Labeled Faces in the Wild (LFW)** dataset.
- Create directories for anchor, positive, and negative images.

### 2. Capture Training Images

- Run the notebook.
- Capture anchor images using the webcam.
- Capture positive images of the registered user.

### 3. Train the Model

- Execute the notebook cells sequentially.
- The Siamese Neural Network is trained using positive and negative image pairs.

### 4. Verify Identity

- Capture a live image using the webcam.
- Compare it with stored reference images.
- The model predicts whether both images belong to the same individual.
- Authentication is accepted if the similarity score exceeds the verification threshold.

---

## Running the Project

Launch Jupyter Notebook.

```bash
jupyter notebook
```

Open the notebook.

```text
FaceCipher_23b1070.ipynb
```

Run all notebook cells in sequence.

---

## Model Architecture

The project implements a Siamese Neural Network consisting of:

- Shared embedding network
- Feature extraction layers
- Euclidean distance computation
- Binary classification output layer

The model learns to minimize the distance between images of the same individual while maximizing the distance between different individuals.

---

## Dataset

The project uses the **Labeled Faces in the Wild (LFW)** dataset for generating negative image pairs.

Training data consists of:

- Anchor images
- Positive images
- Negative images

Image pairs are generated dynamically during training.

---

## Training Pipeline

1. Capture anchor images.
2. Capture positive images.
3. Load negative images from the LFW dataset.
4. Preprocess all images.
5. Generate positive and negative image pairs.
6. Train the Siamese Neural Network.
7. Save the trained model.
8. Perform face verification using live webcam input.

---

## Future Improvements

- Support multiple registered users
- Improve robustness under varying lighting conditions
- Integrate face anti-spoofing techniques
- Deploy as a web application
- Mobile application support
- GPU-accelerated inference
- Improve embedding quality using FaceNet or ArcFace

---

## Demonstration

A screen recording demonstrating the project workflow is included in the repository.

---

If you found this project interesting or useful, consider giving the repository a star.
