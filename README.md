# CustomCNNWithAttention for Dog Cardiomegaly Classification

This repository contains the implementation of a novel attention-based deep learning model, **CustomCNNWithAttention**, for the classification of dog cardiomegaly into three categories: Small, Normal, and Large. The model integrates advanced architectural components like Squeeze-and-Excitation (SE) blocks and Residual Blocks to enhance feature learning and improve classification performance.

## Table of Contents
- [Introduction](#introduction)
- [Model Architecture](#model-architecture)
- [Dataset](#dataset)
- [Training and Validation](#training-and-validation)
- [Results](#results)
- [Installation](#installation)
- [Usage](#usage)
- [Future Work](#future-work)
- [License](#license)

---

## Introduction
Cardiomegaly, or an enlarged heart, is a critical condition in dogs that requires accurate diagnosis and classification for effective treatment. Traditional diagnostic methods, such as radiographic assessments, are time-consuming and prone to human error. This project leverages deep learning to automate the classification process, providing a scalable and efficient solution for veterinary diagnostics.

---

## Model Architecture
The **CustomCNNWithAttention** model consists of:
1. **Convolutional Layers**: Extract low-level features such as edges and textures.
2. **Squeeze-and-Excitation (SE) Blocks**: Introduce channel-wise attention to focus on diagnostically relevant features.
3. **Residual Blocks**: Facilitate deeper feature extraction and improve gradient flow using skip connections.
4. **Global Average Pooling (GAP)**: Reduce feature maps to a single vector for each channel.
5. **Fully Connected Layers**: Output the final probabilities for the three classes (Small, Normal, Large).

---

## Dataset
The model was trained on the **Dag Cardiomegaly dataset**, which contains annotated thoracic radiographs of dogs. The dataset is divided into three categories:
- **Small**
- **Normal**
- **Large**

Preprocessing steps included:
- Resizing images to \(224 \times 224\).
- Normalizing pixel values.
- Data augmentation (random flipping, rotation, and color jittering) to improve generalization.

---

## Training and Validation
The training pipeline included:
- **Loss Function**: Cross-entropy loss for multi-class classification.
- **Optimizer**: Adam optimizer with a Cyclic Learning Rate scheduler.
- **Class Imbalance Handling**: WeightedRandomSampler to ensure balanced representation of all classes.
- **Regularization**: Dropout and L2 regularization to mitigate overfitting.

### Training Results
- **Validation Accuracy**: 64.75%
- Number of Epochs: 75
- Batch Size: 64

---

## Results
The model achieved a validation accuracy of **64.75\%**, demonstrating the potential of the proposed architecture for automating cardiomegaly classification. While promising, further improvements are needed to address class imbalance and generalization challenges.

---

## Installation
To set up the environment and dependencies, follow these steps:
1. Clone the repository:
   ```bash
   git clone https://github.com/your-username/CustomCNNWithAttention.git
