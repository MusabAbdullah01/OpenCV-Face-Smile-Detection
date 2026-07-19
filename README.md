# Real-Time Face & Smile Detection Task

This repository provides a comprehensive guide, setup execution workflow, and source code for detecting human faces and capturing smiling moments in real-time. The project was designed and implemented using OpenCV to fulfill precise computer vision cascading and frame-processing benchmarks.

---

## 🎯 Task Objectives

1. **Phase 1 (Face Detection):** Stream live feed and initialize the primary cascade classifier to identify human faces, dynamically binding them within a structural blue bounding box.
2. **Phase 2 (Smile Tracking):** Isolate the region of interest (ROI) of the detected face, engage the secondary cascade analyzer, and track smiles instantaneously with a green bounding box annotation.

---

## 🎬 Project Demonstration

To review the actual physical execution and response parameters of the computer vision pipeline, refer to the demonstration table below:

![Smile Detection](Real-Time%20Face%20&%20Smile%20Detection_image.png)


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


