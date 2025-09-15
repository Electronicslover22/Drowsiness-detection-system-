# 🚗 Drowsiness Detection System with Arduino Controlled Car

This project is a **Computer Vision + Embedded Systems** based solution that detects driver drowsiness using a camera and automatically controls a toy car for safety.

## 📌 Project Overview
- Uses a **USB-connected phone camera** (via DroidCam) for real-time face monitoring.
- **Python + OpenCV + MediaPipe** detect eyes and track eye closure duration.
- If both eyes remain closed for more than **3 seconds**, Python sends a signal to **Arduino** via Serial USB.
- Arduino reduces the **car’s speed**, turns on the **left indicator**, and uses **ultrasonic obstacle avoidance** to safely steer the car aside.

## ⚙️ Features
- 👀 **Eye Tracking** with EAR (Eye Aspect Ratio).
- 💤 **Drowsiness Alert** when eyes stay closed for threshold time.
- 🔗 **Python ↔ Arduino Serial Communication**.
- 🚘 **Car Safety Control**: 
  - Speed reduction  
  - Left indicator blinking  
  - Automatic side movement with obstacle avoidance  

## 🛠️ Hardware Requirements
- Arduino Uno / Nano  
- Motor Driver (L298N / TB6612FNG)  
- DC motors with toy car chassis  
- Ultrasonic sensor (HC-SR04)  
- Left/Right indicator LEDs  
- Phone camera (via DroidCam / USB webcam)  
- Laptop with Python  

## 💻 Software Requirements
- Python 3.8–3.11 (64-bit recommended)  
- Libraries: `opencv-python`, `mediapipe`, `pyserial`  
- Arduino IDE for motor control code  

## 🚀 Setup & Usage
1. Connect phone camera as USB webcam using **DroidCam**.  
2. Run the Python script:  
   ```bash
   python drowsiness_to_arduino.py

