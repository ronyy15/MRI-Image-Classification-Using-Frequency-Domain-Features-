🧠 MRI Image Classification Using Frequency-Domain Features

This project implements a lightweight and efficient machine learning framework for classifying brain MRI images into normal and tumor categories. Instead of relying on computationally heavy deep learning models, this approach leverages frequency-domain features extracted using Fast Fourier Transform (FFT) combined with classical machine learning classifiers for accurate and interpretable diagnosis support.

This work was presented at the 16th IEEE International Conference on Computing, Communication and Networking Technologies (ICCCNT 2025), IIT Indore. 🎓📄

📌 Project Overview

Traditional MRI diagnosis relies on manual inspection by radiologists, which can be time-consuming and subjective.

Our method introduces an FFT-based frequency-domain analysis pipeline that captures hidden periodic textures and structural variations in brain scans.

Extracted statistical features like energy, entropy, mean, standard deviation, and dominant frequencies are used to train models.

The system is lightweight, interpretable, and computationally efficient, making it suitable for real-time clinical applications.

🛠️ Methodology

Preprocessing

Convert images to grayscale

Apply histogram equalization

Resize to uniform resolution

Edge detection (Sobel/Prewitt filters)

Frequency-Domain Transformation

Apply 2D Fast Fourier Transform (FFT)

Extract magnitude spectrum

Feature Extraction

Energy (signal power)

Entropy (frequency randomness)

Mean & Standard deviation

Top 5 dominant frequency coefficients

Classification Models

Hybrid (Random Forest + Gradient Boosting)

Random Forest

Gradient Boosting

XGBoost (best performer)

LightGBM

📊 Results
Classifier	Accuracy	Precision	Recall	F1-Score
Hybrid (RF + GB)	93.08%	93.5%	93.0%	93.2%
XGBoost	94.86%	95%	95%	95%
LightGBM	94.37%	94%	94.1%	94.5%

✅ XGBoost achieved the highest classification accuracy with minimal misclassifications.

📂 Dataset

Source: Kaggle SIAR Brain MRI Dataset

Total Images: 7,000

Normal: 3,800

Tumor: 3,200

Split: 80% training, 20% testing

⚙️ Tech Stack

Language: Python (Jupyter Notebook)

Libraries: NumPy, Pandas, OpenCV, Matplotlib, Scikit-learn, XGBoost, LightGBM
📌 Applications

Early brain tumor detection

Real-time diagnostic support

Lightweight solution for resource-constrained clinical environments

🏆 Conference Recognition

This work was presented at IEEE ICCCNT 2025 🎓
📍 Venue: IIT Indore, Madhya Pradesh, India
📅 Date: July 6th–11th, 2025
Dataset:https://www.kaggle.com/datasets/masoumehsiar/siardataset
