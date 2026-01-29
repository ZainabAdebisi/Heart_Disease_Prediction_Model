# Heart Disease Prediction Project 🫀

## 📌 Overview
Cardiovascular diseases are the leading cause of death globally. This project utilizes Machine Learning to predict the presence of heart disease in patients based on their medical history and biological markers (such as cholesterol, blood pressure, and chest pain type).

**Objective:** To develop a diagnostic tool that assists healthcare professionals in identifying high-risk patients, with a focus on interpreting the physiological "silent" warning signs.

## ⚙️ Key Features
- **Exploratory Data Analysis (EDA):** Uncovered a critical medical insight regarding **"Silent Ischemia"**—patients reporting *Asymptomatic* chest pain were paradoxically at the highest risk.
- **Data Preprocessing:**
  - **One-Hot Encoding** for categorical variables (Chest Pain, Thalassemia).
  - **Standard Scaling** applied to numerical features (Cholesterol, Age, BP) to prevent model bias.
- **Feature Importance:** Extracted model coefficients to identify the strongest predictors of disease.

## 🔬 Model Performance
I implemented a **Logistic Regression** model, chosen for its interpretability in a clinical setting (providing probability scores rather than just binary outputs).

### Results:
- **Accuracy:** ~85%
- **Recall (Sensitivity):** **87.5%**
  - *Why this matters:* In medicine, Recall is king. The model successfully caught 87.5% of the actual heart disease cases, minimizing dangerous "False Negatives."
- **Precision:** 84%

### 🩺 Clinical Insights (Feature Importance)
The model identified these top risk factors:
1.  **Coronary Vessels (`ca`):** The number of colored vessels seen on fluoroscopy was the strongest predictor of disease.
2.  **Asymptomatic Chest Pain (`cp_3`):** Confirmed that lack of typical pain does not equal lack of risk.
3.  **Maximum Heart Rate (`thalach`):** Lower capacity to achieve high heart rates under stress correlated with disease presence.

## 🛠 Tech Stack
- **Language:** Python 🐍
- **Libraries:**
  - `Pandas` & `NumPy` (Data Manipulation)
  - `Matplotlib` & `Seaborn` (Visualization)
  - `Scikit-learn` (Machine Learning)
