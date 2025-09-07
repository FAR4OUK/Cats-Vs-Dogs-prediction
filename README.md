# 🐱🐶 Cat vs Dog Classifier (HOG + SVM)

## 📌 Project Overview
This project builds a **machine learning model** to classify images of cats and dogs.  
Instead of using deep learning, it applies **classical computer vision techniques**:
- **HOG (Histogram of Oriented Gradients)** for feature extraction
- **Support Vector Machine (SVM)** for classification

The goal is to show how traditional ML can still achieve solid results on image recognition tasks.

---

## 📊 Dataset
- Source: [Kaggle Cats vs Dogs dataset](https://www.kaggle.com/c/dogs-vs-cats)
- Training: 2000 images (1000 cats, 1000 dogs)
- Validation: 20% split from training
- Separate test set provided for evaluation

Each image is resized to **64×64** and converted to grayscale before extracting HOG features.

---

## ⚙️ Methodology
1. **Preprocessing**
   - Grayscale conversion
   - Resize to 64×64
   - HOG feature extraction (1764 features per image)

2. **Model Training**
   - Features standardized using `StandardScaler`
   - SVM classifier with RBF kernel
   - Hyperparameters tuned with GridSearchCV

3. **Evaluation**
   - Accuracy, precision, recall, and F1-score
   - Results saved into Excel/CSV for analysis

---

## ✅ Results
- **Validation Accuracy:** ~71%  
- **Test Accuracy:** (varies depending on dataset split)  
- Model predicts and exports results to `test_results.xlsx` / `test_results.csv`
