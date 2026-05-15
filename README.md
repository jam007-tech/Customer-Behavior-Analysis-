# Customer Behaviour Analysis

A complete end-to-end Data Analyst portfolio project analyzing customer shopping behaviour in the e-commerce domain.

---

## Project Overview

In the E-Commerce Industry, understanding customer behaviour is critical for business growth. This project analyzes 5,000 customer transactions to uncover purchasing patterns, revenue drivers, and actionable business insights.

**Business Problem:**
> How can a retail company understand customer purchasing behavior to increase revenue, improve customer retention, and optimize marketing strategies?

---

## Tech Stack

| Tool | Purpose |
|------|---------|
| Python (Pandas) | Data Cleaning & EDA |
| PostgreSQL | Data Storage & SQL Analysis |
| SQLAlchemy | Python to Database Pipeline |
| Power BI | Interactive Dashboard |

---

## Project Structure

```
 Customer-Behaviour-Analysis
 ┣ customer_shopping_behavior.csv     # Raw dataset (5000 records, 17 columns)
 ┣ Customer_Behavior.ipynb            # Python EDA & Data Cleaning
 ┣ Business_Questions.sql            # 12 SQL Business Queries
 ┣ Customer-Behavior-Analysis.pbix   # Power BI Dashboard
 ┗ Report-Customer Behavior Analysis.pdf  # Full Project Report
```

---

## Dataset

- **Type:** E-commerce
- **Records:** 5,000 customers
- **Columns:** 17 (Age, Gender, Category, Purchase Amount, Season, Payment Method, etc.)

---

##  Phase 1 — Python (EDA & Data Cleaning)

- Loaded and explored the raw dataset
- Fixed category inconsistencies using a mapping dictionary
- Handled missing values with domain-specific logic:
  - `Size` → Based on category (Not Applicable / Free Size / Mode)
  - `Review Rating` → Mean per product
  - `Purchase Amount` → Mean per product
  - `Previous Purchases` → Filled with 0
- Removed duplicate records by Customer ID
- Standardized column names to snake_case
- Exported cleaned data to PostgreSQL using SQLAlchemy

---

## Phase 2 — SQL (Business Insights)

12 business questions answered using PostgreSQL:

1. Which category generates the highest revenue?
2. Are discounts actually increasing purchase value?
3. Revenue breakdown by gender
4. Discount users who still spent above average
5. Top & Bottom 5 products by review rating
6. Average purchase: Standard vs Express shipping
7. Do subscribers spend more than non-subscribers?
8. Top 5 products with highest discount usage %
9. Customer segmentation — New / Returning / Loyal
10. Top 3 most purchased products per category
11. Are repeat buyers more likely to subscribe?
12. Revenue contribution by age group

**Key SQL concepts used:** Aggregations, CTEs, Window Functions (RANK), Subqueries, CASE statements

---

## Phase 3 — Power BI Dashboard

**Page 1 — Customer Analysis Revenue**
- KPI Cards: Total Customers, Unique Items, Avg Rating, Total Spend, Avg Spend
- Revenue by Gender, Category, Season, Location, Age Group, Payment Method
- Shipping Mode Analysis (Line & Clustered Column Chart)
- Interactive Slicers: Category | Gender | Discount | Subscription Status

**Page 2 — Best & Worst Performers**
- Top & Bottom 5 Items by Rating
- Top & Bottom 5 Items by Revenue
- Top & Bottom 5 Locations by Revenue

---

## Key Findings

- **Electronics** drives 49% of total revenue
- **Subscribers** spend 63% more than non-subscribers ($270 vs $165)
- **Discounts** increase average spend by 20% — they are profitable
- **51+ age group** contributes 40% of total revenue
- **62% of customers** are loyal (10+ purchases)
- **Phone** has the lowest rating (2.94) — needs quality improvement
- **New York** generates the highest location revenue

---

## Dashboard Preview
<img width="1082" height="590" alt="image" src="https://github.com/user-attachments/assets/d1158c99-0f8c-4c6f-af76-8c08c27c6a87" />
<img width="1071" height="588" alt="image" src="https://github.com/user-attachments/assets/0771d050-43e3-4949-a2b7-ded14ec044ef" />

---

## Author

**Aman Mishra**
NSUT
