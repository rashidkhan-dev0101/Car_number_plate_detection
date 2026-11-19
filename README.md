
# 🚗 AI Car Number Plate Detection System

An AI-powered vehicle license plate detection system built using **Python, PyTorch, and YOLOv8**. The project uses computer vision to locate vehicle number plates in images and video streams using bounding-box detection.

The goal is to develop a real-time detection application that can identify license plates through a laptop webcam and eventually through a browser-based web application.

\<p align="center">   \<img src="[https://img.shields.io/badge/Python-3.10%2B-blue?logo=python](https://img.shields.io/badge/Python-3.10%2B-blue?logo=python)" />   \<img src="[https://img.shields.io/badge/YOLOv8-Ultralytics-purple](https://img.shields.io/badge/YOLOv8-Ultralytics-purple)" />   \<img src="[https://img.shields.io/badge/PyTorch-Deep%20Learning-ee4c2c?logo=pytorch](https://img.shields.io/badge/PyTorch-Deep%20Learning-ee4c2c?logo=pytorch)" />   \<img src="[https://img.shields.io/badge/OpenCV-Computer%20Vision-green?logo=opencv](https://img.shields.io/badge/OpenCV-Computer%20Vision-green?logo=opencv)" />   \<img src="[https://img.shields.io/badge/Status-In%20Development-orange](https://img.shields.io/badge/Status-In%20Development-orange)" /> \</p>

---

## 📌 Project Overview

Car number plate detection is an important application of computer vision used in intelligent transportation systems, smart parking, traffic monitoring, and vehicle identification.

This project uses a custom-trained YOLOv8 model to detect license plates in vehicle images.

The model predicts the location of a number plate and draws a bounding box around it, along with a confidence score.

**Main objective:** Build a complete AI-powered number plate detection system that supports image uploads, live webcam detection, and browser-based camera detection.

## ✨ Planned Features

- [x] Kaggle dataset integration
- [x] Google Colab GPU setup
- [x] YOLOv8 model training
- [x] Custom-trained model export (`best.pt`)
- [x] Download trained model for local development
- [x] Local webcam detection
- [ ] Image upload and detection
- [ ] FastAPI backend
- [ ] Postman API testing
- [ ] Real-time browser camera detection
- [ ] Bounding boxes and confidence scores
- [ ] Video-based number plate detection
- [ ] OCR integration to read number plate characters

*Features are marked complete only after implementation and testing.*

## 🧠 Model Information

| Component            | Technology                  |
| -------------------- | --------------------------- |
| Model                | YOLOv8n                     |
| Task                 | Object Detection            |
| Framework            | Ultralytics                 |
| Deep Learning        | PyTorch                     |
| Dataset              | Car License Plate Detection |
| Annotation Format    | Pascal VOC (XML)            |
| Training Environment | Google Colab                |
| GPU                  | NVIDIA Tesla T4             |
| Detection Class      | license_plate               |

### Dataset

The model is trained using the Kaggle dataset:

**Car License Plate Detection**

Dataset: [https://www.kaggle.com/datasets/andrewmvd/car-plate-detection](https://www.kaggle.com/datasets/andrewmvd/car-plate-detection)

Dataset information:

- Approximately 433 images.
- License plate bounding-box annotations.
- Pascal VOC XML annotation format.
- One detection class: `license_plate`.

Dataset conversion and preparation are performed before YOLO training.

## 🏗️ Project Architecture

```text
Car Number Plate Detection
│
├── Dataset
│   └── Kaggle License Plate Dataset
│
├── Model Training
│   └── Google Colab
│       └── YOLOv8
│           └── best.pt
│
├── Local Application
│   └── Python + OpenCV
│
├── Backend (Planned)
│   └── FastAPI
│
└── Frontend (Planned)
    └── HTML + CSS + JavaScript
        └── Browser Webcam
```

## 🛠️ Technologies Used

- **Python:** Main programming language.
- **YOLOv8:** License plate object detection.
- **PyTorch:** Deep learning framework.
- **Ultralytics:** YOLO model training and inference.
- **OpenCV:** Image and video processing.
- **Google Colab:** Model training using GPU.
- **FastAPI:** Planned backend API.
- **JavaScript:** Planned browser camera integration.

## 📂 Project Structure

```text
Car_Number_Plate_Detection/
│
├── best.pt
├── test_model.py
├── webcam_detect.py
├── main.py
├── requirements.txt
├── README.md
│
└── venv/
```

The structure will be expanded as the webcam detector, API, and website are implemented.

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/Car_Number_Plate_Detection.git
```

```bash
cd Car_Number_Plate_Detection
```

### 2. Create a virtual environment

```bash
python3 -m venv venv
```

Activate it on macOS or Linux:

```bash
source venv/bin/activate
```

On Windows:

```bash
venv\Scripts\activate
```

### 3. Install dependencies

```bash
pip install -r requirements.txt
```

### 4. Add the trained model

Place your trained YOLO weights file in the project root:

```text
best.pt
```

The model weights are generated by the Google Colab training notebook.

### 5. Verify model loading

```bash
python test_model.py
```

The model should load successfully and display its detection class names.

## 📷 Live Webcam Detection

The planned webcam application will:

1. Request permission to access the webcam.
2. Capture live video frames.
3. Send frames to the YOLO detection model.
4. Identify number plates.
5. Draw bounding boxes around detected plates.
6. Display confidence scores.

The local Python webcam application and browser-based webcam application will be developed and tested separately.

## 🌐 Future Web Application

The planned web application will use the following architecture:

```text
Browser
   │
   │ Webcam / Image Upload
   ▼
JavaScript Frontend
   │
   ▼
FastAPI Backend
   │
   ▼
YOLOv8 Detection Model
   │
   ▼
Detection Results
   │
   ▼
Bounding Boxes + Confidence
```

## 🔍 Object Detection vs OCR

This project initially focuses on **license plate detection**, not character recognition.

- **Object Detection:** Finds the location of the number plate.
- **OCR:** Reads the actual letters and numbers printed on the plate.

OCR will be added as a separate development stage.

## 📊 Model Evaluation

The model will be evaluated using standard object detection metrics:

- Precision
- Recall
- mAP\@50
- mAP\@50-95

Evaluation results and sample predictions will be documented here after final testing.

## 🚀 Future Improvements

- Improve detection accuracy using more diverse images.
- Support multiple number plates in one image.
- Add real-time webcam detection.
- Implement FastAPI endpoints.
- Develop a responsive web interface.
- Add OCR for number plate recognition.
- Support video-based detection.
- Optimize inference speed.

## ⚠️ Limitations

- The initial dataset is relatively small.
- Detection performance can vary with lighting, camera quality, viewing angle, and distance.
- Number plate detection does not automatically recognize the registration characters.
- Real-world reliability requires testing on diverse unseen images and videos.

## 👨‍💻 Developer

**Rashid Khan**

Software Engineering Graduate | Flutter Developer | AI & Machine Learning Enthusiast

Interested in Artificial Intelligence, Computer Vision, Deep Learning, and building practical AI-powered applications.

---

⭐ If you find this project interesting, consider giving the repository a star!

**Project Status:** 🚧 Under Active Development
