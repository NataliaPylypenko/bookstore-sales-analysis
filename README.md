# Bookstore Sales Analysis

## 📌 Project Overview

TI took a "messy" sales file and cleaned it. I added new columns to help the business understand their profits and how fast they work.

## 🛠 Tech Stack

- **Excel**: Advanced Formulas (`VLOOKUP`, `IFERROR`, `SUBSTITUTE`, `DATEVALUE`), Data Cleaning, and Pivot Tables.
- **Data Analysis Concepts**: Feature Engineering, KPI calculation, and Data Validation.

# Project: Sales Data Cleaning & Analysis

## 📌 What is this project about?

I took a "messy" sales file and cleaned it. I added new columns to help the business understand their profits and how fast they work.

## 🛠 What I did (Step-by-Step)

### 1. Sorted products from services

- **Column added:** `Item Category`
- **Why:** I separated real **Products** (books) from **Services** (delivery fees). This helps to see what we are actually selling.

### 2. Fixed the money data

- **Column added:** `Net Revenue Cleaned`
- **Why:** The old revenue numbers had mistakes. I used the formula `Price - Discount` to get the correct amount.

### 3. Tracked real profit

- **Column added:** `COGS` (Cost of Goods)
- **Why:** I used a formula to pull the price of each book from the warehouse data. We need this to see how much we actually spend on products.

### 4.

- **Column added:** `Shipping Cost (UAH)` (The money we pay for delivery.)
- **Why:** I created a complex formula to calculate shipping prices automatically. It helps to see how delivery costs affect our final profit.

- **Logistics Carrier**
  - **What it is:** The name of the delivery service (Nova Poshta or Ukrposhta).
  - **Why I added it:** I pulled this data from the shipping logs. Now we can compare which company is cheaper or more popular among customers.

### 3. Tracked real profit

- **Column added:** `COGS` (Cost of Goods)
- **Why:** I used a formula to pull the price of each book from the warehouse data. We need this to see how much we actually spend on products.

### 3. Automated the shipping costs

- **Columns added:** `Shipping Cost` and `Logistics Carrier`
- **Why:** I used a formula to automatically pull delivery prices for **Nova Poshta** and **Ukrposhta**. No more manual checking!

### 4. Calculated work speed

- **Columns added:** `Order Timestamp` and `Lead Time (Hours)`
- **Why:** I extracted the exact time of each order. Then, I calculated the hours between the "Order" and the "Invoice." This shows how fast the team processes orders.
