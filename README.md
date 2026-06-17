# 🩻 VisionAI: MURA Dataset Classification & Explainable X-Ray Analysis

<p align="center">
  <img src="https://ars.els-cdn.com/content/image/1-s2.0-S0167865525000340-gr5.jpg" width="45%" />
  <img src="https://media.springernature.com/lw1200/springer-static/image/art%3A10.1038%2Fs41598-021-88578-w/MediaObjects/41598_2021_88578_Fig1_HTML.jpg" width="45%" />
</p>

## 📌 Project Overview

**VisionAI: MURA Dataset Classification & Explainable X-Ray Analysis** is a deep learning project designed to automatically classify musculoskeletal X-ray images as **Normal** or **Abnormal** using a transfer-learning approach based on **MobileNetV2**.

In addition to classification, the project includes an **Explainable AI (XAI)** module that generates visual heatmaps highlighting regions that contributed most to the model's prediction, making the results more interpretable for medical analysis and educational purposes.

---

## 📂 Dataset

The project utilizes the **MURA (Musculoskeletal Radiographs) Dataset**, one of the largest publicly available radiographic image datasets released by the Stanford ML Group.

### About MURA

MURA contains musculoskeletal X-ray studies collected from clinical practice and is widely used for research in medical image classification and computer-aided diagnosis.

**Dataset Characteristics**

* **Task:** Binary Classification (Normal vs. Abnormal)
* **Body Parts Covered:**

  * Elbow
  * Finger
  * Forearm
  * Hand
  * Humerus
  * Shoulder
  * Wrist
* **Image Type:** Musculoskeletal Radiographs (X-rays)
* **Labels:** Normal / Abnormal

### Dataset Link

https://www.kaggle.com/datasets/cjinny/mura-v11

---

## 🎯 Objectives

* Detect abnormalities in musculoskeletal X-rays.
* Leverage transfer learning for efficient model training.
* Improve model interpretability using heatmap visualization.
* Demonstrate the application of AI in medical imaging.

---

## 🧠 Model Architecture

The classification model is built using **TensorFlow/Keras** and utilizes:

### MobileNetV2 Transfer Learning

MobileNetV2 was selected because it provides:

* Lightweight architecture
* Fast inference
* Strong feature extraction capability
* Reduced computational requirements

### Architecture Components

* MobileNetV2 Base Model
* Global Average Pooling Layer
* Dense Layers
* Dropout Regularization
* Sigmoid Output Layer for Binary Classification

---

## 🔍 Explainable AI Module (`explainer.py`)

One of the key highlights of this project is the **Explainable AI Dashboard** implemented using Streamlit.

### Features

* Upload an X-ray image.
* Predict whether the image is Normal or Abnormal.
* Generate Grad-CAM style heatmaps.
* Visualize regions influencing model decisions.
* Display confidence scores.
* Interactive web interface.

### How It Works

The `explainer.py` file:

1. Loads the trained MobileNetV2 model.
2. Accepts user-uploaded X-ray images.
3. Preprocesses images to match training dimensions.
4. Generates predictions using the trained model.
5. Computes gradients from the final convolutional layer.
6. Creates a heatmap highlighting important regions.
7. Overlays the heatmap onto the original X-ray.
8. Displays classification results and confidence scores through Streamlit.

### Explainability Benefits

* Improves transparency of AI predictions.
* Helps users understand model focus areas.
* Enhances trust in automated diagnosis systems.
* Demonstrates practical Explainable AI techniques in healthcare.

---

## ✨ Features

* ✅ Binary X-Ray Classification (Normal vs Abnormal)
* ✅ MobileNetV2 Transfer Learning
* ✅ Medical Image Analysis
* ✅ Grad-CAM Inspired Heatmap Visualization
* ✅ Explainable AI Dashboard
* ✅ Streamlit-Based User Interface
* ✅ Confidence Score Display
* ✅ Image Overlay Visualization
* ✅ Interactive X-Ray Upload System

---

## 🛠️ Technologies & Libraries Used

### Deep Learning

* TensorFlow
* Keras
* MobileNetV2

### Data Processing

* NumPy
* Pandas

### Visualization

* Matplotlib

### Computer Vision

* OpenCV (cv2)
* Pillow (PIL)

### Web Application

* Streamlit

### Utilities

* Glob
* OS

---

## 📁 Project Structure

```text
MURA-Dataset-Classification-VisionAI/
│
├── classification.ipynb      # Model training notebook
├── explainer.py              # Streamlit explainability dashboard
├── models/
│   └── xray_mobilenetv2.h5   # Trained model
│
├── README.md
└── requirements.txt
```

## 🛠️ Installation & Requirements

### 1. Clone the Repository

```bash
git clone https://github.com/Shashank14105/MURA-Dataset-Classification-VisionAI.git
cd MURA-Dataset-Classification-VisionAI
```

### 2. Install Dependencies

```bash
pip install numpy pandas matplotlib opencv-python scikit-learn
pip install tensorflow keras
pip install streamlit pillow
```

Alternatively:

```bash
pip install -r requirements.txt
```

---

## 💻 Usage

### 1. Train the Model

To start training the classification model on the MURA dataset:

```bash
python XRayClassification.py
```

or run:

```bash
jupyter notebook classification.ipynb
```

---

### 2. Launch the Explainability Dashboard

```bash
streamlit run explainer.py
```

After launching, open the local Streamlit URL displayed in your terminal.

---

## 📊 Output

The system provides:

* Classification Prediction

  * Normal
  * Abnormal

* Confidence Score

* Heatmap Visualization

* Overlay Analysis View

Example:

```text
Prediction: ABNORMAL (94.32%)

The AI detected potential abnormalities
in the highlighted regions.
```

---

## 🚀 Future Improvements

* Multi-class abnormality detection
* Severity estimation
* Support for additional radiology datasets
* Advanced explainability techniques
* Model deployment on cloud platforms
* Integration with hospital workflows

---

## 📚 Educational Value

This project demonstrates:

* Medical Image Classification
* Transfer Learning
* Computer Vision
* Explainable AI (XAI)
* Streamlit Deployment
* Deep Learning in Healthcare

making it an excellent portfolio project for students and researchers interested in AI for healthcare.

---

## 👨‍💻 Author

**Shashank K**

AI & Machine Learning Enthusiast
VisionAI Project Series

If you found this project useful, consider giving the repository a ⭐.
