# 🎥 Human Activity Recognition using CNN-LSTM

## 📌 Project Overview
This project implements a Hybrid Deep Learning Model (CNN + LSTM) to recognize human activities from video sequences.

The model combines:
- CNN (Convolutional Neural Network) → extracts spatial features from frames
- LSTM (Long Short-Term Memory) → captures temporal dependencies across frames

This project is developed using TensorFlow and trained on Google Colab.

---

## 🎯 Objectives
- Recognize human actions from video data
- Extract spatial and temporal features
- Build an efficient deep learning pipeline for video classification

---

## 📂 Dataset

We used a subset of the UCF101 dataset.

### 📊 Selected Classes (6 Activities)

- WalkingWithDog → Walking with a dog
- JumpingJack → Jumping jacks
- PushUps → Push ups
- Basketball → Playing basketball
- SoccerJuggling → Soccer juggling
- VolleyballSpiking → Volleyball spiking

---

## ⚙️ Dataset Configuration

- Image Size: 64 × 64
- Frames per Video: 10
- Videos per Class: 40
- Total Classes: 6
- Total Samples: ~240 videos

---

## 🧠 Model Architecture

### 🔹 CNN Feature Extractor
- Conv2D (32 filters, 3×3)
- Batch Normalization
- MaxPooling
- Conv2D (64 filters)
- Batch Normalization
- MaxPooling
- Conv2D (128 filters)
- MaxPooling
- Flatten layer

---

### 🔹 LSTM Sequence Model
- LSTM (128 units, return sequences)
- Dropout (0.3)
- LSTM (64 units)
- Dropout (0.3)

---

### 🔹 Fully Connected Layers
- Dense (64 neurons, ReLU)
- Output Layer (6 neurons, Softmax)

---

## 🛠️ Training Configuration

- Optimizer: Adam
- Loss Function: Categorical Crossentropy
- Batch Size: 8
- Epochs: 20
- Callback: EarlyStopping

---

## 🔄 Data Preprocessing

- Extract frames from videos
- Resize frames to 64×64
- Normalize pixel values (0–1)

---

## 🔁 Data Augmentation

Applied techniques:
- Random horizontal flip
- Random brightness adjustment
- Random contrast adjustment

---

## 📊 Evaluation Metrics

- Accuracy
- Loss
- Confusion Matrix
- Classification Report

---

## 📈 Results

The model successfully learns spatial and temporal patterns from video sequences and achieves good performance given the limited dataset size.

---

## 🧪 Prediction Output Example

Prediction:
The person is doing jumping jacks ⭐

Confidence:
92.5%

---

## 🚀 How to Run

1. Open Google Colab
2. Upload notebook
3. Run all cells sequentially
4. Test using sample video

---

## 📌 Key Features

- CNN + LSTM Hybrid Architecture
- Video-based classification
- Data augmentation for better generalization
- Visualization (accuracy, loss, confusion matrix)

---



## ⭐ Notes

A subset of 6 classes was selected to ensure faster training and stable performance within limited computational resources (Google Colab).
