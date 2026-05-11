# 💼 Salary Prediction Using Machine Learning

A Machine Learning regression project that predicts employee salaries based on years of professional experience using multiple regression algorithms and feature engineering techniques.

This project demonstrates:
- Exploratory Data Analysis (EDA)
- Feature Engineering
- Regression Modeling
- Model Evaluation
- Hyperparameter Tuning

---

# 📌 Problem Statement

Given a single numeric feature:

```python
YearsExperience
```

predict an employee’s annual:

```python
Salary
```

in USD.

---

# 📊 Dataset Information

### Dataset Source
Kaggle — Salary Data Dataset

### Dataset Size
- 30 employee records
- 1 input feature
- 1 target variable

---

# 🧠 Features

| Feature | Type | Description |
|---|---|---|
| YearsExperience | float | Years of professional work experience (1.1 – 10.5) |
| Salary | float | Annual salary in USD ($37k – $122k) |

### Engineered Features
- Experience Squared
- Log Experience
- Experience Bands

The dataset is already clean:
- ✅ No missing values
- ✅ No duplicates

---

# 🛠️ Tech Stack

- Python
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn
- Jupyter Notebook

---

# 📂 Project Structure

```bash
Salary-Prediction/
│
├── 01_eda.ipynb
├── 02_data_cleaning.ipynb
├── 03_model_building.ipynb
├── utils.py
├── requirements.txt
├── README.md
└── data/
    ├── salary.csv
    └── salary_cleaned.csv
```

### Run notebooks in order:
```bash
01_eda.ipynb
→ 02_data_cleaning.ipynb
→ 03_model_building.ipynb
```

---

# ⚙️ Machine Learning Models Used

- Linear Regression
- Ridge Regression
- Lasso Regression
- KNN Regressor
- Decision Tree Regressor
- Random Forest Regressor
- Gradient Boosting Regressor

---

# 📈 Model Performance

| Model | R² | RMSE ($) | MAE ($) | MAPE |
|---|---|---|---|---|
| KNN (K=3) | 0.9441 | 5,344 | 4,665 | 0.058 |
| Ridge | 0.8944 | 7,346 | 6,228 | 0.076 |
| Random Forest | 0.8805 | 7,814 | 6,795 | 0.085 |
| Lasso | 0.8747 | 8,001 | 6,546 | 0.083 |
| Linear Regression | 0.8684 | 8,198 | 6,705 | 0.086 |
| Decision Tree | 0.8188 | 9,619 | 7,430 | 0.085 |
| Gradient Boosting | 0.8130 | 9,774 | 8,215 | 0.100 |
| Ridge (Tuned) | 0.8700 | 8,149 | 6,669 | 0.085 |

---

# 🏆 Best Model

## KNN Regressor (K=3)

### Performance
- R² Score: 0.9441
- RMSE: 5,344
- MAE: 4,665
- MAPE: 0.058

### Best Tuned Model
```python
alpha = 0.001
```

Cross Validation Score:
```python
CV R² = 0.8934
```

---

# 🔍 Key Findings

- YearsExperience and Salary are highly correlated (Pearson r ≈ 0.978).
- Each additional year of experience adds approximately:
  
```python
$9,500/year
```

to salary.

- KNN performed best on the small dataset.
- Ridge Regression provided more stable generalized performance.
- Gradient Boosting underperformed due to the tiny dataset size.
- Feature engineering improved prediction quality significantly.

---

# 📊 Feature Engineering

The project includes:
- Polynomial feature creation
- Log transformations
- Experience band categorization
- One-hot encoding

---

# 🚀 Installation

## Clone Repository

```bash
git clone https://github.com/medisanjay-ai/Salary-Prediction.git
```

## Navigate to Project

```bash
cd Salary-Prediction
```

## Install Dependencies

```bash
pip install -r requirements.txt
```

---

# ▶️ Run The Project

```bash
jupyter notebook
```

Open notebooks in order:
1. `01_eda.ipynb`
2. `02_data_cleaning.ipynb`
3. `03_model_building.ipynb`

---

# 📸 Workflow

1. Data Collection
2. Exploratory Data Analysis
3. Feature Engineering
4. Data Preprocessing
5. Model Training
6. Hyperparameter Tuning
7. Model Evaluation

---

# 📌 Future Improvements

- Deploy using Streamlit
- Add XGBoost & LightGBM
- Build salary prediction web app
- Train on larger datasets

---

# 👨‍💻 Author

## Medi Sanjay

AI/ML Engineer | Data Scientist | Generative AI Enthusiast

📍 Hyderabad, India

---

# ⭐ Acknowledgements

- Scikit-learn
- Kaggle
- Open Source ML Community
