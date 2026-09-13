# Smart Study Monitor 🧠

### Real-Time AI Study Focus Monitoring with Computer Vision

Smart Study Monitor is a Python-based computer-vision project that monitors a student's study session through a webcam and provides audio warnings for common distractions and loss of attention.

## ✨ Features

- 😴 **Sleep / Drowsiness Detection** — monitors eye landmarks and detects prolonged eye closure.
- 🙈 **Face-Cover Detection** — warns when the user's face is no longer visible for a sustained period.
- 📱 **Phone Detection** — uses a lightweight YOLO model to detect a cell phone in the camera frame.
- 🔊 **Audio Alerts** — plays separate warning sounds for sleep, face-cover, and phone events.
- 👁️ **Real-Time Webcam Processing** — processes frames continuously using OpenCV.
- 📊 **Eye Ratio Feedback** — displays the calculated eye ratio during monitoring.

## 🧠 How It Works

```text
Webcam Frame
     ↓
OpenCV Capture
     ↓
Face Mesh ─────→ Eye Ratio ─────→ Sleep Warning
     │
     └──────────→ Face Missing ──→ Face-Cover Warning
     │
     └──→ YOLO Object Detection ─→ Phone Warning
                                      ↓
                                Audio Alert
```

The current implementation uses face landmarks for eye-state monitoring and a COCO-trained YOLO model for cell-phone detection. Warning priority is face covered → sleep → phone.

## 🛠️ Tech Stack

- **Language:** Python
- **Computer Vision:** OpenCV
- **Face Landmark Detection:** cvzone Face Mesh
- **Object Detection:** Ultralytics YOLOv8 Nano
- **Audio:** Pygame Mixer
- **Model/Data:** COCO-pretrained YOLO model

## 📁 Project Files

| File | Purpose |
|---|---|
| `app.py` | Main real-time monitoring application |
| `yolov8n.pt` | YOLOv8 Nano model file tracked through Git LFS |
| `face_landmarker.task` | Face landmark model asset |
| `hand_landmarker.task` | Hand landmark model asset |
| `alarm.mp3` | Sleep warning audio |
| `faudio.mp3` | Face-cover warning audio |
| `paudio.mp3` | Phone warning audio |

## 🚀 Installation

### 1. Clone the repository

```bash
git clone https://github.com/codewithyogeshh/Smart_Study_Monitor.git
cd Smart_Study_Monitor
```

### 2. Create a virtual environment

```bash
python -m venv venv
```

Windows PowerShell:

```powershell
.\venv\Scripts\Activate.ps1
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Run

```bash
python app.py
```

Press **Q** in the OpenCV window to exit.

## ⚠️ Notes

- A working webcam and audio output are required.
- YOLO model files are managed with Git LFS in this repository.
- Detection thresholds are prototype settings and may need calibration for different cameras and lighting conditions.
- This is a study/productivity prototype, not a medical diagnostic system.

## 🔮 Future Improvements

- Session analytics and study-time reports
- Better drowsiness estimation using both eyes
- Configurable alert thresholds
- Dashboard for focus statistics
- Additional distraction detection
- More robust low-light and camera handling

## 👨‍💻 Author

**Yogesh Chavan**  
Computer Science & Engineering Student

GitHub: [@codewithyogeshh](https://github.com/codewithyogeshh)
