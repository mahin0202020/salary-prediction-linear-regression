 
# 💰 Salary Prediction using Linear Regression

This project implements a **Multiple Linear Regression** model to predict employee salaries based on various factors such as years of experience, age, education level, and job title. The project includes extensive Exploratory Data Analysis (EDA), data preprocessing, outlier detection, and model evaluation.

## 📌 Project Overview
The goal of this project is to build a predictive model that can estimate the salary of an employee. This is a classic regression problem solved using the **Ordinary Least Squares (OLS)** method via Scikit-Learn.

**Key Features:**
* Handling missing values (Imputation).
* Categorical data encoding (One-Hot Encoding).
* **Outlier Detection:** Using Boxplots and IQR (Interquartile Range) method.
* **Model Evaluation:** Residual Analysis and performance metrics ($R^2$, RMSE).

## 📂 Dataset
The dataset contains the following features:
* **Age:** Age of the employee.
* **Gender:** Male/Female.
* **Education Level:** Bachelor's, Master's, PhD, etc.
* **Job Title:** Designation of the employee.
* **Years of Experience:** Total work experience in years.
* **Salary:** (Target Variable) Annual salary.

## 🛠 Technologies Used
* **Python** (Programming Language)
* **Pandas & NumPy** (Data Manipulation)
* **Matplotlib & Seaborn** (Data Visualization & Outlier Detection)
* **Scikit-Learn** (Machine Learning Model & Metrics)

## 📊 Workflow

### 1. Data Preprocessing
* **Missing Values:** Filled categorical nulls with `Mode` and numerical nulls with `Mean`.
* **Encoding:** Applied `pd.get_dummies` with `drop_first=True` to convert categorical variables into numerical format and avoid the dummy variable trap.

### 2. Exploratory Data Analysis (EDA)
* Analyzed the relationship between *Years of Experience* and *Salary* using Scatter Plots.
* **Outlier Detection:** Used **Boxplots** to visualize outliers in Salary and Experience columns. Implemented the **IQR method** to identify specific outlier data points affecting the model.

### 3. Model Training
* Split the dataset into Training (80%) and Testing (20%) sets.
* Trained a **Multiple Linear Regression** model using Scikit-Learn.

### 4. Model Evaluation
The model performance was evaluated using the following metrics:
* **MAE (Mean Absolute Error)**
* **MSE (Mean Squared Error)**
* **RMSE (Root Mean Squared Error)**
* **R² Score (Accuracy)**

**Residual Analysis:**
A residual plot was generated to check for homoscedasticity. The plot showed that while the model predicts well for lower and mid-range salaries, there are deviations (outliers) in the higher salary range.

## 📈 Visualizations
The notebook contains:
1.  **Scatter Plot:** Experience vs. Salary.
2.  **Actual vs. Predicted Plot:** To visualize model performance.
3.  **Residual Plot:** To detect prediction errors.
4.  **Boxplots:** For outlier detection in numerical columns.

## 🚀 How to Run
1.  Clone the repository:
    ```bash
    git clone [https://github.com/your-username/salary-prediction-linear-regression.git](https://github.com/your-username/salary-prediction-linear-regression.git)
    ```
2.  Install dependencies:
    ```bash
    pip install pandas numpy matplotlib seaborn scikit-learn
    ```
3.  Run the notebook or python script.

## 🔮 Future Improvements
* Removing the detected outliers to improve the $R^2$ score.
* Applying Log Transformation on the 'Salary' column to handle heteroscedasticity.
* Trying other algorithms like Random Forest or Decision Trees for better accuracy.

---
**Author:** Sheikh Mohammad Abdullah
