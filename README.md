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
| [![Watch the Video](Face-Smile-Detection-video.mp4)] |
| *Click the dynamic blueprint button above to access the recorded execution media* |

> 💡 **Note:** Make sure to replace `YOUR_GOOGLE_DRIVE_OR_YOUTUBE_LINK_HERE` with your actual Google Drive video share link.

---

## 🗺️ Environment & Classifier Mapping

To maintain high architectural pipeline processing standards without frame lagging, the following structural dependencies and variables were mapped:

| Component / File | Framework | Core Function | Configuration Parameters |
| :--- | :--- | :--- | :--- |
| **`haarcascade_frontalface_default.xml`** | OpenCV Core | Default Frontal Face Detection Model | `scaleFactor=1.3`, `minNeighbors=5` |
| **`haarcascade_smile.xml`** | OpenCV Core | Granular Smile Extraction Module | `scaleFactor=1.8`, `minNeighbors=20` |
| **`cv2.VideoCapture(1)`** | Local OS Peripheral | Live Virtual Stream Allocation via Iriun | Device Port ID Setup: Index `1` |

---

## 📋 Step-by-Step Implementation Guide

Follow these sequential steps to replicate or deploy this production workspace inside your computer environment:

### Step 1: Setting up the Environment
1. Open your integrated development workspace terminal in **Visual Studio Code**.
2. Initialize or activate your stable **Anaconda Python Environment** where core libraries reside.
3. Install the optimized binary framework packages by executing the following package manager terminal command:
   ```bash
   pip install opencv-python numpy
