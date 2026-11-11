# Breast Cancer Histopathology Image Classification using Random Forest

## 📌 Project Overview

This project implements a **Random Forest Classifier** to classify breast cancer histopathology image patches into two categories:

- **Class 0:** Non-Cancerous
- **Class 1:** Cancerous

The project uses Histogram of Oriented Gradients (HOG) for feature extraction and Scikit-learn for machine learning model development and evaluation.

## 🎯 Objectives

- Classify histopathology image patches using Random Forest.
- Extract image features using HOG.
- Experiment with different hyperparameter configurations.
- Evaluate model performance using standard classification metrics.
- Apply patient-wise data splitting to reduce data leakage.

## 📂 Dataset

**Dataset:** Breast Histopathology Images (IDC Dataset)

**Source:** [Kaggle – Breast Histopathology Images](https://www.kaggle.com/datasets/paultimothymooney/breast-histopathology-images)

- Image type: RGB histopathology patches
- Original image size: 50 × 50 pixels
- Classes: Cancerous and Non-Cancerous

### Dataset Distribution

| Dataset | Total Images | Per Class |
|---|---:|---:|
| Training | 4,000 | 2,000 |
| Validation | 2,000 | 1,000 |
| Testing | 2,000 | 1,000 |

Patient-wise splitting was performed to help prevent patient-level data leakage.

## ⚙️ Technologies Used

- Python
- NumPy
- Pandas
- OpenCV
- Scikit-image
- Matplotlib
- Seaborn
- Scikit-learn
- Joblib
- Jupyter Notebook

## 🔬 Methodology

1. Dataset loading and image path collection.
2. Patient-wise training, validation, and testing split.
3. Balanced dataset creation.
4. Image resizing to 64 × 64.
5. Grayscale conversion.
6. HOG feature extraction.
7. Random Forest model training.
8. Hyperparameter experimentation.
9. Model selection using validation F1-score.
10. Final testing and performance evaluation.

## 🧠 HOG Feature Extraction

The following parameters were used:

| Parameter | Value |
|---|---|
| Image Size | 64 × 64 |
| Orientations | 9 |
| Pixels per Cell | 8 × 8 |
| Cells per Block | 2 × 2 |
| Total Features | 1,764 |

## 🌳 Random Forest Configuration

Different combinations of tree counts and maximum depths were evaluated.

**Best validation configuration:**

| Hyperparameter | Value |
|---|---:|
| n_estimators | 200 |
| max_depth | 5 |
| min_samples_split | 10 |
| min_samples_leaf | 5 |
| random_state | 42 |

### Validation Results

| Metric | Score |
|---|---:|
| Accuracy | 64.35% |
| F1-Score | 68.13% |

## 📊 Final Test Performance

The final model was evaluated using the following metrics.

| Metric | Test Score |
|---|---|
| Accuracy | Update from notebook |
| Precision | Update from notebook |
| Recall | Update from notebook |
| F1-Score | Update from notebook |
| ROC-AUC | Update from notebook |

## 📈 Visualizations

The project generates:

- Random Forest Hyperparameter Comparison
- Confusion Matrix
- ROC Curve
- Feature Importance
- Final Performance Metrics

## 📁 Repository Structure

```text
breast-cancer-histopathology-random-forest/
│
├── Breast_Cancer_Random_Forest.ipynb
├── best_random_forest_model.pkl
├── Random_Forest_Comparison.csv
├── Random_Forest_Final_Results.csv
├── Random_Forest_Hyperparameter_Comparison.png
├── Random_Forest_Confusion_Matrix.png
├── Random_Forest_ROC_Curve.png
├── Random_Forest_Feature_Importance.png
├── Random_Forest_Final_Performance.png
├── requirements.txt
└── README.md
```

## 🚀 Installation

Clone the repository:

```bash
git clone https://github.com/https://github.com/UTKRISHT-ICS52/breast-cancer-histopathology-random-forest.git
```

Install dependencies:

```bash
pip install numpy pandas matplotlib seaborn opencv-python scikit-image scikit-learn joblib jupyter
```

Launch Jupyter Notebook:

```bash
jupyter notebook
```

## 🔮 Future Scope

- Compare Random Forest with KNN and Decision Tree.
- Explore advanced feature extraction methods.
- Implement CNN-based classification.
- Investigate feature selection and ensemble optimization.
- Explore explainable AI techniques.

## ⚠️ Disclaimer

This project is developed for educational and research purposes only. It is not a clinically validated diagnostic system and must not be used for medical decision-making.

## 👨‍💻 Author

**Utkrisht Patel**

Researcher | Machine Learning | AI | Research & Development
---

⭐ If you find this project useful, consider giving the repository a star!
