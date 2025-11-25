# YOLO_Vehicle_Detection

## YOLO Model Deployment Guide

This repository provides instructions to run and deploy a custom YOLO model for object detection using a Jupyter Notebook and Python environment. The steps below guide you from model setup in Google Colab to running inference locally.

---

### Table of Contents
1. [Prerequisites](#prerequisites)  
2. [Setting Up in Google Colab](#setting-up-in-google-colab)  
3. [Downloading and Extracting the Model](#downloading-and-extracting-the-model)  
4. [Local Deployment with Conda](#local-deployment-with-conda)  
5. [Running Inference](#running-inference)  

---

### Prerequisites
- Anaconda / Miniconda installed on your system  
- Python 3.12 compatible environment  
- Access to Google Colab  

---

### Setting Up in Google Colab
1. Open the provided Jupyter Notebook: **`collab code.ipynb`**  
2. Select your runtime hardware accelerator: **T4 GPU**  
3. Download your trained YOLO model file (`my_model.pt`) from Colab.  

---

### Downloading and Extracting the Model
1. If your model is in a compressed file, extract it using Anaconda Prompt or any archive tool.  
2. Ensure the extracted folder contains the `my_model.pt` file.  

---

### Local Deployment with Conda
Follow these steps to set up a Python environment and install dependencies:

#### Create and activate a new conda environment
-`conda create --name yolo-env1 python=3.12 -y`
-`conda activate yolo-env1`

#### Navigate to the folder containing your model (Windows example)
-`cd H:\YOLO\my_model`
-`H:`

#### Install required Python dependencies
`pip install ultralytics`

#### Download the deployment script if not included
-`curl -o yolo_detect.py https://www.ejtech.io/code/yolo_detect.py`

---

### Running Inference
#### You can run the model on videos or live camera feeds as follows:
#### Run inference on a video file
-`python yolo_detect.py --model my_model.pt --source vid1.mp4`

#### Run inference on a USB camera with 1280x720 resolution
-`python yolo_detect.py --model my_model.pt --source usb0 --resolution 1280x720`

---

