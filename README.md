# 🤖 Smart Prosthetic Hand Controlled by EMG Signals and Machine Learning

A low-cost, intelligent prosthetic hand that replicates natural hand gestures using EMG signals and a lightweight machine learning model. This system enables users to open and close a prosthetic hand using muscle signals from their forearm, processed in real time.

---

## 📌 Project Overview

This project combines:  
- **EMG signal acquisition**  
- **Arduino-based motor control**  
- **Raspberry Pi-based gesture prediction using a TFLite model**

The final output is a responsive prosthetic hand capable of mimicking basic gestures like **open** and **close** using six servo motors.

---

## 🧠 System Architecture

```
EMG Sensor (V3 Electrodes)
       │
       ▼
Arduino (Reads EMG analog values)
       │
Serial Communication (USB)
       ▼
Raspberry Pi (Predicts gesture using ML)
       │
Gesture command (Open/Close)
       ▼
Arduino (Controls 6 Servo Motors)
       ▼
Prosthetic Hand Movement
```

---

## 🧰 Hardware Used

- EMG Sensor (Myoware or V3 electrodes)  
- Arduino Uno  
- Raspberry Pi 5  
- 6x Servo Motors  
- 3D-Printed or mechanical prosthetic hand frame  
- Jumper wires, breadboard  

---

## 🛠️ Software & Libraries

- Arduino IDE  
- Python 3  
- TensorFlow Lite  
- NumPy  
- tflite-runtime  
- Serial communication (pySerial)

---

## 🧾 File Structure

```
prosthetic-hand-emg-ml/
├── Arduino_Code/
│   └── prosthetic_hand.ino
├── RaspberryPi_Code/
│   ├── predict_gesture.py
│   └── model.tflite
├── images/
│   ├── circuit_diagram.png
│   ├── workflow_chart.png
│   └── prosthetic_hand_photo.jpg
├── report/
│   └── report_PDF.pdf
├── README.md
└── LICENSE
```

---

## 🚀 How It Works

1. **Arduino reads EMG values** from analog pin and sends them to the Raspberry Pi.  
2. **Raspberry Pi preprocesses** the signal into a 50-length input vector.  
3. **TensorFlow Lite model** predicts the gesture ("open" or "close").  
4. **Gesture command** is sent back to Arduino over serial.  
5. **Arduino controls servo motors** to perform the hand movement.

---

## 🤖 Machine Learning Model

- Model Type: Sequential 1D CNN  
- Input Shape: (1, 50, 1) EMG time-series  
- Output: Binary (0 = Close, 1 = Open)  
- Framework: TensorFlow Lite (for edge deployment)

---

## 🎯 Results

- Real-time prediction latency: < 1 second  
- Prediction accuracy: ~98% on test samples  
- Smooth servo actuation for open/close gestures

---

## 📸 Images

  
*Workflow Diagram*


*Final Setup*

---

## 🧪 Demo



---
