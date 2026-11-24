# 🛍️ Customer Shopping Behavior Analysis

## 📌 Project Overview

This project focuses on analyzing customer shopping behavior using Python, Pandas, and MySQL. The objective is to clean and prepare customer shopping data, perform feature engineering, and store the processed dataset in a MySQL database for further analysis.

The project demonstrates practical data analytics skills, including data exploration, data cleaning, missing value treatment, feature engineering, and database integration.

## 🎯 Project Objectives

- Explore and understand customer shopping data.
- Identify and handle missing values.
- Clean and standardize dataset column names.
- Perform feature engineering to create meaningful variables.
- Categorize customers based on age groups.
- Convert purchase frequency into days.
- Remove unnecessary columns.
- Connect Python with MySQL.
- Store the cleaned dataset in a MySQL database.

## 🛠️ Tools & Technologies

| Tool | Purpose |
|---|---|
| Python | Data analysis and processing |
| Pandas | Data cleaning and manipulation |
| Jupyter Notebook | Development environment |
| MySQL | Database management |
| SQLAlchemy | Database connectivity |
| PyMySQL | Python-MySQL connection |

## 📂 Project Structure

```text
Customer-Shopping-Behavior-Analysis/
│
├── Customer Shopping Behavior.ipynb
├── customer_shopping_behavior.csv
├── README.md
│
└── requirements.txt
```

## 🔍 Project Workflow

### 1. Data Loading & Exploration
- Imported the dataset using Pandas.
- Inspected the first five records.
- Checked dataset information and data types.
- Generated descriptive statistics.
- Identified missing values.

### 2. Data Cleaning
- Checked missing values in each column.
- Filled missing Review Rating values using the median rating within each product category.
- Standardized column names into lowercase.
- Replaced spaces with underscores.
- Renamed `purchase_amount_(usd)` to `purchase_amount`.

### 3. Feature Engineering

**Created Age Groups**

Divided customers into four age groups using Pandas `qcut()`:

- Young Adult
- Adult
- Middle Aged
- Senior

**Created Purchase Frequency Days**

Converted purchase frequency categories into numerical day values:

| Purchase Frequency | Days |
|---|---:|
| Weekly | 7 |
| Fortnightly | 14 |
| Bi-Weekly | 14 |
| Monthly | 30 |
| Quarterly | 90 |
| Every 3 Months | 90 |
| Annually | 365 |

### 4. Data Transformation
- Removed the unnecessary `promo_code_used` column.
- Prepared the cleaned dataset for database storage.

### 5. MySQL Database Integration

Connected Python to MySQL using SQLAlchemy and PyMySQL.

**Database Name:** `customer_behavior`

**Table Name:** `customer`

Performed the following operations:
- Established a MySQL connection.
- Tested the database connection.
- Uploaded the processed DataFrame into MySQL.
- Retrieved the first five records using SQL.

## 💻 Installation & Setup

### Step 1: Clone the Repository

```bash
git clone https://github.com/your-username/Customer-Shopping-Behavior-Analysis.git
```

### Step 2: Install Required Libraries

```bash
pip install pandas sqlalchemy pymysql jupyter
```

### Step 3: Configure MySQL

Create the database:

```sql
CREATE DATABASE customer_behavior;
```

### Step 4: Configure Database Connection

Update your Python database credentials:

```python
from sqlalchemy import create_engine, URL

connection_url = URL.create(
    "mysql+pymysql",
    username="your_username",
    password="your_password",
    host="localhost",
    port=3306,
    database="customer_behavior"
)

engine = create_engine(connection_url)
```

Use environment variables for credentials rather than publishing passwords on GitHub.

### Step 5: Run the Jupyter Notebook

```bash
jupyter notebook
```

Open `Customer Shopping Behavior.ipynb` and execute the cells sequentially.

## 📊 Skills Demonstrated

- Data Cleaning
- Exploratory Data Analysis (EDA)
- Missing Value Treatment
- Data Transformation
- Feature Engineering
- Pandas Data Manipulation
- Python Programming
- MySQL Database Integration
- SQLAlchemy
- Data Preparation

## 💡 Key Learning Outcomes

Through this project, I gained hands-on practical experience in:

- Working with real-world customer shopping data.
- Identifying and handling missing values.
- Creating meaningful analytical features.
- Transforming raw data into structured information.
- Integrating Python with MySQL.
- Preparing datasets for further business analysis.

## 👩‍💻 Author

**Bharti Koli**

Aspiring Data Analyst | Python | SQL | Excel | Power BI

- GitHub: https://github.com/your-username
- LinkedIn: Add your LinkedIn profile URL
- Email: bhartikoli0105@gmail.com

---

⭐ If you find this project useful, feel free to star the repository!

**Thank you for visiting my project!**
