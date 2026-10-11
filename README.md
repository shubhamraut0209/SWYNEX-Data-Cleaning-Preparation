# SWYNEX Internship — Task 1: Data Cleaning & Preparation

## 📌 Project Overview

This project was completed as part of **Task 1 of my internship with SWYNEX Technologies**.

The objective was to identify data quality issues in a public e-commerce transactions dataset and prepare the data for further analysis using **Python and Pandas**.

Data cleaning is an essential step in the data analytics workflow because accurate, consistent, and reliable data supports meaningful analysis and better decision-making.

## 🎯 Objectives

- Identify missing values and duplicate records.
- Detect inconsistent categorical values.
- Inspect and standardize date formats and data types.
- Identify invalid quantity values.
- Apply appropriate data-cleaning techniques.
- Validate the cleaned dataset.
- Generate a data quality report documenting the results.

## 🛠️ Tools & Technologies

- **Python**
- **Pandas** — data manipulation and cleaning
- **NumPy** — numerical operations
- **Google Colab** — notebook development and execution
- **GitHub** — project documentation and version control

## 📂 Dataset Information

The project uses a public e-commerce retail transactions dataset containing information about orders, customers, products, prices, discounts, payment methods, shipping locations, order statuses, and customer ratings.

The dataset includes fields such as:

- Order ID and Customer ID
- Order Date
- Product Category and Product Name
- Quantity and Unit Price
- Discount Percentage
- Payment Method
- Shipping City and Country
- Order Status
- Customer Rating

**Source:** [Public dataset repository](https://github.com/Prithv122/messy-data-eda)

The original dataset is preserved separately from the cleaned output to maintain traceability.

## 🔍 Data Quality Issues Identified

The initial inspection identified several data quality concerns:

- Missing values in discount percentage, shipping city, and customer rating.
- Exact duplicate records.
- Inconsistent payment method labels, including differences in capitalization, spacing, and punctuation.
- Inconsistent country names and abbreviations.
- Multiple date formats in the order date column.
- Invalid quantity values, including zero and negative quantities.

## 🧹 Data Cleaning & Preparation

The following cleaning steps were implemented using Python and Pandas:

1. **Data inspection:** Examined dataset dimensions, column names, data types, missing values, unique values, and duplicate records.
2. **Column standardization:** Standardized column names for consistent processing.
3. **Duplicate handling:** Identified and removed exact duplicate rows.
4. **Whitespace cleaning:** Removed unnecessary leading and trailing whitespace from applicable text values.
5. **Categorical standardization:** Normalized inconsistent payment method labels and country names using explicit mappings.
6. **Date standardization:** Parsed supported date formats into a consistent datetime representation and checked for unparsed values.
7. **Data type validation:** Converted applicable columns to appropriate data types.
8. **Invalid quantity handling:** Removed records with zero or negative quantities according to the project's cleaning rules.
9. **Missing value handling:** Applied field-specific decisions rather than treating all missing values identically.

### Missing Value Handling Decisions

| Column | Treatment | Reason |
|---|---|---|
| Discount Percentage | Missing values filled with `0` | Assumes a blank discount represents no discount; this assumption should be validated where possible. |
| Shipping City | Missing values retained | The correct city cannot be reliably inferred from the available data. |
| Customer Rating | Missing values retained | A missing rating does not mean a rating of zero. |

These decisions were made to improve data quality while avoiding unsupported assumptions about unknown values.

## ✅ Validation

After cleaning, the dataset was checked for:

- Remaining exact duplicate records.
- Missing values in relevant columns.
- Appropriate data types.
- Consistency of standardized categorical values.
- Successful export and reloading of the cleaned CSV file.

A separate data quality report was generated to document relevant column-level information before and after cleaning.

## 📁 Project Structure

```text
SWYNEX-Data-Cleaning-Preparation/
│
├── data/
│   ├── raw/
│   │   └── ecommerce_retail_transactions_raw.csv
│   │
│   └── cleaned/
│       └── ecommerce_retail_transactions_cleaned.csv
│
├── notebooks/
│   └── Task_1_Data_Cleaning.ipynb
│
├── outputs/
│   └── data_quality_report.csv
│
├── README.md
└── requirements.txt
```

## 🚀 How to Run the Project

1. Clone or download this repository.
2. Install the required Python libraries.
3. Open `notebooks/Task_1_Data_Cleaning.ipynb` in Google Colab or a compatible Jupyter environment.
4. Upload the raw CSV dataset when prompted, or update the notebook's input path to match your local project structure.
5. Run the notebook cells in order.
6. Review the validation results and generated output files.

### Install Dependencies

```bash
pip install -r requirements.txt
```

## 📌 Deliverables

- Original raw dataset.
- Cleaned e-commerce transactions dataset.
- Jupyter notebook documenting the cleaning workflow.
- Data quality report.
- Project documentation.

## 📚 Key Learnings

This task strengthened my understanding of practical data preparation, including duplicate detection, missing value treatment, categorical standardization, date parsing, data type validation, and quality checks.

It also reinforced the importance of documenting cleaning assumptions and validating outputs before using data for further analysis.

## 👨‍💻 Internship

**Organization:** SWYNEX Technologies  
**Task:** Task 1 — Data Cleaning & Preparation  
**Tools:** Python, Pandas, NumPy, Google Colab

---

*This project was developed for learning and practical application of data cleaning and preparation techniques as part of an internship task.*
