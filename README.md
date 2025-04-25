# Nova-Mart-Demand-Forecasting-Inventory-Optimization
A Case Study in Statistical Analysis, Regression Modeling & Forecasting with Excel

---

## Business Overview

**Nova Mart** operates a chain of retail stores across various regions in the U.S., offering a wide assortment of products including groceries, clothing, toys, electronics, and furniture. With customer preferences shifting due to seasonality, promotions, and economic trends, Nova Mart is committed to leveraging **data-driven strategies** to optimize operations and maximize customer satisfaction.

---

## Problem Statement

Nova Mart faces major operational challenges due to **demand variability** and **external market volatility**. Fluctuations in daily sales—driven by holidays, weather conditions, competitor pricing, and discount campaigns—lead to issues such as:

- Overstocks and stockouts
- Inefficient procurement and supply planning
- Missed sales opportunities or increased holding costs

Nova Mart needs a **robust forecasting and analytical system** to better predict product demand and improve inventory and promotional strategies.

---

## Project Objectives

- Analyze historical sales and operational data using **descriptive statistics**
- Understand the relationship between key business variables via **correlation and regression analysis**
- Apply forecasting techniques (including Naïve forecasting) to anticipate future demand
- Identify drivers of sales variability to support data-driven planning
- Demonstrate practical use of **Excel for end-to-end analysis and forecasting**

---

## Dataset Overview

| Column | Description |
|--------|-------------|
| `Date` | Daily transaction record |
| `Store ID` / `Product ID` | Unique identifiers for stores and products |
| `Category` | Product classification (e.g., Electronics, Clothing) |
| `Region` | Geographic region |
| `Inventory Level` | Opening inventory for the day |
| `Units Sold` | Quantity sold |
| `Price` | Selling price per unit |
| `Discount` | Applied discount value |
| `Competitor Price` | Price of comparable product in market |
| `Weather Condition` | Weather influence on demand |
| `Holiday/Promotion` | Binary indicators for events affecting sales |

---

## Descriptive Statistics Summary (Key Variables)

| Metric | Units Sold | Price | Discount | Competitor Price |
|--------|------------|-------|----------|------------------|
| Mean | 136.46 | 55.14 | 10.01 | 55.15 |
| Std. Deviation | 108.92 | 26.02 | 7.08 | 26.19 |
| Min - Max | 0 - 499 | 10 - 100 | 0 - 20 | 5.03 - 104.94 |
| Skewness | 0.91 | 0.00 | 0.00 | 0.00 |
| Kurtosis | 0.05 | -1.20 | -1.30 | -1.17 |

---

## Correlation Matrix

| Variables | Units Sold | Price | Discount | Competitor Price |
|-----------|------------|-------|----------|------------------|
| **Units Sold** | 1.00 | 0.001 | 0.003 | 0.001 |
| **Price** | - | 1.00 | 0.002 | 0.994 |
| **Discount** | - | - | 1.00 | 0.002 |
| **Competitor Price** | - | - | - | 1.00 |

**Insight**: Sales (Units Sold) have weak correlations with price, discount, and competitor pricing—suggesting other external or categorical variables might play stronger roles.

---

## Multiple Linear Regression Analysis

**Dependent Variable:** Units Sold  
**Independent Variables:** Price, Discount, Competitor Price

### Regression Results Summary:
- **R²:** 0.9999 (Very high explanatory power)
- **Standard Error:** 1169.26
- **Significant Predictor:** Discount (p-value < 0.00001)

| Predictor | Coefficient | P-value | Interpretation |
|-----------|-------------|---------|----------------|
| Price | 1.24 | 0.395 | Not statistically significant |
| Discount | 4.34 | < 0.001 ✅ | Strong positive effect on sales |
| Competitor Price | 0.45 | 0.760 | Not statistically significant |

**Insight**: Discount is the most impactful predictor of sales among the variables considered.

---

## Forecasting with Naïve Approach (Excel)

| Metric | Value |
|--------|--------|
| **Mean Squared Error (MSE)** | 2,079,918.45 |
| **Mean Absolute Error (MAE)** | 1,137.82 |
| **Mean Absolute Percentage Error (MAPE)** | 8% |
| **Forecast Accuracy** | 92% ✅ |

**Insight**: The Naïve model provides a reliable benchmark for short-term forecasting but may be enhanced by incorporating more advanced models in future iterations.

---

## Key Takeaways

- Excel can be used effectively for advanced analytics, including regression, correlation, and forecasting.
- Discounting was statistically proven to drive sales volumes in the dataset.
- A demand forecasting system can significantly improve procurement timing, inventory levels, and operational efficiency.
- This project demonstrates **practical business analytics skills** using **Excel without code**, making it highly transferable across business environments.

---

## What’s Included in the Repository

| File | Description |
|------|-------------|
| `nova_mart_cleaned_data.xlsx` | Cleaned and prepared dataset |
| `nova_mart_forecasting.xlsx` | Forecasting models and outputs |
| `README.md` | Project documentation (this file) |


