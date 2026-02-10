# Landmark Detection using Deep Learning

This project implements a landmark classification system using **Transfer Learning** with **VGG19**.  
Given an image, the model predicts the landmark category it belongs to.

The code is designed for small-scale experiments and learning purposes, with a clean training and evaluation loop.

---

## 📌 Features

- Uses **VGG19 (ImageNet weights)** as backbone
- Custom classification head with dropout
- Batch-based training loop
- Automatic image path resolution from image ID
- Simple evaluation with correct vs incorrect predictions
- Visual sanity check for random samples

---

## 🧠 Tech Stack

- Python
- TensorFlow / Keras
- OpenCV
- NumPy & Pandas
- Scikit-learn
- Matplotlib

---

## 📂 Project Structure
.
├── LandmarkDetection.py
├── train.csv
├── images/
│ └── a/b/c/imageid.jpg
├── Model/
├── README.md
└── .gitignore

**Image folder format**
image_id = abc123xyz
path = images/a/b/c/abc123xyz.jpg


---

## 📊 Dataset Format

`train.csv` must contain:

| Column Name  | Description |
|-------------|-------------|
| id          | Image ID    |
| landmark_id | Class label |

Example:
```csv
id,landmark_id
0001abcd,12
0002efgh,45

🚀 How to Run
1️⃣ Install dependencies
pip install tensorflow opencv-python numpy pandas scikit-learn matplotlib pillow

2️⃣ Prepare dataset

Place images inside images/ using nested folders

Add train.csv in the root directory

3️⃣ Run training
python LandmarkDetection.py


The trained model will be saved in the Model/ directory.
