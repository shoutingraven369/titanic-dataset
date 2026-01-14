# Titanic Dataset Analysis

A data science project for exploring and analyzing the famous Titanic passenger dataset. This repository contains data preprocessing, feature engineering, and exploratory data analysis notebooks.

## Table of Contents

- [Overview](#overview)
- [Dataset Description](#dataset-description)
- [Project Structure](#project-structure)
- [Features](#features)
- [Requirements](#requirements)
- [Getting Started](#getting-started)
- [Notebooks](#notebooks)
- [Data Preprocessing](#data-preprocessing)
- [License](#license)

## Overview

This project provides a comprehensive analysis of the Titanic dataset, which contains information about passengers aboard the RMS Titanic. The analysis includes data cleaning, handling missing values, feature encoding, and visualization to understand factors that influenced passenger survival.

## Dataset Description

The original Titanic dataset (`Titanic-Dataset.csv`) contains 891 passenger records with the following features:

| Column | Description |
|--------|-------------|
| PassengerId | Unique identifier for each passenger |
| Survived | Survival indicator (0 = No, 1 = Yes) |
| Pclass | Passenger class (1 = First, 2 = Second, 3 = Third) |
| Name | Passenger name |
| Sex | Gender (male/female) |
| Age | Age in years |
| SibSp | Number of siblings/spouses aboard |
| Parch | Number of parents/children aboard |
| Ticket | Ticket number |
| Fare | Passenger fare |
| Cabin | Cabin number |
| Embarked | Port of embarkation (C = Cherbourg, Q = Queenstown, S = Southampton) |

## Project Structure

```
titanic-dataset-main/
|-- Titanic-Dataset.csv       # Original Titanic dataset (891 records)
|-- titanic-updated.csv       # Preprocessed dataset with encoded features (719 records)
|-- elevate_lab_t1.ipynb      # Data preprocessing and feature encoding notebook
|-- elevate_lab_t2.ipynb      # Exploratory data analysis and visualization notebook
|-- README.md                 # Project documentation
```

## Features

- **Data Cleaning**: Handling missing values in Age, Cabin, and Embarked columns
- **Feature Encoding**: One-hot encoding for categorical variables (Sex, Embarked)
- **Imputation**: Using SimpleImputer from scikit-learn for missing value imputation
- **Visualization**: Statistical analysis and data visualization using matplotlib and seaborn
- **Summary Statistics**: Descriptive statistics for understanding data distribution

## Requirements

The project requires the following Python libraries:

- pandas
- matplotlib
- seaborn
- scikit-learn
- category_encoders

### Installation

```bash
pip install pandas matplotlib seaborn scikit-learn category_encoders
```

## Getting Started

1. Clone the repository:
   ```bash
   git clone https://github.com/yourusername/titanic-dataset.git
   cd titanic-dataset
   ```

2. Install the required dependencies:
   ```bash
   pip install -r requirements.txt
   ```

3. Open the Jupyter notebooks:
   ```bash
   jupyter notebook
   ```

4. Run the notebooks in order:
   - Start with `elevate_lab_t1.ipynb` for data preprocessing
   - Continue with `elevate_lab_t2.ipynb` for visualization and analysis

## Notebooks

### elevate_lab_t1.ipynb - Data Preprocessing

This notebook focuses on:
- Loading and exploring the raw dataset
- Identifying missing values and data types
- Handling missing data using imputation strategies
- Encoding categorical variables using OneHotEncoder
- Creating the preprocessed dataset (`titanic-updated.csv`)

### elevate_lab_t2.ipynb - Exploratory Data Analysis

This notebook provides:
- Summary statistics for numerical features
- Data visualization using matplotlib and seaborn
- Analysis of survival rates across different passenger classes
- Correlation analysis between features

## Data Preprocessing

The preprocessing pipeline transforms the original dataset:

1. **Missing Value Handling**:
   - Age: Imputed using median/mean strategy
   - Embarked: Filled with mode or dropped
   - Cabin: Removed due to high percentage of missing values

2. **Feature Encoding**:
   - Sex: One-hot encoded to Sex_female, Sex_male
   - Embarked: One-hot encoded to Embarked_C, Embarked_S, Embarked_Q, Embarked_nan

3. **Output**:
   - The processed dataset (`titanic-updated.csv`) contains 719 records with 14 columns

## License

This project is available for educational and research purposes. The Titanic dataset is a public domain dataset commonly used for machine learning and data science education.

---

**Note**: This project was created for learning purposes as part of a data science training program.
