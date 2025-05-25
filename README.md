# UPI# Transactions

🔗 **Dashboard Link**: [Power BI Report](https://app.powerbi.com/groups/me/reports/c51cc664-17a3-44bf-99ca-d564b5385667?ctid=9e6079e4-4795-4aee-8ad0-1f1dce549bc5&pbi_source=linkShare>

---

## 🧩 Problem Statement

This dashboard is designed to help analyze **UPI (Unified Payments Interface)** transaction trends and patterns across various parameters like:

- Location
- Customer type
- Bank involvement
- Time period
- Transaction status

**Objectives**:
- Monitor overall UPI transaction volume and value.
- Identify peak hours and delay patterns.
- Compare success vs. failure rates.
- Detect bank-wise or region-wise service gaps.
- Understand user segments and their behavior.

---

## 🔧 Steps Followed

1. **Data Import**: Loaded the UPI transaction `.csv` file into Power BI.
2. **Data Profiling**: Used Power Query features:
   - Column Distribution
   - Column Quality
   - Column Profile
3. **Null/Error Handling**:
   - Fields like `Transaction Status`, `Transaction Time` were checked and handled.
4. **Slicers Added**:
   - Bank Name, Transaction Type, Customer Region, Date, Transaction Status.
5. **Card Visuals Created**:
   - Total Transactions
   - Total Value
   - Success Rate
   - Failed Transaction Count
6. **Line & Column Charts**:
   - Transactions Over Time
   - Success vs. Failure Trends
7. **Matrix Visual**:
   - Bank-wise transaction performance.
8. **DAX Measures Created**:
   - Success Percentage
   - Average Transaction Value
   - Failure Trends
9. **Customer Segmentation**:
   - First-time vs. Returning users
10. **Publishing**:
    - Report deployed to Power BI Service.

---

## 🧮 DAX Measures Used

```DAX
Total Transactions = COUNT(upi_data[Transaction ID])

Total Value = SUM(upi_data[Amount])

Success Rate = DIVIDE([Success Count], [Total Transactions]) * 100

Average Transaction Value = AVERAGE(upi_data[Amount])
