# Superstore Profitability Analysis

## Project Overview
This project analyzes sales data from a retail "Superstore" to identify weak areas in the profit chain. The goal is to determine the root causes of negative profitability and provide recommendations.

** Question:** Which strategies, products, and regions are draining the company's profits?

## Tools & Technologies
* **Language:** Python (Pandas, Matplotlib, Seaborn)
* **Environment:** Jupyter Notebook
* **Techniques:** Data Cleaning, Exploratory Data Analysis (EDA), Geospatial Analysis, Correlation Matrix.

## Key Insights

### 1. The Discount Trap
My analysis revealed a negative correlation between Discount and Profit.
Crucially, the discounting strategy is flawed:
* **Irrational Pricing:** Discounts of **70-80%** are frequently applied to orders with a **Quantity of 1**.
* There is no "bulk buy" logic; high discounts are given regardless of order size, destroying margins.

![Quantity Analysis](discount_items.png)

### 2. Geographic Anomaly: The "Texas Binders" Problem
While **Texas** is the worst-performing state overall, the source of the loss was unexpected.
* Unlike the rest of the country where Furniture is the main issue, in Texas, **Binders** (Office Supplies) are the #1 source of loss (**-$14,705**).
* This suggests a specific pricing error or logistics issue for office supplies in this region.

![Texas Losses](texas_5subcategories.png)

### 3. The 20% Threshold
There is a clear "break-even" point for discounts. Transactions with discounts **greater than 20%** consistently result in financial losses. The **Furniture** category is particularly affected by this aggressive pricing.

![Discount Analysis](discount_profitability.png)

### 4. Geographic Overview
Losses are concentrated in specific states like Texas, Ohio, and Pennsylvania, requiring targeted intervention.

![States Loss](states_loss.png)

## Recommendations
Based on the data, I recommend the following actions to restore profitability:

1.  **Eliminate Single-Item Discounts:** Configure the POS system to restrict high discounts (>20%) to bulk orders (Quantity > 5) only.
2.  **Audit Texas Pricing:** Immediately investigate the pricing model for **Binders in Texas**. The -$14k loss indicates items are being sold below cost.
3.  **Stop Furniture Promotions:** Tables and Bookcases should be excluded from marketing promotions due to negative margins.
