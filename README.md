# Lung Cancer Survival Prediction

## 📖 Problem Statement
The goal of this project is to **predict the survival of a lung cancer patient** given their demographic, medical, and treatment details.

This involves:
- Exploring the dataset to understand patient features.
- Preprocessing and cleaning the data.
- Handling class imbalance.
- Training machine learning models to predict survival.
- Evaluating and comparing model performance.

---

## 📂 Dataset
The dataset used (`dataset_med.csv`) contains **80,733 patient records** with 17 columns:

- **Demographics:** age, gender, country
- **Medical history:** family_history, smoking_status, bmi, cholesterol_level, hypertension, asthma, cirrhosis, other_cancer
- **Diagnosis & treatment:** cancer_stage, diagnosis_date, treatment_type, end_treatment_date
- **Target:** survived (1 = survived, 0 = did not survive)

---

## ⚙️ Approach
1. **Data Preprocessing**
   - Handled missing values (mean imputation for numerical, placeholders for categorical).
   - Encoded categorical variables (`LabelEncoder`, one-hot encoding).
   - Engineered feature: `treatment_time` (days between diagnosis and treatment end).
   - Normalized numeric features with `StandardScaler`.

2. **Exploratory Data Analysis (EDA)**
   - Histograms, countplots for distribution analysis.
   - Correlation heatmaps.
   - Insights into cancer stages, smoking habits, and survival outcomes.

3. **Class Imbalance Handling**
   - Applied **SMOTE** to oversample minority survival cases.

4. **Modeling**
   - Logistic Regression
   - Random Forest
   - XGBoost

5. **Evaluation**
   - Metrics: Accuracy, Precision, Recall, F1-score.
   - Compared performance across models.

---

## 📊 Results
| Model                | Accuracy | Recall (Survived) | F1 (Survived) |
|----------------------|----------|-------------------|---------------|
| Logistic Regression  | 0.43     | 0.60              | 0.32          |
| Random Forest        | 0.70     | 0.16              | 0.19          |
| XGBoost              | 0.75     | 0.06              | 0.09          |

- Logistic Regression captured survival cases better (higher recall).
- Random Forest and XGBoost had higher accuracy but poor recall for survival class.
- Class imbalance remains a major challenge.

---

## 📌 Limitations
- Models struggle to predict the **positive class (survived)** effectively.
- Features may not fully capture medical complexity.
- Potential data quality issues (imbalanced and noisy dataset).

---

## 🚀 Future Work
- Try **ensemble methods** (stacking, boosting).
- Use **feature selection/importance analysis**.
- Explore **deep learning models**.
- Collect more balanced survival data.

---

## 📦 Installation & Usage

### 1. Clone Repo
```bash
git clone https://github.com/your-username/Lung-Cancer-Detection.git
cd Lung-Cancer-Detection
