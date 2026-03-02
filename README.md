
# 🚗 Smart License Plate Recognition System (YOLOv5 & Random Forest)

This project is a web-based application that performs automatic license plate detection and Optical Character Recognition (OCR) using a hybrid approach of Deep Learning and Machine Learning.

## 🚀 Live Demo

You can try the application live on Hugging Face Spaces:
**[👉 Click Here for Live Demo](https://huggingface.co/spaces/erdemyavuz/plate-recognition-tr)**

## 🌟 Key Features

* **Hybrid Architecture:** Combines **YOLOv5** for high-accuracy object detection with **Random Forest** for robust character classification.
* **Advanced Image Processing:** Utilizes OpenCV contour analysis and adaptive thresholding for precise character segmentation.
* **HOG Feature Extraction:** Characters are vectorized using **Histogram of Oriented Gradients (HOG)** to capture essential shape and structural information.
* **Modern Web Interface:** A responsive, dark-themed UI built with Flask for a seamless user experience.

## 🛠️ Tech Stack

* **Backend:** Python, Flask
* **Computer Vision:** OpenCV, Scikit-Image
* **Deep Learning:** PyTorch, YOLOv5
* **Machine Learning:** Scikit-Learn (Random Forest)
* **Deployment:** Docker, Hugging Face Spaces

## 📐 How It Works

1. **Plate Detection:** The YOLOv5 model identifies and crops the license plate region from the input image.
2. **Segmentation:** The cropped plate undergoes adaptive thresholding and contour analysis to isolate individual characters (letters and numbers).
3. **Feature Extraction:** Each isolated character is resized to 32x32 pixels, and its HOG feature vector is calculated.
4. **Classification:** The pre-trained Random Forest model analyzes these vectors to predict the corresponding character.

## 🚀 Installation & Local Setup

### 1. Clone the Repository

```bash
git clone https://github.com/ErdemYavuz55/plate-recognition-tr.git
cd plate-recognition-tr

```

### 2. Install Dependencies

```bash
pip install -r requirements.txt

```

### 3. Run the Application

```bash
python app.py

```

Then, navigate to `http://localhost:7860` in your web browser.

## 🐳 Running with Docker

```bash
docker build -t plate-recognition .
docker run -p 7860:7860 plate-recognition

```

## 📊 Model Performance

The OCR component utilizes a Random Forest classifier trained on a labeled dataset of character HOG features. This approach ensures high reliability across various lighting conditions and camera angles.

---
