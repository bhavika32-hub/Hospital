# Dynamic Healthcare Operational Analysis Dashboard & Automated Reporting

---

## Problem Statement

This project analyzes hospital operational and patient management data to identify patient risk patterns, hospitalization trends, ICU workload, operational bottlenecks, and patient-flow challenges — helping understand resource utilization and where operational improvements can be made through data-driven decision-making.

---

## Business Objective

Understand hospital operations and improve healthcare service efficiency using analytical insights. Focus areas:

- Identifying high-risk patient groups
- Understanding ICU workload and prolonged hospitalization patterns
- Monitoring patient wait-time pressure
- Analyzing hospitalization duration trends
- Evaluating department-level performance
- Understanding ward-level patient distribution
- Supporting healthcare decision-making through dynamic reporting

---

## Tools Used

Microsoft Excel · Power Query · Pivot Tables · Excel Formulas · Interactive Dashboarding

---

## Dataset

**Size:** 9K+ patient records

**Fields:** Patient ID, Admission Date, Month & Year, Day, Blood Type, Ward Type, Payment Method, Length of Stay, Gender, Age, Age Group, Department Referral, Satisfaction Score, Wait Time, Risk Score, Risk Category, Admission Status

---

## Data Cleaning & Transformation (Power Query)

- Removed duplicate records
- Corrected invalid/inconsistent date formats and converted text dates to proper date format
- Standardized Gender, Department, Ward Type, and Payment Method values
- Fixed inconsistencies across categorical fields
- Created Full Name (First + Last Name)
- Extracted Year, Month, and Day from Admission Date
- Validated and corrected formatting issues

---

## Custom Features & Data Engineering

Custom fields built using Excel formulas to make analysis more meaningful:

| Feature | Description |
|---|---|
| **Risk Score & Risk Category** | Custom scoring logic classifying patients as High / Medium / Low Risk |
| **Age Group Segmentation** | Custom age bands for demographic analysis |
| **Length of Stay Segmentation** | Short Stay, Normal Stay, Extended Stay, Long Stay, Critical Long Stay |
| **Wait-Time Classification** | Categorized wait times for operational analysis |
| **Dynamic KPI Calculations** | Automated via Pivot Tables and formulas |

**Descriptive statistics:** Mean, median, and mode applied to wait times and hospitalization duration; Age vs. Risk Score and Risk Score vs. Length-of-Stay trends analyzed to uncover risk patterns.

#### Core KPI Snapshot

| Metric | Value |
|---|---|
| Total Patients | 9,216 |
| Average Wait Time | 35 mins |
| Average Satisfaction Score | 1.36 / 10 |
| Admission Rate | 50% |

#### Wait Time — Descriptive Stats

| Statistic | Value |
|---|---|
| Mean | 35.26 |
| Median | 35 |
| Mode | 30 |
| Standard Deviation | 14.73 |
| Coefficient of Variation (CV) | 42% |

#### Length of Stay — Descriptive Stats

| Statistic | Value |
|---|---|
| Mean | 6.09 days |
| Median | 5 days |
| Mode | 5 days |
| Standard Deviation | 5.85 |
| Coefficient of Variation (CV) | 96% |

**Interpretation:** Wait Time has moderate variability (CV 42%) — most patients wait somewhat close to the average. Length of Stay has very high variability (CV 96%) — a small group of patients with much longer stays (Extended/Critical Long-Stay) is pulling the spread up, even though the median stay is only 5 days.

#### Correlation Analysis

| Relationship | Correlation Coefficient | Interpretation |
|---|---|---|
| Age vs. Risk Score | ~0.30 | Weak positive — risk tends to rise with age, but age alone doesn't fully explain risk |
| Risk Score vs. Length of Stay | ~0.31 | Weak positive — higher-risk patients tend to stay longer, though other factors also drive length of stay |

**Patient flow forecasting:** Next-month admissions forecasted using running-average analysis on historical trends, to support capacity planning and resource allocation.

---

## Automated Reporting Pipeline

An end-to-end, refreshable Excel pipeline with minimal manual intervention:

1. Raw patient data is ingested/updated in the source sheet
2. Power Query cleans and transforms the data automatically
3. Dynamic categories and calculated fields are generated
4. Pivot Tables refresh and update automatically
5. KPI calculations and dashboard visuals update instantly
6. Slicers enable interactive, on-demand analysis

---

## Dashboard Overview

An interactive healthcare analytics dashboard covering patient admissions, risk analysis, hospitalization trends, operational performance, and satisfaction.

### KPIs Tracked
Total Patients · Average Wait Time · Average Satisfaction Score · Admission Rate · Wait-Time Variability · Expected Admissions · Risk Distribution · Ward Distribution · Length of Stay Distribution

### Analysis Sections
Monthly Admission Trend · Department-wise Patient Distribution · Gender Distribution · Hospitalization Duration by Department · Age Group Distribution · Risk Category Distribution · Length of Stay Distribution · Ward Type Distribution · Day-wise Admission Analysis · Department Bottleneck Analysis · Department Satisfaction Analysis · Admitted Patients by Age Group

### Interactive Filters
Year · Month · Age Group (via slicers)

### Automation Features
Dynamic Pivot Tables · Interactive Slicers · Power Query–driven refresh · Formula-based category creation

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

# Key Insights

## Admission Trends
- Admissions rise steadily from March to August, peaking in August, then decline toward year-end — indicating seasonal patterns.

## Risk Patterns
- High-risk patients are concentrated in the 71–80 age group, followed by 61–70; risk severity increases with age.
- Low-risk patients are least represented in these older age groups.
- High-risk patients generally have longer hospitalization durations.

## ICU & Critical Care
- ICU accounts for only **10%** of total admissions but carries disproportionate severity:
  - ~**35%** of ICU patients are High Risk
  - Average ICU stay: **10 days**
  - ~**66%** of ICU patients fall in the Extended Stay category (short stays are minimal)
- ICU pressure is driven by patient **severity**, not volume.

## Blood Group Patterns
- **B+** has the highest patient volume overall and the largest share of High-Risk patients; it also dominates ICU admissions.
- **O+** is the second-highest across risk categories.
- Blood group distribution is otherwise fairly consistent across Low/Medium/High-Risk groups.

## Wait-Time Pressure
- General Ward has the most high-wait-time cases (**1,975**) vs. ICU's **371**.
- The "None" referral category and General Practice see the highest concentrations of high-wait-time patients.
- Medium-Risk patients contribute the most high-wait-time cases (**2,136**); High-Risk contributes **1,195**.
- **~87%** of High-Risk patients experience High Wait-Time; **~57%** of Medium-Risk patients do.

## Length of Stay
- Most patients fall under Normal Stay; Extended Stay is the second-largest segment.
- Critical Long-Stay patients are few but resource-intensive.
- **~50%** of High-Risk patients are Extended Stay, vs. only **~17%** of Medium-Risk (**~56%** of Medium-Risk are Normal Stay).
- A small patient group accounts for a disproportionate share of hospital occupancy.

## Ward-Level Patterns
- **General Ward:** Largest patient population and workload; highest number of Normal Stay patients and high-wait-time cases.
- **ICU:** Fewer patients but highest concentration of Extended Stay and prolonged hospitalization.
- **Private Ward:** Balanced stay distribution; lower prolonged-care pressure than ICU.

## Department-Level Patterns
- The "None" referral category has the highest concentration of High-Risk, Extended Stay, and Critical Long-Stay patients.
- General Practice ranks second in High-Risk concentration and contributes significantly to ICU admissions and prolonged stays.
- Orthopedics shows moderate long-duration recovery; Cardiology slightly longer treatment durations; Neurology is relatively stable.
- Renal and Gastroenterology have lower hospitalization intensity.
- **Gastroenterology has the highest patient satisfaction score**, and satisfaction stays fairly stable across departments — higher volume doesn't necessarily mean lower satisfaction.

---

# How These Patterns Connect

- **Age drives resource consumption:** The 61–80 age bracket dominates High/Medium-Risk categories and is more likely to need ICU care and longer stays.
- **High-Risk patients strain multiple fronts at once:** 50% land in Extended Stay and 87% in High Wait-Time — simultaneously affecting clinical workload, bed occupancy, and delays.
- **ICU burden comes from severity, not volume:** ICU accounts for only 10% of total admissions, yet 35% of ICU patients are High Risk, average ICU stay is 10 days, and 66% fall in Extended Stay — showing ICU pressure is driven by patient severity rather than patient count.
- **Referral gaps concentrate pressure:** The "None" referral category and General Practice repeatedly show up across High-Risk, ICU, Extended Stay, and High-Wait-Time cases — suggesting workload is concentrated in a narrow set of referral pathways rather than spread evenly.
- **Risk severity and length of stay move together:** As risk rises, so does hospitalization duration (50% of High-Risk vs. 17% of Medium-Risk in Extended Stay).

---

# Business Recommendations

## 1. Improve ICU Resource Planning
- Monitor Extended Stay patients more closely.
- Improve ICU bed allocation planning.
- Track prolonged-care cases proactively.

**Reason:** ICU patients stay longer and consume a larger share of hospital resources.

## 2. Reduce General Ward Congestion
- Improve patient-flow management.
- Optimize staffing during busy periods.
- Reduce operational delays in high-volume wards.

**Reason:** General Ward experiences the highest patient volume and wait-time burden.

## 3. Focus on Senior High-Risk Patients
- Introduce early-risk identification programs.
- Monitor elderly patients more proactively.
- Prioritize preventive healthcare measures.

**Reason:** Patients aged 61–80 contribute heavily to High-Risk cases, ICU admissions, and prolonged hospitalization.

## 4. Improve Extended Stay Management
- Track prolonged-stay patients regularly.
- Strengthen discharge planning.
- Monitor long-duration occupancy trends.

**Reason:** A small number of patients occupy hospital resources for extended periods.

## 5. Strengthen Referral Tracking
- Improve referral documentation.
- Reduce unspecified referral classifications.
- Standardize patient-routing processes.

**Reason:** The "None" referral category contributes heavily to High-Risk, High Wait-Time, and Extended Stay cases.

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

The dashboard provides a centralized, refreshable view of hospital operations, helping identify high-risk patient groups, ICU workload patterns, extended-stay dependency, wait-time bottlenecks, department performance, hospitalization trends, and satisfaction levels — supporting data-driven healthcare decisions.

---

## Executive Summary

Hospital operations face two core challenges: high patient volume in the General Ward, and prolonged, high-severity care in the ICU. General Ward drives the bulk of operational workload and wait-time pressure, while ICU — despite lower volume — demands significantly more resources due to higher patient risk and longer stays. Addressing patient-flow management, ICU capacity planning, referral tracking, and proactive monitoring of high-risk groups offers the clearest path to improving overall hospital efficiency.
