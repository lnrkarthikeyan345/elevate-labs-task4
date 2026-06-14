# 📊 Financial Sales Dashboard | Power BI
## 📌 Objective
Design an interactive multi-page dashboard for business stakeholders using real financial sales data, built in Power BI with KPIs, navigation, slicers and business insights.

---

## 📂 Dataset
- **Name:** Reliance Finance Sales Dataset
- **Source:** [Kaggle](https://www.kaggle.com/datasets/lovisho13/reliance-finance-sales-dataset)
- **Size:** 200 rows × 20 columns

---

## 🛠️ Tools Used
- Power BI Desktop
- Power Query (Data Cleaning)
- DAX (Calculated Measures)

---

## 📋 Dataset Columns
| Column | Description |
|--------|-------------|
| OrderID | Unique transaction ID |
| OrderDate | Date of transaction |
| ProductName | Name of financial product |
| Category | Investment or Others |
| SubCategory | Mutual Fund, Equity, Debt Fund, Others |
| Quantity | Units purchased |
| UnitPrice | Price per unit |
| TotalSales | Total transaction value |
| Gender | Customer gender |
| Age | Customer age |
| Region | City (Delhi, Mumbai, Chennai, Kolkata, Bangalore) |
| PaymentMode | UPI, Credit Card, Cheque, Net Banking |
| Channel | Online, Offline, Agent |
| TransactionStatus | Success, Failed, Pending |
| FeedbackScore | Customer rating (1-5) |

---

## 📊 Dashboard Structure
5 interactive pages with navigation menu:

| Page | Content |
|------|---------|
| Overview | KPI Cards, Monthly Sales Trend, Sales by Region, Payment Mode, Channel Split |
| Product Analysis | Sales by SubCategory, Product Treemap, Category Split |
| Regional Analysis | India Map, Orders by Region, Avg Feedback by Region |
| Payment & Channel | Orders by Payment Mode, Feedback by Channel, Payment Trend |
| Customer Analysis | Sales by Age Group, Gender vs Payment Mode, Sales by Sales Rep |

---

## 📈 KPIs Tracked
| KPI | Value |
|-----|-------|
| Total Sales | 2.8M |
| Total Orders | 200 |
| Avg Feedback Score | 3.05 / 5.0 |
| Success Rate | 31.5% |

---

## 🧮 DAX Measure Created
```dax
Success Rate % = 
DIVIDE(
    COUNTROWS(FILTER('Reliance_Finance_Sales_Dataset',
    'Reliance_Finance_Sales_Dataset'[TransactionStatus] = "Success")),
    COUNTROWS('Reliance_Finance_Sales_Dataset')
) * 100
```

---

## 🔍 Key Business Insights
1. **Delhi** is the top performing city in sales
2. **Sales declining** month over month from January to July — critical red flag
3. Only **31.5% transactions successful** — needs immediate investigation
4. **Age group 41-50** are the biggest spenders
5. **UPI and Credit Card** are almost equally popular payment methods
6. **Agent channel** drives the highest sales volume

---

## 📁 Repository Structure
```
elevate-labs-task4/
├── DATASET/
│   └── Reliance_Finance_Sales_Dataset.csv
├── PPT/
|   ├── report_summary.pptx
│   └── report_summary.pdf
├── REPORT/
│   ├── report.pbix
│   └── report.pdf
├── SCREENSHOT/
│   ├── overview.jpg
│   ├── product_analysis.jpg
│   ├── regional.jpg
│   ├── payment_and_channel.jpg
│   └── customer.jpg
└── README.md
```
---

## ✅ Result
A fully interactive 5-page Power BI dashboard with dark theme, navigation menu, dropdown slicers and actionable business insights from Reliance Finance sales data.

