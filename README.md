# Dynamic Healthcare Operational Analysis Dashboard & Automated Reporting

---

## Problem Statement

The objective of this project was to analyze hospital operational and patient management data to identify patient risk patterns, hospitalization trends, ICU workload, operational bottlenecks, and patient-flow challenges. The analysis helps understand how hospital resources are utilized and where operational improvements can be made through data-driven decision-making.

---

## Business Objective

The objective of this analysis is to understand hospital operations and improve healthcare service efficiency using analytical insights. The focus areas include:

- Identifying high-risk patient groups
- Understanding ICU workload and prolonged hospitalization patterns
- Monitoring patient wait-time pressure
- Analyzing hospitalization duration trends
- Evaluating department-level performance
- Understanding ward-level patient distribution
- Supporting healthcare decision-making through dynamic reporting

---

## Dashboard Overview

The dashboard was designed as an interactive healthcare analytics solution focused on patient admissions, risk analysis, hospitalization trends, operational performance, and patient satisfaction.

### Dashboard Components

### KPI Monitoring

- Total Patients
- Average Wait Time
- Average Satisfaction Score
- Admission Rate
- Wait-Time Variability
- Expected Admissions

### Dashboard Analysis Sections

- Monthly Admission Trend
- Department-wise Patient Distribution
- Gender Distribution
- Hospitalization Duration by Department
- Age Group Distribution
- Risk Category Distribution
- Length of Stay Distribution
- Ward Type Distribution
- Day-wise Admission Analysis
- Department Bottleneck Analysis
- Department Satisfaction Analysis
- Admitted Patients by Age Group

### Interactive Filters

- Year Filter
- Month Filter
- Age Group Filter

---

## Tools Used

- Microsoft Excel
- Power Query
- Pivot Tables
- Excel Formulas
- Interactive Dashboarding

---

## Dataset

### Dataset Size

- 9K+ Patient Records

### Dataset Includes

- Patient ID
- Admission Date
- Month & Year
- Day
- Blood Type
- Ward Type
- Payment Method
- Length of Stay
- Patient Gender
- Patient Age
- Age Group
- Department Referral
- Patient Satisfaction Score
- Patient Wait Time
- Risk Score
- Risk Category
- Admission Status

---

## Custom Features & Data Engineering

To make the analysis more meaningful, several custom fields were created using Excel formulas.

### Custom Columns Created

#### Risk Score & Risk Category

Created custom patient risk scoring logic and classified patients into:

- High Risk
- Medium Risk
- Low Risk

#### Age Group Segmentation

Created custom age groups for demographic analysis.

#### Length of Stay Segmentation

Created hospitalization categories:

- Short Stay
- Normal Stay
- Extended Stay
- Long Stay
- Critical Long Stay

#### Wait-Time Classification

Created wait-time categories for operational analysis.

#### Dynamic KPI Calculations

Built automated KPI calculations using Pivot Tables and Excel formulas.

---

## KPI Tracking

The dashboard tracks:

- Total Patients
- Average Wait Time
- Average Satisfaction Score
- Admission Rate
- Wait-Time Variability
- Expected Admissions
- Risk Distribution
- Ward Distribution
- Length of Stay Distribution

---

## Key Analysis Performed

- Monthly Admission Trend Analysis
- Department-wise Patient Distribution Analysis
- Age Group Analysis
- Risk Category Analysis
- ICU Patient Severity Analysis
- Length of Stay Analysis
- Extended Stay & Critical Long-Stay Analysis
- Ward-wise Patient Distribution Analysis
- High Wait-Time Patient Analysis
- Department Bottleneck Analysis
- Patient Satisfaction Analysis
- Gender Distribution Analysis
- Blood Group Analysis

---

## Dashboard Automation Features

- Dynamic Pivot Tables
- Interactive Slicers
- Automated Reporting using Power Query
- Refreshable KPI Dashboard
- Year, Month, and Age Group Filters
- Formula-Based Category Creation

---

## Dynamic Reporting Workflow

1. Raw patient data is updated in the source sheet
2. Power Query refreshes transformed data
3. Pivot Tables update automatically
4. KPI calculations refresh dynamically
5. Dashboard visuals update instantly
6. Slicers enable interactive analysis

---

# Key Insights

## Admission Trend Insights

- Patient admissions increase steadily from March to August.
- August records the highest patient volume.
- Admissions gradually decline towards the end of the year.
- Hospital workload fluctuates throughout the year, indicating seasonal admission patterns.

---

## Risk Analysis Insights

- High-risk patients are predominantly concentrated in the 60–80 age group.
- Low-risk patients are primarily observed between the 20–40 age range.
- Risk severity increases with patient age.
- ICU patients have a higher average risk score compared to other wards.
- Approximately 35% of ICU patients belong to the High-Risk category.
- Blood group B+ shows the highest concentration of High-Risk patients.
- ICU admissions are also dominated by B+ blood group patients.
- High-risk patients generally experience longer hospitalization durations.

---

## ICU & Critical Care Insights

- ICU patients represent only 10% of total admissions.
- ICU patients record an average hospitalization duration of 10 days.
- Approximately 66% of ICU patients belong to the Extended Stay category.
- ICU records the highest concentration of Extended Stay patients.
- Short-stay admissions are minimal in ICU.
- ICU handles fewer patients but significantly higher clinical severity.
- Approximately 35% of ICU patients belong to the High-Risk category.

---

## Wait-Time Insights

- General Ward records the highest number of high wait-time cases (1,975 patients).
- ICU contributes comparatively fewer high wait-time cases (371 patients).
- High wait-time cases are concentrated primarily in General Ward operations.
- Operational delays are more visible in high-volume wards than in critical-care wards.

---

## Length of Stay Insights

- Most patients fall under the Normal Stay category.
- Extended Stay patients form the second-largest hospitalization segment.
- Critical Long-Stay patients remain limited in count but require significant hospital resources.
- ICU contributes disproportionately to prolonged hospitalization cases.
- A relatively small group of patients accounts for a large share of hospital occupancy.

---

## Ward-Level Insights

### General Ward

- Handles the largest patient population.
- Records the highest operational workload.
- Manages the largest share of Normal Stay patients.
- Also records the highest number of high wait-time cases.

### ICU

- Handles fewer patients but significantly higher risk intensity.
- Records the highest concentration of Extended Stay patients.
- Contributes heavily to prolonged hospitalization burden.

### Private Ward

- Shows a relatively balanced stay distribution.
- Faces lower prolonged-care pressure compared to ICU.

---

## Department-Level Insights

- Patients without a specified referral department ("None") account for the highest concentration of Extended Stay and Critical Long-Stay cases.
- General Practice contributes significantly to prolonged hospitalization cases.
- Orthopedics demonstrates moderate long-duration recovery cycles.
- Cardiology records slightly longer treatment durations.
- Neurology shows relatively stable hospitalization distribution.
- Renal and Gastroenterology maintain lower hospitalization intensity.
- Gastroenterology records the highest patient satisfaction score.

---

## Satisfaction Insights

- Gastroenterology records the highest satisfaction score among all departments.
- Patient satisfaction remains relatively stable across departments.
- Higher patient volume does not necessarily result in lower satisfaction levels.

---

# Interconnected Insights

### Age and Risk Relationship

The analysis shows a clear relationship between age and patient risk. As patient age increases, the concentration of high-risk cases also increases. Senior patients contribute significantly to ICU admissions and longer hospital stays.

### ICU Burden Comes from Severity, Not Volume

Although ICU accounts for only 10% of total admissions, it contains a much higher proportion of High-Risk and Extended Stay patients. This indicates that ICU workload is driven by patient severity rather than admission volume.

### General Ward Faces the Largest Operational Pressure

General Ward handles the largest number of patients and records the highest number of high wait-time cases. This suggests that operational pressure is primarily driven by patient volume.

### Extended Stay Patients Consume More Resources

While most patients fall under Normal Stay, a relatively small group of Extended Stay and Critical Long-Stay patients contributes significantly to bed occupancy and resource utilization.

### Referral Process May Need Attention

Patients with no specified referral department show the highest concentration of Extended Stay and Critical Long-Stay cases. This may indicate referral-management inefficiencies or data-quality issues.

---

# Business Recommendations

## 1. Improve ICU Resource Planning

- Monitor Extended Stay patients more closely
- Improve ICU bed allocation planning
- Track prolonged-care cases proactively

**Reason:** ICU patients stay longer and consume a larger share of hospital resources.

---

## 2. Reduce General Ward Congestion

- Improve patient-flow management
- Optimize staffing during busy periods
- Reduce operational delays in high-volume wards

**Reason:** General Ward experiences the highest patient volume and wait-time burden.

---

## 3. Focus on Senior High-Risk Patients

- Introduce early-risk identification programs
- Monitor elderly patients more proactively
- Prioritize preventive healthcare measures

**Reason:** Senior patients contribute heavily to ICU demand and prolonged hospitalization.

---

## 4. Improve Extended Stay Management

- Track prolonged-stay patients regularly
- Strengthen discharge planning
- Monitor long-duration occupancy trends

**Reason:** A small number of patients occupy hospital resources for extended periods.

---

## 5. Strengthen Referral Tracking

- Improve referral documentation
- Reduce unspecified referral classifications
- Standardize patient-routing processes

**Reason:** Unspecified referrals show the highest concentration of prolonged hospitalization cases.

---

## Dashboard Highlights

- Built a fully interactive Healthcare Operational Analysis Dashboard in Excel.
- Created custom Risk Score, Risk Category, Age Group, and Length of Stay segmentation logic.
- Automated reporting using Power Query and dynamic Pivot Tables.
- Designed KPI monitoring for patient admissions, satisfaction, and operational performance.
- Developed interactive filtering using slicers.
- Built a refreshable dashboard that updates automatically when new data is added.

---

## Project Outcome

This dashboard helps identify:

- High-risk patient groups
- ICU workload patterns
- Extended Stay dependency
- Wait-time bottlenecks
- Department performance
- Hospitalization trends
- Patient satisfaction performance

The dashboard provides a centralized view of hospital operations and supports data-driven healthcare decision-making.

---

## Executive Summary

The analysis shows that hospital operations face two major challenges: managing high patient volume in the General Ward and handling prolonged-care cases in the ICU. While General Ward experiences the highest operational workload and wait-time pressure, ICU patients require significantly more care due to higher risk levels and longer hospital stays.

The findings highlight opportunities to improve patient-flow management, ICU resource planning, referral tracking, and monitoring of high-risk patient groups to enhance overall hospital efficiency.
