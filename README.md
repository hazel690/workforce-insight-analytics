 📈 Workforce Insight – Attrition & Retention Analytics

An end-to-end HR analytics project spanning python,  Excel, and Power BI — from raw data generation to retention intelligence and visual dashboarding.

---

## 🎯 What It Does

Employee attrition is one of the costliest HR problems. This project builds a full analytics pipeline to:
1. Generate a realistic 10,000-employee workforce dataset
2. Enrich it with department salary benchmarks and retention priority flags
3. Analyze attrition patterns using pivot tables
4. Visualize key workforce insights in a Power BI dashboard

---

## 🛠️ Tools & Technologies

| Tool | Purpose |
|------|---------|
| Python (Pandas, Faker) | Dataset generation |
| Excel — AVERAGEIF | Department-level salary benchmarking |
| Excel — IF / AND | Retention priority classification logic |
| Excel — Pivot Tables | Attrition rate analysis by department |
| Power BI | Interactive workforce dashboard |

---

## 📊 Dataset

**10,000 employees** across 6 departments: IT, Sales, HR, Operations, Finance, Marketing

| Column | Description |
|--------|-------------|
| Employee_ID | Unique identifier |
| Name | Employee name |
| Gender | Male / Female / Non-Binary |
| Age | 22–60 years |
| Department | One of 6 departments |
| Job_Role | Role within department |
| Monthly_Income | ₹40,000 – ₹1,50,000 |
| Tenure_Years | 0–15 years |
| Performance_Rating | 1–5 scale |
| Training_Hours | 10–80 hours |
| Last_Promotion_Years | Years since last promotion |
| Attrition | Yes / No |

---

## ⚙️ Excel Enrichment Logic

Two additional columns were added in Excel using formulas:

### `AVG_SALARY_DEPT` — Department Salary Benchmark
```excel
=AVERAGEIF(E:E, E2, G:G)
```
Calculates the average monthly income for each employee's department dynamically. Used as a benchmark to identify underpaid employees.

---

### `Retention_Priority` — At-Risk Employee Flag
```excel
=IF(AND(H2=5, G2<M2), "High Priority", "Normal")
```
Flags an employee as **"High Priority"** if they are:
- A **top performer** (Performance Rating = 5), AND
- Earning **below their department average**

These are employees most likely to leave if not addressed — highest retention ROI.

---

## 📉 Key Finding — Attrition Pivot Analysis

Attrition rate by department (from Pivot Table):

| Department | Attrition Rate |
|------------|---------------|
| Finance | ~58.4% |
| HR | ~55.7% |
| IT | ~57.8% |
| Marketing | ~58.5% |
| Operations | ~57.9% |
| Sales | ~57.3% |
| **Overall** | **~57.6%** |

> Attrition is uniformly high across all departments (~57-58%), suggesting a systemic issue rather than a department-specific one — pointing to company-wide factors like compensation, growth opportunities, or culture.

---

## 📊 Power BI Dashboard

The `.pbix` dashboard visualizes:
- Overall attrition rate
- Department-wise workforce breakdown
- Salary distribution across roles and departments
- Performance rating distribution
- Retention priority employee count

---

## 📁 Files

```
├── Workforce_insight.xlsx    # Enriched dataset with formulas and pivot table
├── Workforce_insight.csv     # Clean flat data export
├── dashboard.pbix            # Power BI dashboard file
└── README.md
```

---

## 👤 Author

**Abhay Choudhary**
Aspiring People Analyst | HR Operations
[LinkedIn](https://www.linkedin.com/in/abhay-choudhary-6b642b3b6) • [GitHub](https://github.com/hazel690)
