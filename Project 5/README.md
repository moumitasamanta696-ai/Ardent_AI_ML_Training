# 🎭 Real-Time Emotion Detection System

<p align="center">
  <img src="https://img.shields.io/badge/Python-3.8%2B-blue?style=for-the-badge&logo=python&logoColor=white"/>
  <img src="https://img.shields.io/badge/OpenCV-4.x-green?style=for-the-badge&logo=opencv&logoColor=white"/>
  <img src="https://img.shields.io/badge/Keras-Deep%20Learning-red?style=for-the-badge&logo=keras&logoColor=white"/>
  <img src="https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge"/>
</p>

<p align="center">
  A real-time facial emotion recognition system built with OpenCV and a custom-trained deep learning model — no external APIs required.
</p>

<p align="center">
  <a href="https://github.com/moumitasamanta696-ai/portfolio">🌐 Portfolio</a> &nbsp;|&nbsp;
  <a href="https://github.com/moumitasamanta696-ai">👩‍💻 GitHub Profile</a>
</p>

---

## 📌 Overview

This project performs **real-time facial emotion detection** directly from a webcam feed using computer vision and a pre-trained convolutional neural network (CNN). It classifies human faces into **7 emotional states** without relying on third-party services like DeepFace or cloud APIs — making it fast, offline-capable, and fully transparent.

---

## 🎯 Detected Emotions

| Label     | Description                        |
|-----------|------------------------------------|
| 😠 Angry   | Expressions of anger or frustration |
| 🤢 Disgust | Disgust or repulsion                |
| 😨 Fear    | Fearful or anxious expressions      |
| 😊 Happy   | Smiling or joyful expressions       |
| 😢 Sad     | Sadness or sorrow                   |
| 😲 Surprise| Surprise or shock                   |
| 😐 Neutral | Calm, expressionless face           |

---

## 🛠️ Tech Stack

- **Python** — Core programming language
- **OpenCV** — Real-time video capture and face detection (Haar Cascade)
- **Keras / TensorFlow** — Deep learning model loading and inference
- **NumPy** — Image preprocessing and array manipulation

---

## 📁 Project Structure

```
emotion-detection/
│
├── emotion_detection.py              # Main application script
├── emotion_model.hdf5                # Pre-trained CNN emotion model
├── haarcascade_frontalface_default.xml  # OpenCV face detector
└── README.md
```

---

## ⚙️ How It Works

1. **Face Detection** — OpenCV's Haar Cascade classifier scans each video frame to locate faces in real time.
2. **ROI Extraction** — The detected face region is isolated, converted to grayscale, and resized to `64×64` pixels.
3. **Preprocessing** — Pixel values are normalized to `[0, 1]` and reshaped to match the model's expected input format `(1, 64, 64, 1)`.
4. **Emotion Prediction** — The pre-trained CNN predicts probabilities across 7 emotion classes; the highest-confidence label is selected.
5. **Visualization** — A bounding box and emotion label are overlaid on the live video feed in green.

---

## 🚀 Getting Started

### Prerequisites

Make sure you have Python 3.8+ installed. Then install the required packages:

```bash
pip install opencv-python numpy keras tensorflow
```

### Clone the Repository

```bash
git clone https://github.com/moumitasamanta696-ai/emotion-detection.git
cd emotion-detection
```

### Run the Application

```bash
python emotion_detection.py
```

> Press **`q`** to quit the application.

---

## 📷 Platform Notes

- **macOS**: The script uses `cv2.CAP_AVFOUNDATION` for Mac-compatible webcam capture — no configuration needed.
- **Windows/Linux**: You may replace `cv2.VideoCapture(0, cv2.CAP_AVFOUNDATION)` with `cv2.VideoCapture(0)` for broader compatibility.

---

## 🧠 Model Details

| Property         | Value              |
|------------------|--------------------|
| Input Shape      | `(64, 64, 1)` — Grayscale |
| Output Classes   | 7 Emotion Labels   |
| Model Format     | `.hdf5` (Keras)    |
| Inference Mode   | CPU / GPU          |

The model was trained on facial expression datasets and saved in HDF5 format, loaded at runtime without recompilation for fast startup.

---

## 📈 Future Improvements

- [ ] Add confidence score display alongside emotion labels
- [ ] Support multi-face detection simultaneously
- [ ] Export emotion logs to CSV for analysis
- [ ] Build a GUI dashboard with real-time emotion graphs
- [ ] Train on a larger, more diverse dataset to improve accuracy

---

## 👩‍💻 Author

**Moumita Samanta**

- 🌐 Portfolio: [github.com/moumitasamanta696-ai/portfolio](https://github.com/moumitasamanta696-ai/portfolio)
- 💻 GitHub: [github.com/moumitasamanta696-ai](https://github.com/moumitasamanta696-ai)

---

## 📄 License

This project is open-source and available under the [MIT License](LICENSE).

---

<p align="center">
  ⭐ If you found this project useful, please consider giving it a star!
</p>
