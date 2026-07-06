# hr-analytics-powerbi-dashboard
Power BI HR analytics dashboard analyzing 3,000+ US employee records: performance, attrition, compensation, satisfaction, and workforce demographics.

**Date:** 15th April, 2026  
**Tool:** Power BI (Power Query + DAX + Data Modeling)  
**Author:** Reyad Aly  
**Dataset:** HR Dataset (attached to the repo)


## Dashboard Highlights

### KPI Cards
- Total number of employees
- Number of female employees
- Average new pay rate
- Average active employee age

### Visuals
- Active employees gauge
- Performance score distribution (%)
- Employee satisfaction score breakdown
- Termination reasons by non-active employees
- Active employees by gender and position (Decomposition Tree)
- Top 3 shortest average working period positions
- State distribution of employees (%)
- Top 5 positions by average satisfaction score
- Employees by recruitment source
- Top 5 active employees by total bonus commissions
- Average bonus commissions by month (Area chart)
- Active employees by department
- Active employees by manager
- Average satisfaction score by department
- Top 5 managers by total commissions

<img width="1239" height="698" alt="Screenshot 2026-07-06 060343" src="https://github.com/user-attachments/assets/3dccef4c-9c58-47d5-af36-0f7b6e57860a" />
<img width="1237" height="695" alt="Screenshot 2026-07-06 060403" src="https://github.com/user-attachments/assets/93a16f7f-c1b3-4033-8ba9-f30d3148d0da" />
<img width="1234" height="687" alt="Screenshot 2026-07-06 060441" src="https://github.com/user-attachments/assets/34c17a10-f65a-4142-9868-7723184ecca8" />
<img width="1239" height="700" alt="Screenshot 2026-07-06 060458" src="https://github.com/user-attachments/assets/f97e96c0-b625-4735-a112-8f83cbd3a30f" />


## Data Modeling
- **9 tables** connected via relationships
- Main fact table: **HR data Set**
- Dimension tables: Gender Status, Marital Status, Position, Department, Manager, Manager Updated, Active Hiring Months, Bonus Commissions Months, US States Codes

<img width="1418" height="701" alt="Screenshot 2026-07-06 060540" src="https://github.com/user-attachments/assets/33d4ce0f-48b8-417f-acc6-0eda755d03ad" />


## Data Cleaning Steps (Power Query)
- Promoted headers and changed data types
- Removed blank rows and duplicates
- Trimmed and cleaned text columns
- Filtered rows to separate active and terminated employees
- Unpivoted columns for data restructuring
- Renamed and reordered columns for clarity
- Capitalized each word for name standardization
- Replaced incorrect position ID values
- Added conditional columns and custom columns
- Applied multiple type changes across all tables etc.

<img width="1918" height="789" alt="Screenshot 2026-07-06 060830" src="https://github.com/user-attachments/assets/712c3ac9-66b8-4adf-ae56-7c0fc2364662" />


## DAX Measures
- **Avg Terminated Tenure** — AVERAGEX with CALCULATETABLE filtering terminated employees, DATEDIFF between hire and termination dates in months
- **Active Hiring Months** — FILTER + SUMMARIZE for active employees only
- **Active Employee Number**
- **Avg Active Months**
- **Avg Active Age**
- **Avg Pay Rate**
- **Gender Female count**
- **Total Commission (Active)** etc.
<img width="1863" height="779" alt="Screenshot 2026-07-06 060657" src="https://github.com/user-attachments/assets/3bf93a24-affb-4ecb-8206-a40b92082d03" />
<img width="1863" height="781" alt="Screenshot 2026-07-06 060620" src="https://github.com/user-attachments/assets/0b772572-16d6-4fe1-af5e-fe852aa6ce2c" />


## Files Included
| File | Description |
|---|---|
| `hr_dataset_dashboard_RA.pbix` | Main Power BI dashboard file |
| `hr_dataset.zip` | Dataset files (CSV, PDF, TXT etc.) — extract before use |
| `HR_Dataset_Recommendation_Letter.doc` | Dashboard report and recommendation |


## License
MIT License
