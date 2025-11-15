# Titanic Data Preprocessing and Exploratory Data Analysis (EDA)

<p align="center">
  <img src="https://upload.wikimedia.org/wikipedia/commons/f/fd/RMS_Titanic_3.jpg" alt="Titanic Logo" width="450"/>
</p>

This repository contains a Jupyter Notebook **`task-1.ipynb`** that demonstrates clean and structured preprocessing steps along with essential EDA on the Titanic dataset.

---

## 📥 Data Loading & Initial Inspection
- The dataset is loaded directly from a public GitHub URL.
- Initial inspection includes:
  - Viewing first few rows
  - Checking data types
  - Identifying missing values
  - Understanding dataset structure

Dataset Source:
https://raw.githubusercontent.com/datasciencedojo/datasets/master/titanic.csv

---

## 🧹 Data Cleaning

### **1. Handling Missing Values**
- **Cabin** column dropped due to excessive missing values.
- **Embarked** missing values filled using **mode**.
- **Age** missing values filled using **median**.

### **2. Outlier Detection & Removal**
A custom function `remove_outliers_iqr` is used to clean numeric columns:
- Age  
- SibSp  
- Parch  
- Fare  

The function applies the **IQR (Interquartile Range)** method:
- Any value outside **1.5 × IQR** from Q1 or Q3 is treated as an outlier and removed.

---

## 📊 Data Visualization
Box plots are generated before and after outlier removal for numeric columns, enabling a clear comparison of distribution changes.

---

## 💾 Installation
Install required libraries using:
pip install pandas numpy seaborn matplotlib

---

## 🚀 Usage Instructions
1. Download **`task-1.ipynb`**  
2. Open in **Jupyter Notebook** or **JupyterLab**  
3. Run all cells to execute:
   - Data loading  
   - Data cleaning  
   - Outlier removal  
   - Visualizations  

Output includes:
- Cleaned DataFrame shape  
- Before/after box plots  

---

## 📁 Project Structure
├── task-1.ipynb
└── README.md

---

## ✔️ Summary
This notebook provides a clear, step-by-step approach for:
- Cleaning missing data  
- Handling outliers  
- Visualizing distributions  
- Preparing the Titanic dataset for modeling  

A solid foundation for machine learning tasks on the Titanic dataset.
