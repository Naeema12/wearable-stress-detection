#  Wearable Stress Detection Using Physiological Signals

![Python](https://img.shields.io/badge/Python-3.8+-blue)
![Scikit-learn](https://img.shields.io/badge/Scikit--learn-ML-orange)
![Dataset](https://img.shields.io/badge/Dataset-WESAD-green)
![Accuracy](https://img.shields.io/badge/Accuracy-96.5%25-brightgreen)

##  Overview
This project detects stress using physiological signals collected from wearable sensors.
Machine learning models are trained on the **WESAD dataset**, which contains data from
15 subjects wearing chest and wrist devices during baseline, stress, and amusement conditions.

##  Dataset
- **Name:** WESAD (Wearable Stress and Affect Detection)
- **Subjects:** 15 participants
- **Devices:** Chest-worn + wrist-worn sensors
- **Signals:** ECG, EDA, EMG, Temperature, Respiration
- **Source:** [Kaggle](https://www.kaggle.com/datasets/qiriro/wesad-stress-dataset)

##  Methodology
1. **Data Loading** — Load `.pkl` files for each subject
2. **Exploratory Data Analysis** — Visualize sensor signals during stress vs baseline
3. **Feature Extraction** — Sliding window (60s, 50% overlap) → 35 statistical features
4. **Model Training** — Random Forest and SVM classifiers
5. **Evaluation** — Accuracy, F1 Score, Confusion Matrix
6. **Feature Importance** — Identify most predictive sensors

##  Results

| Model | Accuracy | F1 Score |
|-------|----------|----------|
| Random Forest | 100% | 1.000 |
| SVM | 96.5% | 0.947 |

##  Key Finding: Sensor Importance

| Sensor | Importance | Role |
|--------|------------|------|
| EDA | 0.336  | Strongest stress predictor |
| Resp | 0.315  | Breathing pattern changes under stress |
| ECG | 0.173  | Heart rate variability |
| EMG | 0.110 | Muscle activity |
| Temp | 0.065 | Body temperature |

##  Technologies
- Python, NumPy, Pandas, SciPy
- Scikit-learn (Random Forest, SVM)
- Matplotlib, Seaborn

