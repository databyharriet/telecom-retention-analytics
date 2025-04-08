# 📊 Telecom Customer Retention Intelligence Analytics

![Power BI Project](https://img.shields.io/badge/Project-Power%20BI%20Dashboard-yellow)
![Power Query](https://img.shields.io/badge/Used-Power%20Query-green)
![DAX Magic](https://img.shields.io/badge/Tool-DAX-blueviolet)
![Interactive](https://img.shields.io/badge/Feature-Interactive%20Report-orange)

---

## 🚀 Project Overview

This project simulates a real-world case study for **PhoneNow**, a telecom provider, focused on **customer churn analysis** and **retention strategy** using **Power BI**. The goal is to visualize patterns, identify high-risk customers, and support proactive retention decisions.

This project was completed as part of a professional upskilling challenge provided by **PwC Switzerland** to help learners develop strong, real-world analytics capabilities. 🙌

---

## 🎯 Objective

Customers are the heart of telecom businesses, and losing them can be costly. This dashboard was designed to:

- Detect early signals of churn
- Identify at-risk segments like short-tenure users or senior citizens
- Reveal service and contract types most correlated with churn
- Empower decision-makers with actionable visual insights

---

## 🧠 Skills Demonstrated

✅ Power BI Dashboard Design  
✅ Power Query – Data Cleaning  
✅ DAX – KPI and Measure Calculation  
✅ Analytical Storytelling  
✅ Business-Driven Insights  

---

## 🛠️ Tools & Technologies

- **Power BI Desktop**
- **Power Query (ETL)**
- **DAX (Data Analysis Expressions)**
- **Excel** (for raw dataset)
- **PDF** (for brief/project brief understanding)

---

## 🧹 Data Cleaning Summary

Using Power Query, I:
- Corrected data types and handled blanks
- Removed duplicates
- Created calculated columns: `ChurnFlag`, `RiskCategory`, `TenureGroup`
- Formatted data for Power BI visuals

---

## 📊 Key DAX Measures

```DAX
TotalCustomers = DISTINCTCOUNT('01 Churn-Dataset'[CustomerID])

ChurnRate = DIVIDE(SUM('01 Churn-Dataset'[Churn Flag]), COUNT('01 Churn-Dataset'[CustomerID])) * 100

RevenueLoss = SUMX(
    FILTER('01 Churn-Dataset', '01 Churn-Dataset'[Churn Flag] = 1),
    '01 Churn-Dataset'[MonthlyCharges]
)

RetentionRate = 100 - [ChurnRate]

HighRiskCustomers = 
CALCULATE(
    COUNTROWS('01 Churn-Dataset'),
    '01 Churn-Dataset'[RiskCategory] = "High Risk"
)
```

---

## 📈 Dashboard Walkthrough

### 🔹 Page 1 – Executive Summary
- KPI cards for Total Customers, Churn Rate, Monthly Revenue Loss
- Churn by Contract, Internet Services, Payment Methods
- Monthly trend line
<img width="587" alt="Screenshot 2025-04-08 2222" src="https://github.com/user-attachments/assets/cd04d87d-816a-4bd5-a1e3-da4aa4724f00" />

### 🔹 Page 2 – Demographics & Behavior
- Churn patterns by Senior Citizen, Partner, Dependent
- Internet and support services usage
<img width="589" alt="Screenshot 2025-04-08 3333" src="https://github.com/user-attachments/assets/62390e0c-e13b-4496-ab70-aa619a14a9b6" />

### 🔹 Page 3 – High-Risk Customer Focus
- Dynamic table of high-risk profiles
- Filters to slice by service and customer demographics
<img width="592" alt="Screenshot 2025-04-08 4444" src="https://github.com/user-attachments/assets/a810f8fe-6372-4981-a626-17b3b90f2df6" />

---

## 🔍 Insights & Recommendations

- **Month-to-month** customers churn more than others — consider loyalty incentives
- Customers without **tech support** are highly likely to leave
- **Short-tenure (≤ 6 months)** customers are most at risk — target them early
- Senior citizens show different patterns — tailor outreach accordingly

---

## 💡 What Should Change?

- Shift from **reactive retention** to **predictive retention** using insights like "RiskCategory"
- Integrate churn scores into CRM tools
- Enhance customer support and bundled services

---

## 📁 Project Files

- `📊 Customer Call Analysis.pbix` – Interactive Power BI report
- `📄 02 Churn-Dataset.xlsx` – Dataset used
- `📃 PhoneNow inputs.pdf` – Project brief

---

## 🙏 Acknowledgment

Big thanks to **PwC Switzerland** for designing this realistic telecom analytics task to boost practical learning. It sharpened my Power BI, data storytelling, and business decision-making skills. 💼📊

---

## 🔗 Let’s Connect!

📧 *jmercy306@gmail.com *  
🔗 [LinkedIn](https://www.linkedin.com/in/mercy-jacob/) 


---

⭐ **If you found this helpful, give it a star!**
```

---

Would you like me to save this into a `README.md` file for direct upload to your GitHub repo? Also, feel free to drop your LinkedIn/portfolio link and email if you'd like me to plug those in too!

