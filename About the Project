# 📊 CRM Employee Dataset 2026

A cleaned and structured HR/CRM employee dataset covering 20 employees across 11 countries and 10 departments. Prepared for analytics, reporting, and data pipeline projects.

---

## 📁 Repository Structure

```
crm-dataset-2026/
├── README.md
├── CRM_2026_Cleaned.xlsx        # Main cleaned workbook (4 sheets)
└── data/
    └── CRM-DATASET_2026_Analysis_PIVOT_TABLES.xlsx  # Original source file
```

---

## 📋 Dataset Overview

| Property | Value |
|---|---|
| Total Employees | 20 |
| Departments | 10 |
| Countries | 11 |
| Salary Range (USD/mo) | $1,500 – $9,800 |
| Hire Period | 2018 – 2024 |
| Source Format | `.xlsx` |

---

## 🗂️ Workbook Sheets

### 1. `Employee Data`
The primary cleaned employee table with 16 columns.

| Column | Type | Notes |
|---|---|---|
| Employee ID | String | Unique identifier (E001–E020) |
| Full Name | String | |
| Email | String | ⚠️ Placeholder emails — see Data Quality section |
| Job Title | String | |
| Department | String | |
| Hire Date | Date | Format: DD-MMM-YYYY |
| Skills | String | Comma-separated list |
| Country | String | |
| Salary (USD/mo) | Number | Monthly salary in USD |
| Bonus Rate | Percentage | Decimal (e.g. 0.2 = 20%) |
| Experience (yrs) | Number | Years of experience |
| Status (Original) | String | Original field — inconsistently applied |
| Status (Corrected) | String | Derived from Job Title |
| Performance Score | Number | Internal KPI score |
| Total Compensation | Number | Annual total comp |
| Seniority Level | String | Individual Contributor / Junior / Manager / Lead / Director / VP |

---

### 2. `Department Summary`
Aggregated statistics per department, sorted by average salary descending.

| Column | Description |
|---|---|
| Department | Department name |
| # Employees | Headcount |
| Avg Salary (USD) | Average monthly salary |
| Min / Max Salary | Salary range |
| Avg Performance | Mean performance score |
| Avg Experience (yrs) | Mean years of experience |

---

### 3. `Skills Matrix`
Frequency table of all technical skills across the team.

| Column | Description |
|---|---|
| Skill | Technology or tool name |
| # Employees | Number of employees with this skill |
| % of Team | Share of total headcount |

**Top 5 skills:** DataBricks (12), Hadoop (8), R (7), Power BI (6), Java / SQL (6 each)

---

### 4. `Data Quality Log`
23 flagged data issues for review before production use. Categories:

| Issue Type | Count | Action Required |
|---|---|---|
| Status Mismatch | 6 | Status field corrected in `Employee Data`; originals preserved for audit |
| Placeholder Email | 19 | Replace all `*kamau@gmail.com` addresses with real emails |
| Zero Bonus | 1 | Confirm whether E008 (Fatima Ali, VP of Sales) intentionally receives no bonus |

---

## ⚠️ Known Data Quality Issues

Before using this dataset in production or analysis pipelines, address the following:

1. **Placeholder emails** — 19 of 20 email addresses follow the pattern `firstnamekamau@gmail.com` and are not real. Replace before any outreach or email integration.

2. **Status field inconsistency** — The original `Status` column (Junior/Senior) was applied incorrectly for 6 employees. The `Status (Corrected)` column has been derived from Job Titles. Both are preserved in the dataset.

3. **Typo in source file** — The original source file contains the column header `"Bonus Stutus"` (misspelling of "Bonus Status"). This has been corrected in the cleaned file.

4. **Mixed pivot/raw data in source** — The original `DataSet Table` sheet contained embedded pivot table fragments below the main data, inflating the apparent row count to 44. Only the 20 valid employee rows (E001–E020) are included in the cleaned file.

---

## 🌍 Country Coverage

| Region | Countries |
|---|---|
| East Africa | Kenya (6), Uganda (3) |
| West Africa | Nigeria (2), Ghana (1) |
| Southern Africa | Zimbabwe (1) |
| Middle East | UAE (2), Egypt (1) |
| Asia | China (1) |
| Europe | Spain (1), UK (1) |
| North America | USA (1) |

---

## 💡 Usage Notes

- All salary figures are in **USD per month**.
- Total Compensation is an **annual** figure.
- The Bonus Rate is a decimal multiplier (e.g. `0.18` = 18% of salary).
- Performance scores are internal KPI values and not normalized to a fixed scale.
- Skills are stored as comma-separated strings — parse with `str.split(',')` for analysis.

---

## 🛠️ Suggested Next Steps

- [ ] Replace placeholder email addresses
- [ ] Validate and reconcile the `Status` field with HR records
- [ ] Normalize the Skills column into a relational skills table
- [ ] Add a `Last Updated` timestamp column for change tracking
- [ ] Connect to a CRM or HRIS system for live data

---

## 📄 License

This dataset is for internal use only. Do not distribute externally without authorization.
