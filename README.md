# Customer Behaviour Analysis

## Project Overview
This project focuses on analyzing customer purchasing behavior using Python, PostgreSQL, and Power BI. The objective is to uncover meaningful insights from customer transaction data, identify purchasing patterns, evaluate customer preferences, and create an interactive dashboard to support business decision-making.

---

## Dataset Summary

The dataset consists of **3,900 customer transaction records** with **18 columns**, capturing customer demographics, purchasing behavior, shopping preferences, and transaction details.

The features are grouped as follows:

### Customer Demographics
- Customer ID
- Age
- Gender
- Location

### Purchase Details
- Category
- Item Purchased
- Purchase Amount
- Previous Purchases
- Frequency of Purchases

### Shopping Preferences
- Size
- Color
- Season
- Shipping Type
- Payment Method

### Customer Experience
- Review Rating
- Subscription Status
- Discount Applied
- Promo Code Used

## Exploratory Data Analysis Using Python

Exploratory Data Analysis (EDA) was performed using **Python** to understand the dataset, clean the data, engineer new features, and prepare it for PostgreSQL and Power BI analysis.

### Libraries Used

- Pandas
- NumPy

### Data Cleaning

- Inspected the dataset structure and verified data types.
- Checked for missing values across all columns.
- Replaced missing values in the **Review Rating** column with the **median review rating of the corresponding product category**.
- Standardized column names by:
  - Converting all column names to lowercase.
  - Replacing spaces with underscores for consistency.
- Removed duplicate/redundant columns.
- Dropped the **promo_code_used** column since it contained the same information as **discount_applied**.

### Feature Engineering

#### Age Group Creation

Created a new **age_group** column by categorizing customers into:

- Young Adult
- Adult
- Middle Aged
- Aged

#### Purchase Frequency Transformation

Converted the categorical **frequency_of_purchases** column into a numerical feature named **purchases_frequency_days**.

Example mapping:

| Original Value | Days |
|---------------|-----:|
| Weekly | 7 |
| Bi-Weekly | 14 |
| Fortnightly | 14 |
| Monthly | 30 |
| Quarterly | 90 |
| Every 3 Months | 90 |
| Annually | 365 |

### Data Validation

- Verified the transformed columns.
- Reviewed the final dataset structure after preprocessing.

### PostgreSQL Integration

After preprocessing, the required packages were installed:

```bash
pip install psycopg2-binary sqlalchemy
```

The cleaned dataset was then:

- Connected to PostgreSQL using SQLAlchemy.
- Loaded into a PostgreSQL database.
- Prepared for SQL-based business analysis and Power BI visualization.

### Analysis Performed

- Dataset overview
- Missing value analysis
- Data type validation
- Summary statistics
- Distribution of purchase amounts
- Customer age distribution
- Gender distribution
- Product category analysis
- Correlation analysis
- Purchase trend visualization

---

## Data Analysis Using PostgreSQL

SQL queries were written to answer various business questions, including:

- Total revenue generated
- Average purchase amount by gender
- Discount usage analysis
- Subscription analysis
- Customer segmentation
- Top-selling products
- Revenue contribution by category
- Revenue contribution by age group
- Shipping type comparison
- Repeat customer analysis
- Product purchase rankings
- Customer behavior insights

---

## Power BI Dashboard

An interactive Power BI dashboard was developed to visualize customer behavior.

### Dashboard Features

- Total Customers
- Average Purchase Amount
- Average Review Rating
- Discounted Purchases
- Revenue by Category
- Revenue by Gender
- Revenue by Shipping Type
- Subscription Status Distribution
- Product Purchase Treemap
- Interactive Filters and Visualizations

---

## Key Performance Insights / Business Insights

- Clothing generated the highest revenue among all product categories.
- Average purchase amount remained consistent across customer segments.
- Female and male customers contributed nearly equal revenue.
- A significant percentage of customers used discounts while shopping.
- Subscription status influenced customer purchasing behavior.
- Certain products consistently received higher purchase counts.
- Shipping preferences varied across customer groups.
- Customer review ratings remained consistently high, indicating overall customer satisfaction.

---

## Technologies Used

- Python
- PostgreSQL
- Power BI
- Pandas
- NumPy
- Matplotlib
- Seaborn
- SQL

---

## Project Structure

```
customer_behaviour_analysis/
│
├── customer_behaviour.ipynb
├── requirements.txt
├── README.md
├── PowerBI_Dashboard.pbix
├── dataset/
└── images/
```

---

## Author

**Roshika**
