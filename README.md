#  ETL Midterm Project – DSA 2040 A

**Student:** Kevin  
**ID:** 656  
**Project Folder:** ETL_Midterm_Kevin_656

---

##  1. Project Overview

This project demonstrates an end-to-end ETL (Extract, Transform, Load) pipeline using Python and realistic sales data. It includes extracting raw datasets, transforming them through cleaning and enrichment, and loading the cleaned data into structured formats for analysis.

---

##  2. ETL Phases

###  `etl_extract.ipynb`
- Loads `raw_data.csv` and `incremental_data.csv` from the `data/` folder
- Displays `.head()`, `.info()`, `.describe()` to inspect data
- Highlights missing values, duplicates, and structure issues

###  `etl_transform.ipynb`
- Applies 4+ meaningful transformations:
  - Filled missing `customer_name`, `quantity`, `unit_price`, `region`
  - Dropped rows with missing `order_date`
  - Created a `total_price = quantity × unit_price` column
  - Converted `order_date` to datetime
  - Added a bonus **bar chart visualization**
- Saves output to the `transformed/` folder

###  `etl_load.ipynb`
- Loads the cleaned data into a SQLite database (`.db`)
- Runs basic queries to validate inserted data
- Saves results into the `loaded/` folder

---

##  3. Tools Used

- Python 3.10+
- Pandas
- SQLite (via `sqlite3`)
- Matplotlib
- Jupyter Notebook
- Git + GitHub

---

##  4. How to Run the Project

``bash
# 1. Clone the repository
git clone https://github.com/kevinkorir2004/DSA2040A_ETL_Midterm_Kevin_656.git
cd DSA2040A_ETL_Midterm_Kevin_656

# 2. Install dependencies
pip install pandas matplotlib jupyter

# 3. Run notebooks in this order:
#    - etl_extract.ipynb
#    - etl_transform.ipynb
#    - etl_load.ipynb



##  Screenshot of Chart Output

Below is a screenshot of the actual chart generated in the notebook:

![Chart Screenshot](chart_screenshot.png)

