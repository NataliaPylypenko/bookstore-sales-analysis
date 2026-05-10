# Bookstore Sales Analysis

## 📌 Project Overview

I took a "messy" sales file and cleaned it. I added new columns to help the business understand their profits and how fast they work.

## 🛠 What I did (Step-by-Step)

### 🗓 Sales Data Tab

I cleaned and improved the raw data to make it reliable for analysis.

- **Data Accuracy:** I recalculated the revenue in the `Net Revenue Cleaned` column to fix errors in the original file.

- **Logistics Integration:** I integrated shipping costs and carrier information from reference tables. This allows the business to see the total cost of every sale, including delivery.

- **Operational Metrics:** I extracted the `Order Date` and calculated `Lead Time (hours)`. This shows how much time the warehouse needs to process an order.

- **Profitability Tracking:** I added `COGS` for calculate the real profit for every transaction.

### 🗓 Publisher Analysis Tab

In this tab, I analyzed the performance of different publishers.

**1. Key Metrics Calculated:**

- **Net Revenue:** I extracted total sales after discounts by publisher. This shows the scale of the business.

- **Gross Margin:** I calculated profit after paying for the products (Net Revenue - COGS).

- **Margin %:** I calculated profitability of each publisher. It helps identify which partners are the most profitable.

**2. Pareto Analysis (80/20 Rule):**

I used the Pareto principle to find the most important publishers.

- **The logic:** I sorted publishers by Net Revenue and calculated the cumulative percentage.

- **Result:** I discovered that only **12% of publishers generate 80% of the total revenue**.

- **Business impact:** This means the business is highly dependent on a small group of top partners.

**3. Negative Margin Alerts:**

I found cases where the margin was negative.
This happened when discounts were too high or the purchase price (COGS) was higher than the selling price.

### 🗓 Customer Insights Tab

In this tab, I analyzed customer behavior and operational efficiency to understand purchasing patterns and warehouse performance.

**1. Key Metrics Calculated:**

- **Unique Customers (DAU):** I used the UNIQUE and FILTER functions to count how many individual people made a purchase each day. This distinguishes real customers from the total number of transactions.

- **Order Volume:** I tracked the total number of invoices per day to see the daily workload.

- **Average Order Value (AOV):** I calculated the average spend per order, strictly excluding shipping costs. This reflects the "clean" amount customers spend on products.

**2. High-Value Order Analysis:**

I identified orders that contribute the most to the company's revenue.

- **The logic:** I flagged all orders exceeding 600 UAH using a helper column.

- **Result:** I calculated the percentage of these high-value orders compared to the daily total.

- **Business impact:** This helps the marketing team evaluate if bundles or "buy more" promotions are successfully increasing the basket size.
