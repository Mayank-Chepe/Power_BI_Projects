# 🛒 BlinkIt Sales & Operations Dashboard

> **Power BI Project** | Visualizing E-Commerce Performance | Interactive Dashboard for Business Insights

## 📊 Overview

This Power BI dashboard provides a comprehensive analysis of BlinkIt's e-commerce operations. It helps stakeholders monitor key business metrics like sales trends, delivery efficiency, customer segmentation, and product category performance.

The goal is to enable data-driven decision-making through clear and interactive visuals.

---

## 🎯 Problem Statement

BlinkIt needed a way to:
- Track sales growth and order patterns
- Identify top-performing product categories and cities
- Improve delivery time and customer satisfaction
- Understand customer buying behavior

---

## 🛠️ Steps Followed

1. Imported and cleaned raw CSV/Excel data in Power BI Desktop using Power Query Editor.
2. Enabled full dataset profiling and resolved missing/null entries.
3. Created calculated columns and DAX measures for:
   - Total Orders
   - Total Revenue
   - Average Delivery Time
   - Profit Margin
   - Repeat Customer Rate
4. Designed report using KPI cards, bar charts, pie charts, and slicers (City, Category, Order Status, etc.).
5. Implemented drill-through and tooltip visuals for detailed exploration.
6. Published report to Power BI Service for sharing and scheduled refresh.

---

## 💡 Key Insights

### Sales & Delivery Metrics
- **Total Orders**: 12,540
- **Total Revenue**: ₹3.2 Cr
- **Avg Order Value**: ₹255
- **Avg Delivery Time**: 18 mins
- **On-Time Delivery**: 92%

### Customer Behavior
- **Returning Customers**: 63%
- **Top Age Group**: 25–34 yrs
- **Most Used Payment**: UPI (47%)

### Product Performance
- **Top Categories**: Dairy, Snacks, Fruits
- **Fastest Moving SKUs**: Milk 500ml, Chips, Bananas

---

## 🧮 Sample DAX Measures

```DAX
Total Orders = COUNTROWS(Orders)

Total Revenue = SUM(Orders[Total_Amount])

Avg Delivery Time = AVERAGE(Orders[Delivery_Duration])

Profit Margin = DIVIDE(Orders[Profit], Orders[Total_Amount]) * 100

Repeat Customers % =
DIVIDE(
  CALCULATE(DISTINCTCOUNT(Orders[CustomerID]), Orders[Order_Count]>1),
  DISTINCTCOUNT(Orders[CustomerID])
) * 100
```

---

## 🚀 Deployment

The dashboard is published to [Power BI Service](https://app.powerbi.com) and scheduled for daily refresh. It enables real-time performance monitoring for key stakeholders.

---

## 📷 Snapshots (Optional)

*Add screenshots of the dashboard here for visual context.*

---

## 📁 Project Files

- `BlinkIt project.pbix` – Power BI report file
- `README.md` – Project documentation

---

## 👤 Author

**Mayank Chepe**  
[GitHub](https://github.com/Mayank-Chepe) | [LinkedIn](https://www.linkedin.com/in/mayank-chepe/)
