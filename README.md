# Real-Time Face & Smile Detection Task

This repository provides a comprehensive guide, setup execution workflow, and source code for detecting human faces and capturing smiling moments in real-time. The project was designed and implemented using OpenCV to fulfill precise computer vision cascading and frame-processing benchmarks.

---

## 🎯 Task Objectives

1. **Phase 1 (Face Detection):** Stream live feed and initialize the primary cascade classifier to identify human faces, dynamically binding them within a structural blue bounding box.
2. **Phase 2 (Smile Tracking):** Isolate the region of interest (ROI) of the detected face, engage the secondary cascade analyzer, and track smiles instantaneously with a green bounding box annotation.

---

## 🎬 Project Demonstration

To review the actual physical execution and response parameters of the computer vision pipeline, refer to the demonstration table below:

| Functional System Demo |
| :---: |
| [![Watch the Video](https://img.shields.io/badge/PLAY-Project%20Demo%20Video-green?style=for-the-badge&logo=youtube)](Face-Smile-Detection-video.mp4) |
| *Click the dynamic blueprint button above to access the uploaded execution media* |

---

## 🗺️ Environment & Classifier Mapping

To maintain high architectural pipeline processing standards without frame lagging, the following structural dependencies and variables were mapped:

| Component / File | Framework | Core Function | Configuration Parameters |
| :--- | :--- | :--- | :--- |
| **`haarcascade_frontalface_default.xml`** | OpenCV Core | Default Frontal Face Detection Model | `scaleFactor=1.3`, `minNeighbors=5` |
| **`face_smile_detection.txt`** | Python Source | Production Script Implementation | Embedded Hardware Port Index `1` |
| **`Face-Smile-Detection-video.mp4`** | Output Media | Recorded System Operational Demo | High-definition Framework Verification |

---

## 📋 Step-by-Step Implementation Guide

Follow these sequential steps to replicate or deploy this production workspace inside your computer environment:

### Step 1: Setting up the Environment
1. Open your integrated development workspace terminal in **Visual Studio Code**.
2. Initialize or activate your stable **Anaconda Python Environment** where core libraries reside.
3. Install the optimized binary framework packages by executing the following package manager terminal command:
   ```bash
   pip install opencv-python numpy
### Step 2: Workspace Dependency Verification
1. Ensure the pre-trained structural configuration model file `haarcascade_frontalface_default.xml` is present in the absolute root path of your directory.
2. Ensure your smart mobile camera utility platform (**Iriun Webcam**) is fully linked and running in the background.

### Step 3: Setting Up the Production File
1. Locate the standalone text script file named `face_smile_detection.txt` inside your repository.
2. Change the file extension from `.txt` to `.py` (to become `face_smile_detection.py`) so it can be executed by the Python compiler.

### Step 4: Executing the Computer Vision Task
1. Run the Python execution script from your integrated terminal environment:
   ```bash
   python face_smile_detection.py

### 💻 Production Source Code
import cv2

# Initialize core pre-trained cascade architecture classifiers
face_cascade = cv2.CascadeClassifier('haarcascade_frontalface_default.xml')
smile_cascade = cv2.CascadeClassifier(cv2.data.haarcascades + 'haarcascade_smile.xml')

# Allocate live video streaming channel interface via webcam index
cap = cv2.VideoCapture(1)

print("\n" + "="*50)
print(" System Status: OpenCV Project is running successfully!")
print(" Instructions : Press 'q' or 'ESC' to exit safely.")
print("="*50 + "\n")

while True:
    ret, frame = cap.read()
    if not ret:
        break
        
    # Convert BGR frame space to grayscale to maximize tracking throughput
    gray = cv2.cvtColor(frame, cv2.COLOR_BGR2GRAY)
    
    # Process multi-scale detection matrix parameters for facial tracking
    faces = face_cascade.detectMultiScale(gray, scaleFactor=1.3, minNeighbors=5)
    
    for (x, y, w, h) in faces:
        # Render tracking geometries for face classification
        cv2.rectangle(frame, (x, y), (x+w, y+h), (255, 0, 0), 2)
        cv2.putText(frame, 'Face Detected', (x, y-10), cv2.FONT_HERSHEY_SIMPLEX, 0.6, (255, 0, 0), 2)
        
        # Segment and slice specific Region of Interest matrix for sub-cascades
        roi_gray = gray[y:y+h, x:x+w]
        roi_color = frame[y:y+h, x:x+w]
        
        # Parse localized tracking bounds for sub-facial expressions
        smiles = smile_cascade.detectMultiScale(roi_gray, scaleFactor=1.8, minNeighbors=20)
        
        for (sx, sy, sw, sh) in smiles:
            # Render tracking boundaries for smile validation
            cv2.rectangle(roi_color, (sx, sy), (sx+sw, sy+sh), (0, 255, 0), 2)
            cv2.putText(frame, 'Smiling!', (x, y+h+25), cv2.FONT_HERSHEY_SIMPLEX, 0.6, (0, 255, 0), 2)
            
    # Project final integrated real-time detection window overlay
    cv2.imshow('Face & Smile Recognition Project', frame)
    
    # Evaluate interrupt handling criteria
    key = cv2.waitKey(1) & 0xFF
    if key == ord('q') or key == 27:
        break

# Safely release hardware interface and clear processing memory buffers
cap.release()
cv2.destroyAllWindows()
cv2.waitKey(1)

print("\n" + "="*50)
print(" System Status: Camera closed successfully.")
print("="*50 + "\n")
