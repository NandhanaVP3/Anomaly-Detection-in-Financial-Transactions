# SQL Anomaly Detection in Financial Transactions

## Overview

This project demonstrates anomaly detection in financial transaction data using **SQL only**. It identifies outlier transactions per user using the Z-score statistical method—no Python or BI tools required. This approach highlights advanced SQL analytics, suitable for interviews and real-world use cases.

---

## Project Structure

```
sql-anomaly-detection/
├── data/
│   └── transactions.csv
├── queries/
│   └── anomaly_detection.sql
├── README.md
```

---

Dataset

A sample dataset of 10 transactions from 3 users across different merchants and locations.  
File: `data/transactions.csv`

---

How It Works

1. **Database Setup**
    - Create the `transactions` table using the provided schema.
    - Import the `transactions.csv` file into your SQL database.

2. **Statistical Analysis**
    - Calculate the average (`AVG`) and standard deviation (`STDDEV_POP`) of transaction amounts per user.

3. **Z-score Calculation**
    - For each transaction, calculate its Z-score relative to the user's mean and standard deviation.

4. **Anomaly Detection**
    - Transactions with an absolute Z-score greater than 2.5 are flagged as anomalies.

---

SQL Script Usage

- Run the SQL script in `queries/anomaly_detection.sql` in your database environment.
- Edit import statement as needed for your DBMS (e.g., PostgreSQL: `COPY`, MySQL: `LOAD DATA INFILE`, SQLite: `.import`).
- The final query outputs a table of flagged anomalous transactions.

---
