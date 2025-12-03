# Smart-Waste-Segregation-System-OpenCV-CNN-
🗑️ Smart Waste Segregation System using OpenCV &amp; CNN  This project implements an AI-powered waste classification system capable of identifying four waste categories — Organic, Plastic, Paper, and Metal — in real time. The system uses a MobileNetV2-based Convolutional Neural Network (CNN) along with OpenCV to perform live detection using a webcam.

🚀 Features

Real-time waste detection using webcam

Trained MobileNetV2 model for accurate classification

Organized dataset pipeline with data augmentation

High accuracy (~94% validation accuracy)

Automatic bounding box + label display

Lightweight model suitable for edge devices

🧠 Tech Stack

Python

TensorFlow / Keras

OpenCV

NumPy

Pillow

Matplotlib

📂 Project Structure
Smart Waste/
│
├── dataset/
│   ├── metal/
│   ├── organic/
│   ├── paper/
│   └── plastic/
│
├── models/
│   └── waste_mobilenet.h5
│
├── src/
│   ├── prepare_dataset.py
│   ├── train_mobilenet.py
│   └── realtime_detect.py
│
└── README.md

📝 How It Works

Dataset Preparation
Images are organized into categories and preprocessed for training.

Model Training
MobileNetV2 is used as the base model with fine-tuned layers.
The final model achieves high accuracy on the validation dataset.

Real-Time Detection
The trained model is loaded and used to classify frames captured from the webcam.

▶️ Running the Project
1. Train the Model
python src/train_mobilenet.py


Model will be saved to models/waste_mobilenet.h5.

2. Run Real-Time Detection
python src/realtime_detect.py

📸 Output Example

Webcam feed with label overlay

Class: Organic / Metal / Paper / Plastic

Confidence score

📚 Applications

Smart waste bins

Recycling plants

Automated waste segregation

IoT-based environmental solutions

🛑 README for Project 2 — Driver Drowsiness Detection System (OpenCV + dlib)
🚗 Driver Drowsiness Detection using Eye Aspect Ratio (EAR)

This project detects driver drowsiness in real-time using facial landmarks and Eye Aspect Ratio (EAR) measurement. When the driver closes their eyes for more than 4 seconds, an alarm automatically plays in the background.
If the driver's eyes remain open for more than 5 seconds, the alarm stops.

✨ Features

Real-time eye detection using webcam

Eye aspect ratio–based drowsiness monitoring

Background alarm audio (non-blocking)

Auto-start alarm when eyes closed for >4 sec

Auto-stop alarm when eyes open for >5 sec

Fast and lightweight

🧠 Tech Stack

Python

OpenCV

dlib

Pygame (for audio playback)

NumPy

📂 Project Structure
DrowsinessDetection/
│
├── alarm.mp3
├── shape_predictor_68_face_landmarks.dat
├── drowsy_detect.py
└── README.md

🔧 How It Works

dlib landmark detector finds the eyes

EAR value is calculated for left & right eye

If EAR < threshold for 4 seconds → Alarm ON

If EAR > threshold for 5 seconds → Alarm OFF

Alarm audio is played in background (non-blocking)

▶️ Running the Project
python drowsy_detect.py


Press Q to quit.

📸 Output

Live webcam feed with:.

Eye boundary tracking

Real-time EAR value

Alerts for "Eyes Closed" & "Drowsiness Detected"
