# 🚀 Alpha-SME: The Ultimate MLP Quant
> **Strategic Financial Risk Analysis & Bankruptcy Prediction for SMEs**

[![Python](https://img.shields.io/badge/Python-3.8%2B-blue.svg)](https://www.python.org/)
[![Framework](https://img.shields.io/badge/Scikit--Learn-F16061?style=flat&logo=scikit-learn&logoColor=white)](https://scikit-learn.org/)
[![Domain](https://img.shields.io/badge/Domain-Quantitative%20Finance-green.svg)]()

## 📌 Project Overview
**Alpha-SME** is a high-performance financial intelligence system designed to predict corporate bankruptcy among Small and Medium Enterprises (SMEs). Built on "First Principles," the project transforms raw, high-dimensional financial ratios into actionable risk scores using a custom-built Multi-Layer Perceptron (MLP) architecture.

The pipeline addresses critical financial modeling challenges such as missing data, extreme class imbalance, and the necessity for calibrated probability outputs in credit risk assessment.

## 🛠 Key Technical Features
- **Temporal Data Engineering:** Implements strict "Time-Walk" splitting to prevent data leakage and simulate real-world forecasting.
- **Robust Imputation:** Utilizes **KNN Imputer** to intelligently handle missing financial indicators based on similar corporate profiles.
- **Advanced Class Handling:** Custom logic to manage highly imbalanced datasets (Bankruptcy rate ~4.8%).
- **Calibrated AI (XAI):** Features **Platt Scaling** for probability calibration and feature importance analysis to explain "why" a company is flagged as high-risk.

## 📊 The Pipeline (Phase-by-Phase)

### Phase 0: Data Ingestion & Sanitization
- Processing of 64 financial ratios (Attributes) for over 43,000 corporate records.
- Initial cleaning and removal of non-contributory identifiers.

### Phase 1: Quantitative Pre-processing
- **Feature Scaling:** Leveraging `StandardScaler` to normalize diverse financial metrics (e.g., Profitability vs. Total Assets).
- **Leakage Prevention:** Segregating data into Training, Validation (for calibration), and Test sets based on fiscal years.

### Phase 2: MLP Architecting & Training
- Development of a deep neural network (MLP) optimized for binary classification.
- Hyperparameter tuning to maximize **Recall**, ensuring no potential bankruptcy goes undetected.

### Phase 3: Post-Processing & Calibration
- Implementation of **Platt Scaling** on the validation set to ensure the output scores represent real-world probabilities.
- Feature importance extraction to identify the top 5 bankruptcy drivers (e.g., `Attr55`).

## 📈 Performance Metrics
The model achieves industry-leading sensitivity:
- **Test Recall:** `~99%` (Critical for catching defaults)
- **Brier Score:** `~0.10` (Reflecting high calibration quality)
- **XAI:** Clear transparency on the impact of specific financial ratios.

## 🧰 Tech Stack
- **Core:** Python
- **Data:** Pandas, NumPy
- **ML/DL:** Scikit-Learn (MLPRegressor/Classifier, CalibrationPipe)
- **Visualization:** Matplotlib, Seaborn

## 🚀 How to Use
1. Clone the repository.
2. Open `Quantative_Risk_Analysis(2).ipynb` in Jupyter Notebook or Google Colab.
3. Run all cells to reproduce the preprocessing, training, and evaluation results.

---
*Developed with a focus on Financial AI Deployment Architecture.*
