# Bookstore Sales Analysis

## Project Overview

Built an Excel sales analytics dashboard for an online bookstore using formulas, Pivot Tables, XLOOKUP, SUMIFS, and business KPI analysis.

Analyzed sales performance, publisher profitability, customer behavior, shipping costs, and marketing campaign efficiency.

Created dashboard with KPI cards, Pareto analysis, revenue trends, and promo campaign profitability insights.

## What I did (Step-by-Step)

### Sales Data Tab

I cleaned and improved the raw data to make it reliable for analysis.

- I recalculated the revenue in the `Net Revenue Cleaned` column to fix errors in the original file.

- I integrated shipping costs and carrier information from reference tables. This allows the business to see the total cost of every sale, including delivery.

- I extracted the `Order Date` and calculated `Lead Time (hours)`. This shows how much time the warehouse needs to process an order.

- I added `COGS` for calculate the real profit for every transaction.

### Publisher Analysis Tab

In this tab, I analyzed the performance of different publishers.

**1. Key Metrics Calculated:**

- I extracted total sales after discounts by publisher (Net Revenue). This shows the scale of the business.

- I calculated profit after paying for the products (Gross Margin).

- I calculated profitability of each publisher (Margin %). It helps identify which partners are the most profitable.

**2. Pareto Analysis (80/20 Rule):**

I used the Pareto principle to find the most important publishers.

I sorted publishers by Net Revenue and calculated the cumulative percentage. I discovered that only **12% of publishers generate 80% of the total revenue**. This means the business is highly dependent on a small group of top partners.

**3. Negative Margin Alerts:**

I found cases where the margin was negative.
This happened when discounts were too high or the purchase price was higher than the selling price.

### Customer Insights Tab

In this tab, I identified orders that contribute the most to the company's revenue.

I flagged all orders exceeding 600 UAH using a helper column. I calculated the percentage of these high-value orders compared to the daily total. This helps the marketing team evaluate if bundles or "buy more" promotions are successfully increasing the basket size.

### Promo Efficiency Tab

In this section, I analyzed how different marketing activities affect the company's bottom line.
