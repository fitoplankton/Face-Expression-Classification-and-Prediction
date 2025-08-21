# Face-Expression-Classification-and-Prediction

This project is designed for **facial expression classification** from static image files.  
The system extracts features from uploaded face images using **HOG (Histogram of Oriented Gradients)**, **OD-LBP (Orthogonal Difference Local Binary Pattern)**, and applies **PCA (Principal Component Analysis)** for dimensionality reduction.  
Classification is performed with **SVM (Support Vector Machine)**, and the trained model is integrated into a web application where users can upload an image to get the predicted facial expression.

---

## 📌 Key Features
- Feature extraction using:
  - HOG
  - OD-LBP
  - PCA for dimensionality reduction
- Classification using SVM
- Supports multiple expression classes:
  - Neutral  
  - Happiness  
  - Anger  
  - Disgust  
  - Fear  
  - Sadness  
  - Surprise
- Web application (Flask / Streamlit) for **image upload & prediction**
- Models stored in **Pickle (.pkl)** format

---

## 📂 Project Structure
── app.py # Main web application
├── utils.py # Feature extraction (HOG, OD-LBP, PCA, etc.)
├── new_models/ # Saved models (PCA, SVM, etc.)
│ ├── pca_hog_8.pkl
│ ├── svm_model.pkl
│ └── ...
├── static/ # Static files (CSS, images)
├── templates/ # HTML templates (Flask)
├── dataset/ # Facial dataset (if available)
└── README.md # Project documentation

---

## ⚙️ Installation
1. Clone this repo:
   ```bash
   git clone https://github.com/username/facial-expression-recognition.git
   cd facial-expression-recognition

2. Create a virtual environment (optional but recommended):

python -m venv env
source env/bin/activate   # Linux/Mac
env\Scripts\activate      # Windows

3. Install dependencies:

pip install -r requirements.txt

---

## 🚀 Usage

1. Run the application:

python app.py

2. Open your browser at:

http://127.0.0.1:5000

3. Upload a face image file → the system will predict the expression.

---

📊 Model Training

- Models are trained using facial expression datasets with labeled images.
- Features are extracted using HOG / OD-LBP.
- PCA is applied to reduce feature dimensionality for efficiency.
- SVM is used as the main classifier.
- Trained models are saved in .pkl format to be used directly in the application.

---

📝 Notes

- The web application only supports image uploads (not real-time webcam input).
- If you use a new dataset, retrain the model and save the new PCA & SVM models into the new_models/ directory.
- Ensure the number of features during training matches those during prediction (to avoid PCA mismatch errors).
