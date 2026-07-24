# SALES_ETL
# ETL Pipeline: CSV to PostgreSQL

## Project Overview

This project demonstrates an ETL (Extract, Transform, Load) pipeline using Python. The pipeline extracts sales data from a CSV file, performs basic data cleaning and transformation, and loads the cleaned data into a PostgreSQL database.

---

## Technologies Used

- Python
- Pandas
- PostgreSQL
- psycopg2

---

## ETL Process

### 1. Extract

The extract stage reads the sales dataset from a CSV file into a Pandas DataFrame.

### 2. Transform

The transform stage performs the following operations:

- Removes duplicate records
- Handles missing values
- Converts column names to uppercase
- Converts appropriate columns to the correct data types
- Performs basic data cleaning

### 3. Load

The cleaned data is inserted into a PostgreSQL table named **Sales_Record** using psycopg2.

Duplicate records are ignored using PostgreSQL's `ON CONFLICT DO NOTHING`.

---

## How to Run

1. Install the required packages.

```bash
pip install -r requirements.txt
```

2. Ensure PostgreSQL is running.

3. Create the required database and table.

4. Update the database credentials inside `etl.py`.

5. Run the script.

```bash
python etl.py
```

---

## Expected Output

When the script runs successfully, it will:

- Read the CSV file
- Clean and transform the data
- Insert the records into PostgreSQL
- Display a success message

Example:

```
Connected to PostgreSQL
250 records loaded successfully.
Connection closed.
```

---

## Author

**Adeyemi Tomiwa**

Data Analyst | Python | SQL | PostgreSQL | Power BI
