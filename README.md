# Hospital Medical Record Analysis Dashboard | Excel

**Turning 11,500 hospital records into actionable healthcare insights through data analytics, statistical testing, and dashboard design.**

## Project Overview

**This project analyses 11,500 hospital medical records spanning 2018–2024 to explore disease distribution, patient outcomes, hospital resource utilization, risk profiles, treatment patterns, and annual case trends.**

Using Microsoft Excel, Power Query, and Power Pivot, I developed an interactive dashboard that transforms raw hospital data into meaningful insights for healthcare performance monitoring and evidence-informed decision-making.

The analysis focuses on five medical conditions: Chronic Obstructive Pulmonary Disease (COPD), diabetes complications, heart disease, kidney disease, and lung cancer.

The central finding is that the recorded caseload is relatively evenly distributed across the five conditions, while complications, readmissions, and deaths represent substantial outcome burdens requiring further investigation.

## Dashboard Preview

[Hospital Medical Record Analysis Dashboard]([images/hospital-dashboard.png](https://github.com/oloruntayobolade/Hospital-Medical-Record-Analysis/blob/main/Overview-Dashboard..png)

*Excel dashboard featuring KPI cards, PivotCharts, disease distribution, hospitalization days, treatment patterns, patient risk profiles, family history, and annual case trends.*

## Business and Healthcare Questions

This project was designed to answer the following questions:

- Which medical conditions account for the largest share of recorded cases?
- What proportions of cases involve death, complications, and readmissions?
- How many hospitalization days and medications are recorded across conditions?
- How are patients distributed across low-, medium-, and high-risk categories?
- How common are hypertension, asthma, and family history of disease?
- How are cases distributed across treatment types?
- How has the annual case volume changed from 2018 to 2024?
- Do the observed differences in disease, treatment, and annual case counts appear statistically significant?
- How can data quality checks improve confidence in dashboard reporting?

## Tools and Technologies

| Tool | Application |
|---|---|
| Microsoft Excel | Data analysis, calculations, KPI development, and dashboard creation |
| Power Query | Data cleaning, transformation, standardization, and validation |
| Power Pivot | Data modelling and centralized data management |
| PivotTables | Aggregation and summarization of hospital records |
| PivotCharts | Interactive visualization of healthcare indicators |
| Statistical analysis | Chi-square goodness-of-fit tests and confidence interval estimation |

## Data Preparation and Analytical Workflow

The project followed a structured data analytics workflow:

**1. Data cleaning and transformation**
- Imported the raw records into Power Query.
- Reviewed data types, missing values, duplicate records, and inconsistent category labels.
- Standardized field names, including `disease_type`, `treatment_type`, `hospitalization_days`, and `medication_count`.
- Extracted the year from date-related information for time-series analysis.

**2. Data modelling**
- Loaded the cleaned data into the Excel Data Model using Power Pivot.
- Used a centralized model as the source for dashboard KPIs, PivotTables, and PivotCharts.
- Maintained consistent aggregation across the dashboard.

**3. Exploratory data analysis**
- Summarized disease frequencies, outcomes, treatment categories, and risk classifications.
- Examined hospitalization days and medication counts across the five conditions.
- Evaluated annual case trends from 2018 through 2024.

**4. Statistical analysis**
- Applied chi-square goodness-of-fit tests to assess differences in disease distribution, treatment frequencies, and yearly case volumes.
- Examined the family-history distribution against an equal 50/50 split.
- Estimated uncertainty around the recorded death proportion.

**5. Dashboard development**
- Designed KPI cards for key healthcare indicators.
- Created column charts, a line chart, a doughnut chart, and a horizontal bar chart.
- Arranged the visuals into a single-page dashboard to support rapid interpretation of results.

**6. Data validation**
- Reconciled disease, survival, treatment, family-history, and annual case totals against the 11,500-record base.
- Checked whether dashboard percentages agreed with the underlying counts.
- Reviewed chart scales and highlighted fields requiring additional verification.

## Key Findings

### 1. Disease Distribution

| Medical condition | Cases | Share of records |
|---|---:|---:|
| Heart disease | 2,377 | 20.67% |
| Diabetes complications | 2,325 | 20.22% |
| Lung cancer | 2,311 | 20.10% |
| Kidney disease | 2,265 | 19.70% |
| COPD | 2,222 | 19.32% |
| **Total** | **11,500** | **100%** |

Heart disease recorded the highest case count, while COPD recorded the lowest. The difference between them was relatively small.

A chi-square goodness-of-fit test produced χ² = 6.08, with 4 degrees of freedom and p = 0.19. At the 5% significance level, the analysis did not find statistically significant evidence that the observed distribution differed from an equal distribution across the five categories.

### 2. Patient Outcomes

| Indicator | Recorded cases | Percentage |
|---|---:|---:|
| Deaths | 3,488 | 30.33% |
| Complications | 5,773 | 50.20% |
| Readmissions | 5,739 | 49.90% |
| Survived | 8,012 | 69.67% |

Complications and readmissions each accounted for approximately half of all records. The recorded death proportion was 30.33%.

These results identify important areas for further investigation, including factors associated with poor outcomes, patterns of readmission, and differences in outcomes by disease and risk category.

### 3. Hospital Resource Utilization

- **Total hospitalization days:** 338,468
- **Average hospitalization days per record:** Approximately 29.4
- **Total medications recorded:** 51,282
- **Average medication count per record:** Approximately 4.46

Lung cancer had the highest recorded medication count per case, at 4.62, while diabetes complications had the lowest, at 4.36.

The average hospitalization duration requires further validation to establish whether the source field represents length of stay per admission or another measure of hospitalization days.

### 4. Patient Risk and Coexisting Conditions

- Medium risk: 35%
- Low risk: 33%
- High risk: 32%
- Family history of disease: 50.02%
- Hypertension recorded: 49.44%
- Asthma recorded: 50.03%

Approximately 67% of records were classified as medium or high risk. Hypertension, asthma, and family history were also frequently recorded.

Further cross-tabulation would help determine whether these characteristics are associated with complications, deaths, or readmissions.

### 5. Treatment Patterns

| Treatment type | Cases | Share |
|---|---:|---:|
| Chemotherapy | 2,908 | 25.29% |
| Medication only | 2,879 | 25.03% |
| Surgery | 2,875 | 25.00% |
| Radiation | 2,838 | 24.68% |

Treatment counts were relatively evenly distributed. A chi-square goodness-of-fit test produced p = 0.83, providing no statistically significant evidence of a difference from an equal distribution.

However, the treatment categories should be checked against the underlying clinical definitions before drawing conclusions about treatment selection or appropriateness.

### 6. Annual Case Trends

Annual case volume peaked at **1,704 in 2019** and declined to **1,599 in 2024**, a decrease of approximately 6.16% from the peak.

A chi-square goodness-of-fit test for equal yearly volumes produced p = 0.24. The observed fluctuations were not statistically significant at the 5% level under this test.

## Recommendations from the Analysis

Based on the patterns observed, the following areas merit further investigation:

1. **Complication prevention:** Investigate clinical and demographic factors associated with the 50.20% recorded complication rate.
2. **Readmission monitoring:** Examine readmission patterns by disease, treatment, age, and other available patient characteristics.
3. **Outcome analysis:** Cross-tabulate deaths and complications by disease type and risk category to identify groups with poorer recorded outcomes.
4. **Medication review:** Investigate medication counts by condition and assess whether the recorded medication burden warrants clinical review.
5. **Length-of-stay validation:** Confirm the definition and calculation of hospitalization days before using the average for benchmarking or capacity planning.
6. **Data quality improvement:** Validate treatment definitions and risk classifications, and investigate possible inconsistencies between recorded diagnoses and treatments.

The priority is to move beyond overall counts and identify which patient groups and clinical factors are associated with different outcomes.

## Data Quality and Validation

Seven validation checks were documented in the accompanying report. These included:

- Reconciliation of disease counts to 11,500 records.
- Reconciliation of survival status to the full record count.
- Reconciliation of treatment categories.
- Reconciliation of family-history categories.
- Verification of annual totals across 2018–2024.
- Recalculation of dashboard percentages from underlying counts.
- Verification that the risk-category percentages sum to 100%.

All seven reported checks reconciled to the expected totals.

**Important:** These checks establish arithmetic consistency for the fields tested; they do not independently establish the clinical accuracy or completeness of the source data.

## Limitations

- The analysis is descriptive and does not establish causal relationships.
- The dataset's source, sampling method, and representativeness are not established in this report.
- Aggregate dashboard results do not reveal patient-level relationships between risk factors and outcomes.
- The recorded hospitalization duration and treatment classifications require additional validation.
- The similarity between complication and readmission counts does not establish that the same patients experienced both events.
- Further statistical analysis is needed before drawing conclusions about factors associated with mortality or complications.

## Skills Demonstrated

- Healthcare data analytics
- Data cleaning and transformation with Power Query
- Data modelling with Power Pivot
- Exploratory data analysis
- KPI development and dashboard design
- PivotTables and PivotCharts
- Statistical hypothesis testing
- Confidence interval estimation
- Data quality auditing and reconciliation
- Healthcare insight generation and analytical reporting

## Future Improvements

Potential next steps include:

- Building disease-by-outcome cross-tabulations.
- Analysing mortality and complications by risk category.
- Investigating readmission patterns and predictors.
- Validating hospitalization duration at the individual admission level.
- Developing a Power BI version of the dashboard.
- Exploring suitable regression models if the required patient-level variables and data quality are available.

## How to Use This Project

1. Clone or download this repository.
2. Open the Excel dashboard workbook in Microsoft Excel.
3. If the workbook includes the underlying data and queries, review the Power Query transformation steps and Power Pivot Data Model.
4. Explore the dashboard charts and KPI indicators.
5. Refer to the accompanying report for interpretation, validation checks, limitations, and recommendations.

## Conclusion

This project demonstrates how Microsoft Excel can be used beyond basic spreadsheet calculations to build a structured healthcare analytics workflow, from data preparation and modelling to statistical testing, visualization, and interpretation.
By analysing 11,500 medical records across seven years, I identified patterns in disease distribution, patient outcomes, resource utilization, risk profiles, and treatment categories while documenting data-quality limitations and opportunities for deeper investigation.

The project reflects my interest in **using data analytics to support healthcare research, public health decision-making, and evidence-informed improvements in patient care**.
---
**Author:** Bolade Oloruntayo  
**Focus Areas:** Healthcare Analytics | Public Health | Data Analysis | Research

*Note: This project is intended for analytical and educational purposes. The findings should not be interpreted as clinical recommendations or used as a substitute for patient-level clinical assessment.*
