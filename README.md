# Heart Disease Prediction Models

This project explores how machine learning can be used to **predict the likelihood of heart disease** using demographic and clinical data. I built, tested, and compared multiple models on a cleaned dataset compiled from five well-known heart disease datasets.  

---

## 📌 Project Overview
- **Goal**: Classify whether a patient has heart disease (1) or not (0).  
- **Why it matters**: Heart disease is the leading cause of death worldwide, responsible for ~18M deaths annually (WHO, 2024). Accurate early prediction can empower preventive healthcare, reduce hospitalizations, and lower costs 
- **Approach**: Clean and merge datasets, engineer meaningful clinical features, build machine learning models, and evaluate them using accuracy, precision, recall, and AUC.  

---

## 🗂 Dataset
- **Source**: Integrated from 5 major datasets (Cleveland, Hungarian, Switzerland, Long Beach VA, Statlog).  
- **Size**: 918 unique patient records after cleaning.  
- **Variables**:
  - Demographics: Age, Sex  
  - Clinical: ChestPainType, RestingBP, Cholesterol, FastingBS, RestingECG, MaxHR, ExerciseAngina, Oldpeak, ST_Slope  
  - **Target**: `HeartDisease` (1 = disease present, 0 = normal) 

The dataset was **pre-cleaned** (duplicates removed, no missing values) and additional **feature engineering** was applied (e.g., converting cholesterol and age into clinical flags).  

---

## ⚙️ Methods

### Preprocessing
- Encoded categorical variables using scikit-learn pipelines.  
- Created engineered features to capture clinical cutoffs and patterns.  

### Models Built
1. **Logistic Regression** ✅ (best performing)  
2. Random Forest  
3. Gradient Boosting  
4. Ensemble (Voting)  

### Evaluation Metrics
- Accuracy  
- Precision  
- Recall (True Positive Rate)  
- ROC AUC  

---

## 📊 Results

| Model                | Accuracy | Precision | Recall | AUC  |
|-----------------------|----------|-----------|--------|------|
| Logistic Regression   | **92.9%** | 93.7%     | **94.5%** | **0.95** |
| Random Forest         | 91.3%    | 92.7%     | 92.7%  | 0.95 |
| Gradient Boosting     | 87%      | 88.0%     | 88.0%  | 0.92 |
| Ensemble (Voting)     | 90.2%    | 90.0%     | 90.0%  | 0.935 |

➡️ **Logistic Regression outperformed the others**, achieving nearly **93% accuracy** with high recall, which is crucial for identifying patients at risk.

---

## 🚀 Impact
- Helps detect heart disease early with high accuracy.  
- Promotes **health equity** by enabling preventive screening.  
- Reduces hospitalization rates and overall healthcare costs.  

---

## 🔮 Future Work
- Cost-sensitive learning to address false negatives.  
- Hyperparameter tuning for stronger model optimization.  
- External validation with new datasets.  
- Deployment as a **real-time continuous learning pipeline**.

---

## 🛠️ Tech Stack
- **Languages**: Python  
- **Libraries**: pandas, scikit-learn, matplotlib, seaborn  
- **Tools**: Jupyter Notebook  

---
