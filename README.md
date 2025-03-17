# Data Cleaning Demo Project

![GitHub](https://img.shields.io/badge/Tools-Python-blue)
![GitHub](https://img.shields.io/badge/Libraries-Pandas|Numpy-orange)
![GitHub](https://img.shields.io/badge/Focus-Data_Cleaning-green)

This project demonstrates the process of cleaning and preprocessing a dataset using Python libraries like **Pandas** and **Numpy**. The dataset contains information about products, including SKU, branch, price, stock, and other attributes. The goal is to handle missing values, clean the data, and extract useful insights for further analysis.

---

## Table of Contents
- [Overview](#overview)
- [Steps for Data Cleaning](#steps-for-data-cleaning)
  - [Import Data](#1-import-data)
  - [Handling Missing Values](#2-handling-missing-values)
  - [Cleaning & Trimming Rows](#3-cleaning--trimming-rows)
  - [Data Transformation](#4-data-transformation)
  - [Feature Engineering](#5-feature-engineering)
- [Key Insights](#key-insights)
- [Conclusion](#conclusion)

---

## Overview
The dataset consists of two main files:
1. **PRICES-STOCK.csv**: Contains information about product prices, stock, and branch details.
2. **PRODUCTS.csv**: Contains detailed product information such as SKU, description, category, and brand.

The data cleaning process involves:
- Handling missing values.
- Cleaning and trimming unnecessary rows.
- Transforming categorical data.
- Extracting useful features from the description.

---

## Steps for Data Cleaning

### 1. Import Data
The dataset was imported using Python's **Pandas** library. Two main files were loaded:
- **PRICES-STOCK.csv**: Contains product prices, stock, and branch information.
- **PRODUCTS.csv**: Contains detailed product descriptions, categories, and other attributes.

---

### 2. Handling Missing Values
Missing values were identified and handled appropriately:
- **Branch Information**: 19.96% of the records had missing branch information. These rows were removed as they did not provide significant insights.
- **BUY_UNIT**: 33.3% of the records had missing values. These were marked as **'N/A'**.
- **DESCRIPTION_STATUS**: 20.07% of the records had missing values. These were marked as **'N/A'**.
- **ORGANIC_ITEM**: 33.33% of the records had missing values. These were marked as **'N/A'**.

---

### 3. Cleaning & Trimming Rows
- Rows with missing branch information were removed.
- Unnecessary columns like `SUB_CATEGORY` and `SUB_SUB_CATEGORY` were dropped to simplify the dataset.

---

### 4. Data Transformation
- The **DESCRIPTION** column was cleaned by removing HTML tags (`<p>` and `</p>`).
- Categorical columns like `BUY_UNIT`, `DESCRIPTION_STATUS`, and `ORGANIC_ITEM` were transformed to handle missing values effectively.

---

### 5. Feature Engineering
- A new feature called **Package** was created by extracting information from the **DESCRIPTION** column. This feature identifies the type of packaging (e.g., 'UN', 'KG', 'LT', 'PZA', 'ML', 'GRS') based on keywords in the description.

---

## Key Insights
- **Branch Information**: 19.96% of the records had missing branch information. These rows were removed as they did not provide significant insights.
- **BUY_UNIT**: 33.3% of the records had missing values. These were marked as **'N/A'**.
- **DESCRIPTION_STATUS**: 20.07% of the records had missing values. These were marked as **'N/A'**.
- **ORGANIC_ITEM**: 33.33% of the records had missing values. These were marked as **'N/A'**.
- **Package Information**: The **Package** feature was successfully extracted from the **DESCRIPTION** column, providing additional insights into product packaging.

---

## Conclusion
The data cleaning process successfully handled missing values, removed unnecessary rows, and transformed the dataset for further analysis. Key features like **Package** were extracted, and categorical data was cleaned and standardized. This cleaned dataset is now ready for exploratory data analysis (EDA) and modeling.

---
