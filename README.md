# ecommerce-funnel-analysis
Diagnosing a sales funnel collapse &amp; data integrity issue using GA4 data and SQL.

## Business Problem
The leadership team needed visibility into website performance to make informed decisions about marketing and product strategy. However, a deep dive into the data revealed that critical financial metrics (revenue, profit) were not reliably populated.

## Solution: The Pivot
Faced with this real-world data constraint, I pivoted the analysis from pure financials to **user engagement and behavioral metrics**. I engineered a SQL data model to reconstruct the customer journey and identify key drop-off points in the sales funnel.

## Key Insights Delivered
- **Traffic Volume:** The site attracted 2,546 unique users generating over 25,489 sessions in a single day.
- **Critical Leak:** A massive 92.8% of users dropped off between the homepage and product pages, indicating a major site navigation or usability issue.
- **Data Advocacy:** The analysis served a dual purpose: it provided immediate insights into user behavior and also functioned as a data quality audit, clearly demonstrating to the engineering team the critical need to fix the transaction data pipeline.

## Technical Details
- **Tools:** Google BigQuery (SQL), Microsoft Excel 
- **Data Challenge:** Primary financial metrics were null due to a known data collection issue within the GA4 dataset.
- **Methodology:** Developed a robust SQL query to calculate proxy metrics for engagement and build a view of the sales funnel without relying on revenue data.

## Recommendations
1.  **Immediate:** Focus UX/Product efforts on the homepage and navigation to improve product discovery.
2.  **Critical:** Task the data engineering team with resolving the instrumentation flaw that is preventing the capture of purchase revenue data.

---

### Dashboard Preview:
![Sales Funnel Dashboard](dashboard.png)
