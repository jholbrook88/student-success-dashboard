# Student Academic Outcomes Dashboard

An Excel dashboard analyzing 1,000 student records to explore how test preparation, lunch type, parental education, and subject-level performance relate to academic outcomes.

![Student Academic Outcomes Dashboard](images/dashboard-preview.png)

## Project highlights

| KPI | Result |
|---|---:|
| Students analyzed | 1,000 |
| Overall average score | 67.8 |
| Pass rate | 71.5% |
| At-risk students | 285 |
| High performers | 198 |

## Key findings

- Students who completed test preparation averaged **72.7**, compared with **65.0** for students who did not—a **7.7-point difference**.
- Students receiving standard lunch averaged **70.8**, compared with **62.2** for students receiving free/reduced lunch.
- Pass rates were highest for students whose parents held a master's degree (**83.1%**) or bachelor's degree (**82.2%**).
- Reading had the highest subject average (**69.2**), followed by writing (**68.1**) and math (**66.1**).
- The performance-band distribution was **28.5% At Risk**, **51.7% Meets Standard**, and **19.8% High**.

These results describe associations in this dataset and should not be interpreted as causal effects.

## Workbook design

The workbook contains four worksheets:

| Worksheet | Purpose |
|---|---|
| `StudentsPerformance` | Source data converted to an Excel table, plus calculated helper columns |
| `Analysis` | PivotTable summaries used by the dashboard |
| `Dashboard` | KPI cards and five charts presenting the main results |
| `README` | In-workbook project notes and definitions |

### Calculated fields

- **Average Score:** mean of math, reading, and writing scores
- **Pass Flag:** `1` when Average Score is at least 60; otherwise `0`
- **Outcome:** `Pass` or `At Risk` based on the 60-point threshold
- **Performance Band:** `High` (80+), `Meets Standard` (60–79.9), or `At Risk` (below 60)
- **Score Gap:** difference between a student's highest and lowest subject score

## Tools and techniques

- Microsoft Excel
- Excel Tables and structured-reference formulas
- PivotTables and PivotCharts
- KPI calculations and dashboard layout
- Data validation and outcome segmentation

## Repository contents

```text
.
├── Student_Academic_Outcomes_Dashboard.xlsx
├── data/
│   └── StudentsPerformance.csv
├── images/
│   └── dashboard-preview.png
├── .gitattributes
├── .gitignore
└── README.md
```

The original `archive.zip` is intentionally omitted because it contains only a duplicate copy of `StudentsPerformance.csv`.

## How to explore the project

1. Download `Student_Academic_Outcomes_Dashboard.xlsx`.
2. Open it in Microsoft Excel for the best PivotTable and chart compatibility.
3. Start with the `Dashboard` worksheet, then review `Analysis` and `StudentsPerformance` to trace the calculations.

## Data notes

- The source data includes gender, race/ethnicity, parental education, lunch type, test-preparation status, and math, reading, and writing scores.
- The supplied files did not include a canonical source URL or redistribution license. Confirm the original dataset's attribution and license before making this repository public.
- No student names or direct personal identifiers are included in the dataset.

## Quality checks

- Confirmed 1,000 source records and eight raw fields.
- Confirmed all four worksheets, three Excel tables, five dashboard charts, and calculated outcome fields.
- Scanned worksheet XML for common formula errors (`#REF!`, `#DIV/0!`, `#VALUE!`, `#NAME?`, and `#N/A`); none were found.

