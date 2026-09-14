# Data Ingestion, Cleaning & Preprocessing with Pandas

## Project Overview

This project demonstrates a complete data ingestion, cleaning, and preprocessing workflow using **Python and Pandas** on a real-world style retail sales dataset containing more than **12,000 records**.

The raw dataset intentionally contains common data-quality issues such as missing values, duplicate records, inconsistent text formatting, inconsistent data types, and invalid values. The objective is to transform this messy dataset into a clean, standardized dataset suitable for further analysis and business intelligence.

---

## Objectives

- Load and inspect a raw retail sales dataset using Pandas.
- Identify missing values and duplicate records.
- Detect and handle invalid or inconsistent data.
- Standardize categorical values and data types.
- Handle missing values through appropriate imputation.
- Perform feature engineering using date and financial fields.
- Calculate profit and profit margin.
- Export the final cleaned dataset as a CSV file.

---

## Dataset

The project uses a retail sales transaction dataset containing **12,000+ records**.

### Main Columns

| Column | Description |
|---|---|
| `order_id` | Unique order identifier |
| `order_date` | Date of the transaction |
| `customer_id` | Customer identifier |
| `product` | Product purchased |
| `region` | Sales region |
| `sales_channel` | Online, Store, or Marketplace |
| `quantity` | Number of units purchased |
| `unit_price` | Price per unit |
| `discount_pct` | Discount percentage |
| `sales_amount` | Total sales/revenue |
| `cost_amount` | Cost associated with the order |
| `profit` | Sales amount minus cost |
| `profit_margin_pct` | Profit as a percentage of sales |
| `year` | Extracted year |
| `month` | Extracted month |
| `month_name` | Month name |
| `quarter` | Extracted quarter |

---

## Data Quality Issues Addressed

The raw dataset contains several common data-quality problems:

- Missing customer IDs
- Missing regions
- Missing prices and discount values
- Duplicate transaction records
- Inconsistent date formats
- Inconsistent categorical text formatting
- Numeric fields stored in inconsistent formats
- Invalid quantities
- Invalid or negative prices

These issues are identified and handled systematically using Pandas.

---

## Data Cleaning Process

### 1. Data Ingestion

The raw CSV file is loaded into Pandas using:

`pd.read_csv()`

The dataset is then inspected for:

- Number of rows and columns
- Missing values
- Duplicate records
- Data types
- Statistical information

### 2. Text Standardization

Categorical fields are cleaned by:

- Removing leading/trailing spaces
- Standardizing capitalization
- Normalizing category values

### 3. Date Conversion

Different date formats are converted into a consistent Pandas datetime format.

### 4. Numeric Conversion

Numeric columns are explicitly converted to appropriate numeric data types.

### 5. Duplicate Removal

Exact duplicate records are identified and removed to prevent double-counting.

### 6. Invalid Value Handling

Invalid quantities and non-positive prices are identified and treated as missing values before imputation.

### 7. Missing Value Handling

Missing values are handled using appropriate techniques:

- Median imputation for numeric fields
- Product-level median for missing unit prices
- `"Unknown"` category for missing regions

### 8. Feature Engineering

New analytical features are created:

- Year
- Month
- Month name
- Quarter
- Profit
- Profit margin percentage

---

## Before vs After

The notebook includes data-quality checks before and after preprocessing, including:

- Duplicate count
- Missing-value count
- Invalid quantity count
- Invalid price count
- Final dataset dimensions

This provides evidence that the cleaning process successfully improved the dataset quality.

---

## Project Files

### `messy_retail_sales.csv`

The original raw dataset containing intentionally introduced data-quality issues.

### `Data_Ingestion_Cleaning_Preprocessing_Pandas.ipynb`

Jupyter Notebook containing the complete implementation, data-quality checks, cleaning process, feature engineering, and final validation.

### `clean_retail_sales.csv`

The final cleaned and standardized dataset ready for further analysis.

---

## Tools & Technologies

- **Python**
- **Pandas**
- **NumPy**
- **Jupyter Notebook**
- **CSV**

---

## Key Outcome

The project converts a messy retail transaction dataset into a structured and standardized dataset by applying a complete Pandas data-preprocessing workflow.

The final dataset can be used for:

- Exploratory Data Analysis
- Business reporting
- Data visualization
- Sales analysis
- Profitability analysis
- Machine learning preprocessing

---

## Author

**Snehil Raj**
