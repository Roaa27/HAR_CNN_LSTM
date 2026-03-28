# 🎥 Human Activity Recognition using CNN-LSTM (UCF101)

## 📌 Project Overview
This project implements a Deep Learning model for Human Activity Recognition (HAR) using a hybrid architecture of CNN and LSTM.

The model is trained on video data and is capable of classifying human actions based on sequences of frames.

---

## 🎯 Objective
To classify human activities from videos by combining:
- CNN for spatial feature extraction (from frames)
- LSTM for temporal sequence learning (between frames)

---

## 📂 Dataset
We used the UCF101 dataset.

Dataset link:
https://www.crcv.ucf.edu/data/UCF101/

---

## 🏷️ Selected Classes (15 Classes)

- WalkingWithDog
- JumpingJack
- PushUps
- Basketball
- SoccerJuggling
- VolleyballSpiking
- TennisSwing
- Punch
- PlayingGuitar
- PlayingPiano
- GolfSwing
- HorseRiding
- SkateBoarding
- Surfing
- Bowling

---

## ⚙️ Data Preprocessing

- Extracted frames from each video
- Selected 10 frames per video
- Resized frames to 64×64 pixels
- Normalized pixel values to range [0, 1]

---

## 🧠 Model Architecture

### 🔹 CNN Feature Extractor
- Conv2D (16 filters)
- MaxPooling
- Conv2D (32 filters)
- MaxPooling
- Conv2D (64 filters)
- MaxPooling
- Flatten layer

---

### 🔹 LSTM Sequence Model
- LSTM (64 units)
- Dropout (0.5)

---

### 🔹 Fully Connected Layers
- Dense (64 neurons, ReLU)
- Output Layer (15 classes, Softmax)

---

## 🛠️ Training Configuration

- Optimizer: Adam
- Loss Function: Categorical Crossentropy
- Batch Size: 8
- Epochs: 10
- Validation Split: 20%

---

## 📊 Evaluation Metrics

The model is evaluated using:

- Accuracy
- Loss
- Confusion Matrix

---

## 📈 Visualization

The project includes:

- Training vs Validation Accuracy graph
- Training vs Validation Loss graph
- Confusion Matrix heatmap

---

## 🧪 Prediction Example

The model predicts the activity from a video and returns confidence score.

Example Output:

Prediction: Jumping Jack  
Confidence: 87.3%

---

## 🚀 How to Run

1. Open Google Colab
2. Upload notebook
3. Run all cells sequentially
4. Test model using:

```python
test_video("path_to_video.avi")
