# HR Employee Attrition Analysis
Python · Pandas · Seaborn · Plotly · EDA · Google Colab

---

## Overview

HR teams rarely know which employees are at risk of leaving until it's too late. This project digs into 1,200 records to find which departments, salary bands, and satisfaction levels correlate most with exits — so retention efforts can be targeted rather than guesswork.

The analysis covers attrition patterns by department, salary, job satisfaction, and work-life balance across 5 departments.

**Tech stack:**
- Python (Pandas, NumPy) — data cleaning and preprocessing
- Seaborn & Matplotlib — statistical charts
- Plotly Express — interactive charts
- Google Colab — development environment

---

## How it works
```
Raw Dataset (1,200 records | 9 features)
        ↓
Python (Data Cleaning + Outlier Handling)
        ↓
EDA (Attrition + Department + Satisfaction Analysis)
        ↓
Visualizations (Bar Charts, Pie Charts, Box Plots)
        ↓
Business Insights & HR Recommendations
```

---

## Dataset

| Metric | Value |
|--------|-------|
| Total employees | 1,200 |
| Employees who left | 241 (20.1%) |
| Employees who stayed | 959 (79.9%) |
| Avg monthly salary | ₹67,003 |
| Avg tenure | 13 years |
| Max tenure | 40 years |
| Total features | 9 |
| Departments | 5 (Sales, IT, Finance, HR, Operations) |
| Performance levels | 4 (Low, Medium, High, Very High) |
| Work-life balance categories | 4 (Poor, Average, Good, Excellent) |

---

## Analysis

**Data cleaning**
- Missing values: median imputation for Age, mode imputation for categorical columns
- Outliers in Age and Years_at_Company detected using IQR method (Seaborn boxplot)
- Categorical columns standardized — Department, Job Satisfaction, Work-Life Balance
- Salary Band feature added via pd.qcut() — Low, Medium, High, Very High

**Exploratory analysis**
- Department-wise attrition rates across all 5 departments
- Job satisfaction level vs attrition count
- Salary distribution — employees who left vs. stayed
- Work-life balance category vs attrition breakdown
- Performance rating distribution across 1,200 employees

**Charts**
- Pie chart — overall attrition split (20.1% vs 79.9%)
- Bar charts — department salary averages, attrition counts, satisfaction vs attrition
- Box plots — age and tenure outlier detection

---

## Department attrition

| Department | Employees | Left | Attrition rate |
|------------|-----------|------|----------------|
| Finance | 183 | 41 | 22.4% — highest |
| Sales | 309 | 65 | 21.0% |
| IT | 372 | 76 | 20.4% |
| HR | 151 | 26 | 17.2% |
| Operations | 117 | 17 | 14.5% — lowest |

---

## Key findings

| Finding | Numbers | What it means |
|---------|---------|---------------|
| Overall attrition | 241/1,200 (20.1%) | 1 in 5 employees left |
| Highest-risk dept | Finance — 22.4% | Leads all departments by a margin |
| Salary paradox | Left: ₹67,703 / Stayed: ₹66,828 | Leavers earned ₹875 more on average |
| WLB anomaly | Good WLB — 23.2% attrition | Higher exit rate than "Poor" WLB group |
| Poor WLB retention | 16.7% attrition | Lowest attrition of any WLB category |
| Avg tenure | 13 years | Long-tenured workforce overall |
| Performance split | High (301) / Very High (303) / Medium (309) / Low (287) | Roughly even across all four tiers |

---

## File structure
```
HR-Employee-Attrition-Analysis/
├── hrdata.ipynb
├── HR_Employee_Attrition_Dataset.csv
└── README.md
```

---

## How to run

1. Open `hrdata.ipynb` in Google Colab or Jupyter
2. Upload `HR_Employee_Attrition_Dataset.csv` to your environment
3. Run all cells in order

---

## Conclusions

The headline number is 20.1%, but the more interesting patterns sit underneath it.

Employees who left were actually earning more than those who stayed — ₹875/month more on average. That takes salary off the table as the main driver. Finance leads all departments at 22.4% attrition, which is harder to explain given it's not the lowest-paid department.

The work-life balance result is the strangest finding. Employees who rated their WLB as "Good" left at 23.2% — a higher rate than those who rated it "Poor" (16.7%). It likely means something else is pushing exits in that group: growth opportunities, management quality, or role fit. WLB scores alone don't predict who stays.

Operations is the most stable department at 14.5%. Finance is the least. That gap is probably where any retention effort should start.
