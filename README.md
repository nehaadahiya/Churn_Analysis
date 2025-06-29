# Customer Churn Analysis

## Project Story

Customer churn is one of the biggest silent threats to any subscription-based business. Understanding why customers leave — and identifying them before they go — can save millions in revenue and strengthen long-term relationships.

This project focuses on analyzing churn patterns using SQL for data exploration and Power BI for visualization. The goal: uncover actionable insights to help reduce churn and improve customer retention strategies.

## Project Overview

* **Objective**: Analyze customer churn data to identify key risk factors and visualize insights for business stakeholders.
* **Tools Used**:

  * SQL (for data cleaning, preparation, and exploratory analysis)
  * Power BI (for building interactive dashboards)

## Database & SQL Analysis

### Steps

1. **Data Cleaning & Preparation**

   * Handled missing values and inconsistent entries.
   * Converted data types where necessary.
   * Created derived columns such as tenure buckets and payment method categories.

2. **Exploratory SQL Queries**

```sql
SELECT Customer_Status, Count(Customer_Status) as TotalCount, Sum(Total_Revenue) as TotalRev,
Sum(Total_Revenue) / (Select sum(Total_Revenue) from stg_Churn) * 100  as RevPercentage
from stg_Churn
Group by Customer_Status;
```

## Power BI Dashboard

### Screenshot

#### Overall Churn Dashboard

![Dashboard Screenshot](/output_dashboard_powerbi.png)

### Dashboard Features

* Interactive filters for contract type, tenure, payment method, and more.
* Dynamic KPIs highlighting churn rates and revenue impact.
* Visual segmentation of high-risk customer groups.
* Clear storytelling visuals for business teams and decision-makers.

## Future Improvements

* Integrate predictive churn scoring using machine learning models.
* Add sentiment analysis from customer feedback surveys.
* Automate periodic data refresh for near real-time insights.

## Contact

For questions, ideas, or collaborations, feel free to reach out.

---

Turning raw data into loyalty — one insight at a time.
