# HR Analytics Dashboard – Employee Attrition & Workforce Insights (Power BI)

Interactive 4-page Power BI report built on an HR analytics dataset from Kaggle. The dashboard helps HR understand attrition patterns, pay fairness, engagement levels, and career growth across the organization.


## 1. Project Overview

This project simulates an HR analytics use case where an internal HR team wants to answer:

- Who is leaving the company, and what are the main drivers of attrition?
- Is compensation fair across departments, job roles, and gender?
- How engaged and satisfied are employees, and does that link to attrition?
- Where do career growth and promotion bottlenecks appear?

The result is a navigable Power BI report with a Home page and four focused dashboard pages.


## 2. Data

- **Source**: [HR Analytics – Kaggle (by Rushikesh Konapure)](https://www.kaggle.com/datasets/rishikeshkonapure/hr-analytics-prediction)
- **Format**: Original CSV converted to Excel and cleaned in Power Query
- **Key fields** (examples – adjust to your actual columns):
  - Demographics: `Age`, `Gender`, `MaritalStatus`
  - Job: `Department`, `JobRole`, `JobLevel`, `BusinessTravel`
  - Pay: `MonthlyIncome` (or salary field in your dataset), `PercentSalaryHike` / pay-hike related fields
  - Engagement & performance: satisfaction / performance / work–life–related fields
  - Tenure & growth: tenure at company and related experience fields
  - Target: attrition / churn / left flag (depending on column naming)

### Data preparation (Power Query)

- Checked for and removed:
  - Blank rows
  - Duplicate columns
  - Non-informative or constant columns
- Standardized data types (numeric, text, date)
- Created derived fields where relevant, for example:
  - Age bands (e.g., 20–29, 30–39, 40–49, 50+)
  - Income bands (Low / Medium / High based on salary)
  - Tenure bands (0–2, 3–5, 6–10, 10+)
- Renamed columns into HR-friendly labels for use in visuals


## 3. Dashboard Structure

### Home – Navigation Hub
Landing page with buttons to navigate to:
- Overview & Attrition
- Compensation & Fairness
- Engagement & Performance
- Tenure & Growth


### Page 1 – Overview & Attrition

**Goal:** High-level view of the workforce and attrition patterns.

- KPIs:
  - Total employees
  - Attrition count
  - Attrition rate
  - Average age
  - Average monthly income / salary
  - Avg Years in company
- Visuals:
  - Attrition by Department
  - Attrition by Job Role
  - Attrition by Gender and Age band
  - Attrition by Education / Education Field 
  - Attrition by Years at Company band


### Page 2 – Compensation & Fairness

**Goal:** Explore pay structure and fairness across different groups.

- KPIs:
  - Average and median income/salary
  - Average salary hike (if present)
  - Average stock/benefit level (if present)
- Visuals:
  - Average income by Department and JobRole
  - Average income by Gender (within Department/JobRole)
  - Attrition rate by Income Band (Low / Medium / High)
  - Salary hike vs Attrition (leavers vs stayers)
  - Attrition by stock/benefit level (if applicable)


### Page 3 – Engagement, Performance & Workload

**Goal:** Understand how satisfaction, performance, and workload relate to attrition.

- KPIs:
  - Average satisfaction scores (job / environment / relationship – depending on available columns)
  - Average work–life balance (if available)
  - Percentage of employees working overtime / high workload (if available)
- Visuals:
  - Attrition by satisfaction level
  - Average satisfaction by Department and/or JobRole
  - Performance rating distribution split by Attrition (Yes / No)
  - Attrition vs overtime / workload level


### Page 4 – Tenure & Growth

**Goal:** Analyze retention over the employee lifecycle and career growth signals.

- KPIs:
  - Average tenure at company
  - Average time in current role
  - Average time since last promotion (if present)
  - Average manager tenure / experience fields
  - Training count / learning-related metrics (if present)
- Visuals:
  - Attrition by tenure band
  - Average tenure by Department
  - Attrition by time since promotion (if present)
  - Attrition by training / development metrics (if present)


## 5. Key Insights (example placeholders)

Replace these with your actual findings after exploring the Kaggle dataset:

- Certain departments and roles show significantly higher attrition than others.
- Lower income bands have higher attrition compared to higher bands.
- Lower satisfaction scores and heavier workload correlate with higher attrition.
- Employees with shorter tenure or long time without growth show higher likelihood of leaving.


## 6. Tools & Skills

- **Power BI Desktop**
  - Data modeling
  - DAX measures (Attrition Rate, % of employees, average metrics)
  - Slicers and cross-filtering
  - Page navigator and button-based navigation
- **Power Query**
  - Data cleaning and type conversion
  - Calculated columns for bands (age, income, tenure)
- **Domain**
  - HR analytics: attrition, compensation, engagement, tenure
  - Dashboard design and storytelling for business stakeholders


## 7. How to Use This Report

1. Install **Power BI Desktop**.
2. Clone or download this repository.
3. Open the `.pbix` file in Power BI Desktop.
4. If prompted, point the data source to the Excel/CSV version of  
   [`hr-analytics-prediction` by Rushikesh Konapure](https://www.kaggle.com/datasets/rishikeshkonapure/hr-analytics-prediction).
5. Use slicers (Department, JobRole, Gender, Age band, Income band, Attrition, etc.) to explore each page.

## 8. Repository Structure (example)

