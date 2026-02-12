# Task_1
# 📊 Dataset Cleaning & Preparation (Python + Pandas)

This project demonstrates a robust data cleaning pipeline designed to transform messy, raw data into a structured, analysis-ready format. Using **Python** and **Pandas**, the script automates the handling of missing values, duplicates, and inconsistent formatting.


## Table of Contents
- [Objective](#objective)
- [Tech Stack](#tech-stack)
- [Cleaning Steps Performed](#cleaning-steps-performed)
- [Project Structure](#project-structure)
- [How to Run](#how-to-run)
- [Outcome](#outcome)

---

## 📌 Objective
The goal of this project is to process a raw dataset (`Mall_Customers.csv`) and resolve common data quality issues, making it suitable for Machine Learning, Business Intelligence, or Data Visualization.

**Key Issues Addressed:**
* Missing values (nulls)
* Duplicate records
* Inconsistent text formats
* Incorrect data types
* Unclean column headers

---

## 🛠 Tech Stack
* **Language:** Python 3.8+
* **Library:** Pandas
* **Data Format:** CSV

---

## ⚙️ Cleaning Steps Performed

### 1. Column Standardization
Converted all column names to **lowercase** and **snake_case** format to ensure easier coding and database compatibility.
> **Example:** `Annual Income (k$)` ➔ `annual_income_k$`

### 2. Missing Value Handling
* **Numerical columns:** Filled with the **Mean**.
* **Categorical columns:** Filled with the **Mode**.

### 3. Duplicate Removal
Identified and removed redundant rows using `df.drop_duplicates()` to prevent biased analysis.

### 4. Text Standardization
* Converted all text to lowercase.
* Trimmed extra leading/trailing whitespace.
* Standardized categorical values (e.g., mapping `M` or `m` to `male`).

### 5. Date & Type Fixing
* Converted date strings into proper `datetime` objects.
* Ensured numerical columns (like `age`) are stored as integers rather than floats or strings.

---

## 📦 Project Structure
```plaintext
dataset-cleaning-project/
│
├── Mall_Customers.csv          # Raw input dataset
├── cleaned_mall_customers.csv  # Final output dataset
├── data_cleaning.py            # Python script for cleaning
├── requirements.txt            # List of dependencies
└── README.md                   # Documentation
