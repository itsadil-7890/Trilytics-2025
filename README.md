# Farmer Income Prediction using Linear Regression

This project aims to predict the **annual income of farmers** using demographic, socio-economic, and environmental features. The model is built using **Linear Regression**, with appropriate data cleaning, feature engineering, and evaluation steps.

---

## Dataset

- Provided train and test datasets.
- Each record represents information about a farmer and their environment.
- The target variable is **Income** (transformed using log for modeling).

---

## Key Steps & Highlights

### 1. Exploratory Data Analysis (EDA)
- Checked distribution of target variable (`Income`)
- Identified **positive skew** and applied **log transformation**
- Analyzed categorical variables like `SEX`, `REGION`, `MARITAL_STATUS`
- Visualized outliers and distributions

### 2. Data Preprocessing
- **Separated min/max range columns** (e.g., `"20 / 40"` → two separate numeric columns)
- **Encoded categorical variables** (e.g., `SEX`, `REGION`, etc.)
- **Dropped less useful or problematic categorical columns** with `object` dtype

### 3. Feature Scaling
- Identified numerical columns with more than 2 unique values
- Applied **StandardScaler** to normalize continuous features
- Retained one-hot encoded or binary features without scaling

### 4. Model Building
- Used **Linear Regression** from `sklearn`
- Trained model on log-transformed income (`Income_Log`)
- Ensured **consistent column order and structure** in test set

### 5. Model Evaluation
- Calculated **MAPE (Mean Absolute Percentage Error)** on training data
- Achieved a MAPE of **~30.47%** (~69.5% average prediction accuracy)

### 6. Final Prediction
- Reversed the log transformation (`np.expm1`) to get predicted income
- Generated final CSV/Excel file with `Farmer_ID` and predicted income

---

##  Technologies Used

- Python (Pandas, NumPy, Scikit-learn)
- Matplotlib / Seaborn 
- Git & GitHub for version control

---
##  Suggestions & Feedback

Have ideas to improve this project? 

Suggestions are welcome on:
- Model improvement or feature engineering
- Handling missing values or outliers
- Code optimization or visualizations





