# 🖐️ Volume Hand Control 

This project enables you to control your system's audio volume using just your hand gestures, captured through a webcam! It leverages computer vision with **OpenCV**, **MediaPipe**, and **pycaw**.

## 🛠️ Features

- Real-time hand tracking using MediaPipe
- Fingertip detection (thumb and index)
- Volume control based on hand distance
- Visual feedback with bars and FPS counter
- Modular code structure using a custom `HandTrackingModule`

---

## 📁 Project Structure
```bash
 ├── HandTrackingModule.py # Hand detection and position extraction(common hand tracking module) 
 ├── HandTrackingMin.py # Simple hand tracking (used in the project) 
 ├── VolumehandControl.py # Main program to control volume 
```
---

## 📦 Requirements

Install the required packages using pip:

```bash
pip install opencv-python mediapipe comtypes pycaw numpy
```
⚠️ Make sure your webcam is connected and accessible by OpenCV.

## 🚀 How to Run
Clone the repository:
```bash
git clone https://github.com/sumukhpshetty25/Volume-hand-control.git
cd Volume-hand-control
```
Run the main script
- Move your thumb and index finger closer or farther apart to control the system volume.

## ✨ How It Works
MediaPipe detects your hand and provides 21 landmark points.

We track landmarks 4 (thumb tip) and 8 (index tip).

The distance between them is mapped to a volume level using numpy.interp.

Volume is set using pycaw (Windows only).

## 📷 Reference
MediaPipe Hands Documentation

pycaw GitHub
