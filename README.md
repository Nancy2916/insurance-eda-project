# insurance-eda-project
Exploratory Data Analysis on Insurance Dataset

# Insurance Cost Analysis (EDA & Feature Engineering)

## Project Overview

This project performs **Exploratory Data Analysis (EDA)** and **feature engineering** on a medical insurance dataset.
The goal is to understand the relationship between different features (such as age, BMI, smoking habits, and region) and **insurance charges**.

The analysis helps identify the most important factors affecting insurance costs and prepares the dataset for machine learning models.

---

## Dataset Information

The dataset contains **1338 records and 7 features**.

Features in the dataset:

* **age** – Age of the policyholder
* **sex** – Gender of the person (male/female)
* **bmi** – Body Mass Index
* **children** – Number of dependents covered by insurance
* **smoker** – Whether the person smokes (yes/no)
* **region** – Residential region (northeast, northwest, southeast, southwest)
* **charges** – Medical insurance cost (target variable)

---

## Exploratory Data Analysis (EDA)

Several analyses were performed:

### 1. Data Inspection

* Checked dataset shape
* Viewed sample records
* Verified data types
* Checked missing values

### 2. Statistical Summary

Used descriptive statistics to understand:

* mean
* standard deviation
* min and max values
* distribution of numerical variables

### 3. Data Visualization

Different plots were used to understand data distribution:

* **Histograms with KDE** to observe numerical distributions
* **Count plots** for categorical variables
* **Boxplots** to detect outliers
* **Correlation heatmap** to understand relationships between variables

---

## Data Cleaning

The dataset was cleaned before further analysis:

* Duplicate records were removed
* Checked for missing values
* Converted categorical features to numerical format

---

## Feature Engineering

Several transformations were applied:

### Encoding

Categorical variables were converted into numeric values:

* `sex` → binary encoding
* `smoker` → binary encoding
* `region` → one-hot encoding

### BMI Category Creation

BMI values were grouped into categories:

* Underweight
* Normal
* Overweight
* Obese

Then these categories were converted into dummy variables.

---

## Feature Scaling

Important numerical features were scaled using **StandardScaler**:

* age
* bmi
* children

This helps improve performance for machine learning algorithms.

---

## Feature Selection

Two statistical methods were used to identify important features.

### Pearson Correlation

Used to measure correlation between each feature and **insurance charges**.

The strongest relationship was observed with:

* **smoking status**
* **age**
* **BMI**

### Chi-Square Test

Used for categorical feature importance testing.

Features with significant p-values were kept for modeling.

---

## Key Insights

Important findings from the analysis:

* **Smoking has the strongest impact on insurance charges**
* **Older individuals tend to have higher insurance costs**
* **Higher BMI is associated with increased medical charges**
* Region has relatively weaker influence compared to smoking and age

---

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* Scikit-learn
* SciPy

---

## Project Structure

```
insurance-eda-project
│
├── project1.ipynb        # Main analysis notebook
├── insurance.csv         # Dataset
└── README.md             # Project documentation
```

---

## Future Work

Possible extensions of this project:

* Build a **machine learning model to predict insurance charges**
* Compare different regression algorithms
* Perform hyperparameter tuning
* Deploy the model as a web application
