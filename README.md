# Deep Learning-Based Framework for Real-Time Detection and Classification of Lemon Plant Leaf Diseases

This repository serves as the **official research artifact repository for the manuscript submitted to the journal *The Visual Computer***.

The associated manuscript is titled:

**Deep Learning-Based Framework for Real-Time Detection and Classification of Lemon Plant Leaf Diseases**

This project presents an **AI-powered mobile system for detecting lemon plant leaf diseases and generating treatment recommendations in real time**. The system combines deep learning, computer vision, and large language models to support early disease diagnosis and assist farmers with actionable treatment guidance.

The proposed framework integrates a **hybrid machine learning pipeline** consisting of:

- **One-Class Support Vector Machine (OC-SVM)** for novelty detection to ensure that only lemon leaf images are processed.
- **MobileNetV2-based Convolutional Neural Network (CNN)** for classification of lemon leaf conditions.
- **Large Language Model (LLM)** based advisory system for generating treatment recommendations.

The system is designed for **mobile deployment**, allowing farmers to capture leaf images directly using their smartphones and receive instant diagnostic results and treatment advice.

---

# System Architecture

The overall workflow of the system is illustrated below:

Mobile Application  
→ Backend API  
→ AI Inference Server  
→ Hybrid Model (OC-SVM + MobileNetV2)  
→ Disease Prediction  
→ Treatment Recommendation Service  
→ Results displayed to the user

---

# Project Repositories

This project is implemented across multiple repositories, each responsible for a different system component.

### AI Inference Service
Performs plant disease detection using the trained hybrid deep learning model.

Repository:  
https://github.com/Muhammad-Faizan-Soomro/precision-plant-care-model

---

### Backend API
Handles user authentication, image uploads, and communication between the mobile application and the AI inference service.

Repository:  
https://github.com/SHERRY699/Precision-Plant-Care-Backend

---

### Mobile Application
Mobile interface allowing users to capture plant leaf images and view disease predictions and treatment recommendations.

Repository:  
https://github.com/SHERRY699/Precision-Plant-Care

---

### Treatment Recommendation Service
Generates treatment advice based on disease predictions using a large language model.

Repository:  
https://github.com/SHERRY699/treatment-bot

---

# Disease Classes

The model currently detects three categories of lemon leaf conditions:

- Healthy Leaf
- Black Spot Disease
- Leaf Curl Disease

---

# Dataset

The dataset consists of **lemon leaf images collected under real-world conditions using smartphone cameras**.

Dataset characteristics:

- Healthy leaves
- Leaves affected by black spot disease
- Leaves affected by leaf curl disease
- Variations in lighting, orientation, and background

To improve generalization, the dataset was augmented using:

- image rotation
- horizontal and vertical flipping
- brightness adjustments
- zoom transformations

Dataset DOI:  
https://doi.org/10.5281/zenodo.18916104

---

# Reproducibility Guide

To reproduce the system:

### 1. Run the AI Inference Server (Quick Testing Option)

For ease of use and quick experimentation, users can **test the disease prediction model by running the AI inference server independently**. The inference server includes a built-in web interface that allows users to upload leaf images directly and obtain disease predictions without running the full system stack.

Steps:

Clone the AI repository and install dependencies.

`pip install -r requirements.txt`

Run the Flask server:

`python app.py`

Once the server starts, open the provided local URL in a browser.  
The interface allows users to:

- upload a lemon leaf image
- run the hybrid prediction pipeline
- view the predicted disease class and confidence score

This option provides a **simple standalone way to evaluate the trained model** without deploying the backend API, mobile application, or recommendation service.

---

### 2. Start the Backend API

Install dependencies:

`npm install`

Run the server:


`node index.js`

---

### 3. Deploy the Treatment Recommendation Service

Install dependencies:

`pip install -r requirements.txt`

Run the FastAPI server:

`uvicorn app:app --host 0.0.0.0 --port 8000`

---

### 4. Run the Mobile Application

Install dependencies:

`npm install`

Start the Expo development server:

`npx expo start`

Open the app using Expo Go on a mobile device.

---

# Code Availability

All source code used in this research is publicly available via the repositories listed above.

This repository serves as the **central research artifact repository** linking all system components to ensure transparency and reproducibility.

Code DOI:  
https://doi.org/10.5281/zenodo.18921366

---

# License

This project is released under the **MIT License**.

See the LICENSE file for details.

---

# Citation

If you use this code or system in your research, please cite the following manuscript:


Deep Learning-Based Framework for Real-Time Detection and Classification of Lemon Plant Leaf Diseases

---

# Acknowledgment

This project was developed as part of research on AI-assisted plant disease detection systems to support precision agriculture and improve crop monitoring using mobile technologies.
