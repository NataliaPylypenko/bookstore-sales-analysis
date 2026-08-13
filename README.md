# Bookstore Sales Analysis

## 1. Order to Cash (O2C)

- Етап 1. Order to Cash (O2C)

1. Чи всі замовлення мають Customer ID? - ✅
2. Чи всі Sales Orders мають Order Date? - ✅
3. Чи один Customer Order має лише один Customer ID? - ✅

У наборі даних кожне замовлення Customer Order Reference належить лише одному клієнту Customer ID. (pivot)

❌ Але

Один Invoice ID пов'язаний із декількома різними Customer ID.

4. Чи є дублікати Invoice ID? - ✅

Invoice ID повторюється кілька разів, тому що в одному замовленні кілька книг. Один рядок таблиці - це один товар у рахунку.

- Етап 2. Sales Order → Products

1. Чи всі товари мають SKU? - ✅
2. Чи немає від'ємної кількості? (Returns) - ✅
3. Чи правильно розрахована знижка?
   Net Revenue = Qty × Gross Price − Discount - ❌

   Diff Net Revenue отриманого в таблиці і розрахованого from -0.61 to 0.99

4. Які товари продаються найкраще? - ✅

   Top 3 in pivot

- Етап 3. Pricing & Promotions

1. Чи всі знижки мають Promo Code? - ❌
2. Чи є Promo Code, які не дали знижку? - ❌

Ситуація з PROMO досить складна. Багато невідповідностей.
Зробила перерахунок, враховуючи умови акцій, врахувала що частина товарів виключена з промо, тобто Promo Code не поширюється на всі позиції. (Tab Check_Promo)

Виявила аномальні комбінації полів, які потребують перевірки бізнес-логіки.

Можливі пояснення:

Помилка в даних або в системі розрахунку знижки.
Промокод мав діяти лише на певні товари, а цей товар до них не належав.
Можливо, Extra -7% означає саме додаткові 7% поверх іншої промоакції.

В реальних умовах спочатку перевірила б дані з першоджерелом, можливо дані зїхали при експорті чи розрахунках. Потім обговорила б з колегами систему розрахунку знижок.

В деяких рядках Discount є, але Promo Code відсутній. Можливо, певний клієнт автоматично отримує Х%.

!!!Надалі вважатиму шо система показує коректні знижки.

3. Which promotion generated the highest revenue?

- Етап 4. Availability / Inventory Check

Немає фактичних даних про кількість товару на складі.

- Етап 5. Fulfillment / Picking

Один Invoice ID KNIL-87132021 має 2 Fulfillment ID, всі інші 1:1. Можливо,одне замовлення виконувалося частинами.

- Етап 6. Shipping / Delivery

\*\*

## 1. Check Quality Data

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
