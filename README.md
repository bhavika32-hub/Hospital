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

# 🔄 Data Cleaning & Transformation (Power Query)

Data cleaning and transformation were performed using Power Query to create a semi-automated reporting workflow.

### Cleaning Steps Performed

- Removed duplicate records.
- Corrected invalid and inconsistent date formats.
- Converted text-based dates into proper date format.
- Standardized Gender values.
- Standardized Department names.
- Standardized Ward Type values.
- Standardized Payment Method entries.
- Fixed inconsistencies across categorical fields.
- Created Full Name by combining First Name and Last Name.
- Extracted Year, Month, and Day from Admission Date.
- Validated and corrected formatting issues.

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

- High-risk patients are predominantly concentrated in the 71–80 age group, followed by the 61–70 age group.
- Low-risk patients are least represented in the 71–80 and 61–70 age groups.
- Risk severity increases with patient age.
- ICU patients have a higher average risk score compared to other wards.
- Approximately 35% of ICU patients belong to the High-Risk category.
- Blood group B+ shows the highest concentration of High-Risk patients.
- ICU admissions are also dominated by B+ blood group patients.
- High-risk patients generally experience longer hospitalization durations.

---

## Blood Group Insights

- B+ records the highest patient volume across all risk categories.
- B+ also contributes the largest share of High-Risk patients.
- O+ records the second-highest patient count across risk categories.
- Blood group distribution remains relatively consistent across Low, Medium, and High-Risk categories.

---

## ICU & Critical Care Insights

- ICU patients represent only 10% of total admissions.
- ICU patients record an average hospitalization duration of 10 days.
- Approximately 66% of ICU patients belong to the Extended Stay category.
- ICU records the highest concentration of Extended Stay patients.
- Short-stay admissions are minimal in ICU.
- ICU handles fewer patients but significantly higher clinical severity.

---

## Wait-Time Insights

- General Ward records the highest number of high wait-time cases (1,975 patients).
- ICU contributes comparatively fewer high wait-time cases (371 patients).
- Patients under the "None" referral category account for the highest number of High Wait-Time cases.
- General Practice records the second-highest concentration of High Wait-Time patients.
- Medium-Risk patients contribute the highest number of High Wait-Time cases (2,136 patients).
- High-Risk patients contribute 1,195 High Wait-Time cases.
- Approximately 87% of High-Risk patients fall into the High Wait-Time category.
- Approximately 57% of Medium-Risk patients fall into the High Wait-Time category.

---

## Length of Stay Insights

- Most patients fall under the Normal Stay category.
- Extended Stay patients form the second-largest hospitalization segment.
- Critical Long-Stay patients remain limited in count but require significant hospital resources.
- ICU contributes disproportionately to prolonged hospitalization cases.
- Approximately 50% of High-Risk patients belong to the Extended Stay category.
- Only 17% of Medium-Risk patients belong to the Extended Stay category.
- Around 56% of Medium-Risk patients fall under the Normal Stay category.
- A relatively small group of patients accounts for a large share of hospital occupancy.

---

## Ward-Level Insights

### General Ward

- Handles the largest patient population.
- Records the highest operational workload.
- Manages the largest share of Normal Stay patients.
- Also records the highest number of High Wait-Time cases.

### ICU

- Handles fewer patients but significantly higher risk intensity.
- Records the highest concentration of Extended Stay patients.
- Contributes heavily to prolonged hospitalization burden.

### Private Ward

- Shows a relatively balanced stay distribution.
- Faces lower prolonged-care pressure compared to ICU.

---

## Department-Level Insights

- Patients without a specified referral department ("None") account for the highest concentration of High-Risk patients.
- General Practice records the second-highest concentration of High-Risk patients.
- General Practice contributes significantly to ICU admissions.
- Patients without a referral department account for the highest concentration of Extended Stay and Critical Long-Stay cases.
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

### Age Drives Risk and Hospital Resource Consumption

Patients aged 71–80 and 61–70 dominate both High-Risk and Medium-Risk categories. These age groups are more likely to require ICU care, experience longer hospital stays, and consume more healthcare resources.

---

### High-Risk Patients Create Multiple Operational Challenges

High-Risk patients not only require more clinical attention but also stay longer in the hospital.

- 50% of High-Risk patients fall under Extended Stay.
- 87% of High-Risk patients fall under High Wait-Time.

This indicates that High-Risk patients contribute simultaneously to clinical workload, bed occupancy, and operational delays.

---

### ICU Burden Comes from Severity, Not Volume

Although ICU accounts for only 10% of total admissions, it contains a much higher concentration of High-Risk and Extended Stay patients.

- 35% of ICU patients are High Risk.
- Average ICU stay is 10 days.
- 66% of ICU patients belong to the Extended Stay category.

This shows that ICU pressure is driven by patient severity rather than patient volume.

---

### Operational Pressure Is Concentrated in Specific Referral Groups

Patients under the "None" referral category and General Practice consistently appear across:

- High-Risk cases
- ICU admissions
- Extended Stay patients
- High Wait-Time cases

This indicates that a large share of hospital workload is concentrated within a limited number of referral pathways.

---

### Extended Stay Is Strongly Linked to Risk Severity

Length-of-stay patterns show a clear relationship between patient risk and hospitalization duration.

- 50% of High-Risk patients belong to Extended Stay.
- Only 17% of Medium-Risk patients belong to Extended Stay.

As risk severity increases, hospitalization duration also increases significantly.

---

# Business Recommendations

## 1. Improve ICU Resource Planning

- Monitor Extended Stay patients more closely.
- Improve ICU bed allocation planning.
- Track prolonged-care cases proactively.

**Reason:** ICU patients stay longer and consume a larger share of hospital resources.

---

## 2. Reduce General Ward Congestion

- Improve patient-flow management.
- Optimize staffing during busy periods.
- Reduce operational delays in high-volume wards.

**Reason:** General Ward experiences the highest patient volume and wait-time burden.

---

## 3. Focus on Senior High-Risk Patients

- Introduce early-risk identification programs.
- Monitor elderly patients more proactively.
- Prioritize preventive healthcare measures.

**Reason:** Patients aged 61–80 contribute heavily to High-Risk cases, ICU admissions, and prolonged hospitalization.

---

## 4. Improve Extended Stay Management

- Track prolonged-stay patients regularly.
- Strengthen discharge planning.
- Monitor long-duration occupancy trends.

**Reason:** A small number of patients occupy hospital resources for extended periods.

---

## 5. Strengthen Referral Tracking

- Improve referral documentation.
- Reduce unspecified referral classifications.
- Standardize patient-routing processes.

**Reason:** The "None" referral category contributes heavily to High-Risk, High Wait-Time, and Extended Stay cases.

---

## 6. High-Risk Patient Fast-Track Monitoring

- Prioritize High-Risk patients during admission and assessment.
- Create dedicated monitoring workflows.
- Improve early intervention practices.

**Reason:** 87% of High-Risk patients experience High Wait-Time and 50% belong to Extended Stay.

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

The findings highlight opportunities to improve patient-flow management, ICU resource planning, referral tracking, and monitoring of high-risk patient groups to enhance overall hospital efficiency and healthcare delivery.
