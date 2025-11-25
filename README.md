# Titanic Dataset Cleaning & Exploratory Data Analysis

## Project Overview
This project focuses on **cleaning, analyzing, and visualizing the Titanic dataset** to understand passenger demographics, survival patterns, and relationships between features. The workflow demonstrates **data inspection, preprocessing, univariate/bivariate/multivariate analysis, outlier handling, and target variable exploration**.

---

## Dataset
- **Source:** Kaggle Titanic dataset (`train.csv`)  
- **Rows:** 891  
- **Columns:** 12 (after preprocessing, 11 features + `AgeGroup`)  
- **Key Features:** `PassengerId`, `Survived`, `Pclass`, `Name`, `Sex`, `Age`, `SibSp`, `Parch`, `Ticket`, `Fare`, `Embarked`, `AgeGroup`

---

## Workflow & Detailed Steps

### 1. Data Inspection
- Loaded dataset using **pandas**.
- Checked dataset shape, column types, unique values, and duplicates.
- Identified missing values in `Age`, `Cabin`, and `Embarked`.

### 2. Data Cleaning
- Filled missing `Age` with median.
- Dropped `Cabin` due to excessive missing values.
- Filled missing `Embarked` with mode.
- Confirmed all critical features were complete post-cleaning.

### 3. Univariate Analysis
- Visualized distributions:
  - Age (overall, male, female)
  - Fare
  - Passenger class
  - Gender
  - Embarked points
  - Survival counts
- Detected outliers in `Age` and `Fare` using boxplots (retained due to real variability).

### 4. Bivariate Analysis
- Explored relationships between:
  - Age vs. Sex
  - Fare vs. Pclass
  - Age vs. Survival
  - Embarked vs. Survival

### 5. Multivariate Analysis
- Examined combined effects:
  - Age, Fare, and Pclass on Survival
  - Survival by Embarked and Pclass
  - Interaction of Gender and Class on Survival

### 6. Target Variable Analysis
- Survival distribution (imbalanced: non-survivors > survivors)
- Survival by:
  - Gender
  - Passenger class
  - Embarkation port
  - Age group
- Children and females in first class had the highest survival rates.

### 7. Output
- **Cleaned dataset CSV:** `cleaned_Titanic.csv` (ready for modeling or further analysis)

---

## Skills Demonstrated
- **Data Analysis & Exploration:** pandas, numpy, seaborn, matplotlib  
- **Data Cleaning & Preprocessing:** handling missing values, feature engineering (`AgeGroup`)  
- **Data Visualization:** histograms, boxplots, scatter plots, countplots, catplots  
- **Exploratory Data Analysis (EDA):** univariate, bivariate, multivariate analysis  
- **Outlier Detection & Interpretation:** boxplots, domain reasoning for retention  
- **Target Variable Analysis:** survival patterns by demographics and socio-economic factors  
- **Workflow Management:** end-to-end dataset cleaning and visualization  

---

## Outputs & Insights
- Cleaned dataset free of missing critical values.
- Identified demographic patterns influencing survival:
  - Female passengers survived more than males.
  - First-class passengers had the highest survival rates.
  - Children (0–12) had higher survival probability.
  - Embarkation port influenced survival patterns.
- Visualizations ready for reporting or predictive modeling.
