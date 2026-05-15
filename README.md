# CodeAlpha_DiseasePrediction_ML
A disease prediction system using ensemble methods (Random Forest, XGBoost) and SVM to classify heart disease risk from patient medical data including age, blood pressure, cholesterol levels, and symptoms, optimizing model evaluation through F1-score, confusion matrices, XGBoost, and cross-validation techniques.

 Heart Disease Prediction Model

Predicting heart disease using Machine Learning algorithms as part of CodeAlpha Machine Learning Internship.

Project Overview

This project develops a machine learning model to predict the presence of heart disease in patients using the UCI Heart Disease dataset. The model analyzes 13 clinical features to provide binary classification (Disease Present/Absent) with 86.67% accuracy.

Objective

Build a reliable classification model that can assist in preliminary heart disease screening by analyzing patient medical data including age, blood pressure, cholesterol levels, and diagnostic test results.

Dataset

- **Source:** UCI Machine Learning Repository - Cleveland Heart Disease Database
- **Size:** 303 patients (297 after cleaning)
- **Features:** 13 clinical parameters
- **Target:** Binary classification (0 = Healthy, 1 = Disease Present)

### Key Features:
- `age`: Age in years
- `sex`: Gender (1 = male, 0 = female)
- `cp`: Chest pain type (4 values)
- `trestbps`: Resting blood pressure
- `chol`: Serum cholesterol in mg/dl
- `fbs`: Fasting blood sugar > 120 mg/dl
- `restecg`: Resting electrocardiographic results
- `thalach`: Maximum heart rate achieved
- `exang`: Exercise induced angina
- `oldpeak`: ST depression induced by exercise
- `slope`: Slope of peak exercise ST segment
- `ca`: Number of major vessels colored by fluoroscopy
- `thal`: Thalassemia (blood disorder)

Technologies Used

- **Python 3.x**
- **Libraries:**
  - pandas, numpy - Data manipulation
  - scikit-learn - Machine Learning algorithms
  - XGBoost - Gradient boosting
  - matplotlib, seaborn - Data visualization

Models Implemented

| Model | Accuracy | ROC-AUC | False Negatives |
|-------|----------|---------|-----------------|
| Logistic Regression | 83.33% | - | 6 |
| Random Forest | 85.00% | - | 6 |
| **XGBoost (Final)** | **86.67%** | **0.892** | **5** |

Key Results

- **Best Model:** XGBoost Classifier
- **Accuracy:** 86.67%
- **ROC-AUC Score:** 0.892 (Excellent)
- **Recall (Disease Detection):** 82.1%
- **Precision:** 88.5%

### Top Predictive Features:
1. **thal** (Thalassemia) - 24.93% importance
2. **cp** (Chest Pain Type) - 18.02% importance
3. **ca** (Number of Major Vessels) - 12.17% importance

Methodology

1. **Data Loading & Exploration**
   - Loaded UCI Heart Disease dataset
   - Handled missing values (6 rows with '?')
   - Converted multi-class target to binary

2. Data Preprocessing
   - Removed missing values
   - Split features (X) and target (y)
   - Train-test split (80-20)

3. Model Training
   - Trained 3 models: Logistic Regression, Random Forest, XGBoost
   - Compared performance metrics
   - Selected XGBoost as final model

4. Model Evaluation
   - Confusion matrix analysis
   - ROC curve and AUC score
   - Feature importance analysis
   - Classification report (precision, recall, F1-score)

Visualizations

- Confusion Matrix
- ROC Curve
- Feature Importance Chart
- Correlation Heatmap
- Feature Distribution Plots

Key Insights

- Thalassemia (blood disorder) is the strongest predictor of heart disease
- Chest pain type and number of major vessels are critical indicators
- Model shows excellent discrimination ability (AUC = 0.892)
- Only 5 false negatives out of 28 disease cases (82% catch rate)

How to Run

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/CodeAlpha_HeartDiseaseDetection.git

# Install dependencies
pip install pandas numpy scikit-learn xgboost matplotlib seaborn

# Run the Jupyter notebook
jupyter notebook heart_disease_prediction.ipynb
```

Project Structure
CodeAlpha_HeartDiseaseDetection/
│
├── heart_disease_prediction.ipynb    # Main notebook with complete code
├── README.md                          # Project documentation
├── requirements.txt                   # Python dependencies
└── results/                           # Visualizations and outputs
├── confusion_matrix.png
├── roc_curve.png
├── feature_importance.png
└── model_comparison.png

Learning Outcomes

- Data preprocessing and handling missing values
- Binary classification with multiple algorithms
- Model evaluation using various metrics
- Feature engineering and importance analysis
- Understanding healthcare ML considerations (recall vs precision)

Future Improvements

- Hyperparameter tuning using GridSearchCV
- Feature engineering (polynomial features, interactions)
- Ensemble methods (stacking multiple models)
- Cross-validation for more robust evaluation
- Deployment as web application using Flask/Streamlit

Author:

Ambreen Zafar
- LinkedIn: https://www.linkedin.com/in/ambreen-zafar-71101b51? 
- GitHub: https://github.com/Ambii
- Email: venatrixaihorror@gmail.com

License

This project was completed as part of the **CodeAlpha Machine Learning Internship Program**.

 🙏 Acknowledgments

- Dataset: UCI Machine Learning Repository
- Internship: CodeAlpha
- Guidance: CodeAlpha Mentorship Team

---

⭐ If you found this project helpful, please give it a star!
