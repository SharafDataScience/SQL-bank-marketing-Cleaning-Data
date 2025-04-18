# Bank Marketing Data Cleaning Project

## Project Overview

This project involves cleaning and restructuring data collected from a bank's personal loan marketing campaign. The cleaned data will be used to populate a PostgreSQL database and serve as a template for importing data from future campaigns.

The source data is provided in a CSV file named `bank_marketing.csv`, and the output consists of three cleaned CSV files ready for ingestion into a relational database.

---

## Dataset Source

- **Original File**: `bank_marketing.csv`
- **Provided By**: Bank's marketing team
- **Context**: Collected during a campaign promoting personal loans in the UK.

---

## Goals

- Clean and validate raw marketing data
- Reformat and split the data into structured tables
- Ensure compatibility with PostgreSQL database schema
- Output three CSV files:
  1. `customers.csv`
  2. `campaigns.csv`
  3. `loans.csv`

---

## File Descriptions

### 1. `customers.csv`

Contains customer personal and demographic information.

**Columns:**
- `customer_id` (Primary Key)
- `age` (Integer)
- `job` (Categorical)
- `marital_status` (Categorical)
- `education` (Categorical)
- `default` (Boolean)
- `housing` (Boolean)
- `loan` (Boolean)

---

### 2. `campaigns.csv`

Includes data related to each customer's interaction with the marketing campaign.

**Columns:**
- `campaign_id` (Primary Key)
- `customer_id` (Foreign Key)
- `contact_method` (Categorical)
- `contact_day` (Integer)
- `contact_month` (Categorical)
- `campaign_calls` (Integer)
- `previous_contacts` (Integer)
- `previous_outcome` (Categorical)

---

### 3. `loans.csv`

Records whether the customer subscribed to a personal loan product.

**Columns:**
- `loan_id` (Primary Key)
- `customer_id` (Foreign Key)
- `loan_subscribed` (Boolean)

---

## How to Run

1. Load the Jupyter notebook `Bank_loan.ipynb`.
2. Execute all cells to process the raw `bank_marketing.csv`.
3. The script will output the three cleaned CSV files:  
   - `customers.csv`  
   - `campaigns.csv`  
   - `loans.csv`  
   in the same directory.

---

## Requirements

- Python 3.8+
- pandas
- numpy
- Jupyter Notebook

Install required libraries using:
```bash
pip install pandas numpy
