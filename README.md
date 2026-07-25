# Comprehensive Exploratory Data Analysis: FIFA 19 Player Dataset ⚽📊

An end-to-end Exploratory Data Analysis (EDA) and data preprocessing pipeline built with Python, analysing player statistics, valuations, and demographics from the official FIFA 19 dataset.

Built as part of the SkillOrbit Machine Learning internship.

**Author:** Parantap Guha

## 📌 Project Overview
This repository contains a structured analytical workflow designed to inspect, clean, and visualise the dataset. The project focuses on data hygiene, memory optimisation, and identifying statistical distributions and outliers across 18,000+ professional football players.
- Dataset Source: [FIFA 19 Complete Player Dataset](https://www.kaggle.com/datasets/winterbreeze/fifa19eda)

## 🗂️ Workflow & Methodology

### 1. Environment Setup & Data Ingestion
* Automated Kaggle API integration (`kaggle.json`) to download and extract dataset archives directly within the environment.
* Import of core data science libraries: `pandas`, `numpy`, `matplotlib`, and `seaborn`.

### 2. Structural Inspection
* Comprehensive audit of dataframe dimensions (**18,207 rows × 18 features**).
* Summary statistics (`describe()`) capturing central tendencies, dispersion, and range for all player metrics (Overall, Potential, Value, Wage, etc.).
* Memory usage monitoring and data type separation (numerical vs. categorical).

### 3. Data Cleaning & Preprocessing
* **Missing Value Imputation:** Numerical features (`Value`, `International Reputation`, `Skill Moves`) imputed using mean values.
* **Categorical Handling:** Dropped records with missing critical categorical data (`Club`, `Contract Valid Until`), resulting in a 100% clean dataset (0 nulls remaining).
* **Duplicate Audit:** Verified dataset integrity by screening for redundant records.
* **Data Type Optimisation:** Converted string dates (`Joined`, `Contract Valid Until`) to standard `datetime64[ns]` formats and categorical strings (`Club`, `Position`, `Nationality`, etc.) to Pandas `category` types for optimized memory usage.

### 4. Univariate Analysis
* Generated side-by-side comparative visualisations for all numerical features.
* **Histograms with KDE:** To identify data skewness and frequency distributions.
* **Boxplots:** To detect statistical outliers across player ratings, release clauses, physical attributes, and financial valuations.

## 🛠️ Technologies Used
* **Language:** Python 3
* **Data Manipulation:** Pandas, NumPy
* **Data Visualization:** Matplotlib, Seaborn
* **Environment:** Jupyter Notebook / Google Colab

## 🚀 How to Run
1. Clone the repository:
   ```bash
   git clone [https://github.com/ParantapGuha-2005/SkillOrbit_MinorProject1_Fifa19_EDA.git](https://github.com/ParantapGuha-2005/SkillOrbit_MinorProject1_Fifa19_EDA.git)
   ```
2. Install the required dependencies:
   ```bash
   pip install pandas numpy matplotlib seaborn kaggle
   ```
3. Ensure your Kaggle API key (`kaggle.json`) is placed in the `~/.kaggle/` directory if running the automated download cells, or manually place `fifa_eda.csv` in the root directory.
4. Launch Jupyter Notebook and open ParantapGuha_MinorProject_1.ipynb:
   ```bash
   jupyter notebook ParantapGuha_MinorProject_1.ipynb
   ```
