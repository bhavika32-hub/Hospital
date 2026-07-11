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

**Size:** 9,216 patient records

**Fields:** Patient ID, Admission Date, Month & Year, Day, Blood Type, Ward Type, Payment Method, Length of Stay, Gender, Age, Age Group, Department Referral, Satisfaction Score, Wait Time, Risk Score, Risk Category, Admission Status

---

## Data Cleaning & Transformation (Power Query)

- Removed duplicate records
- Corrected invalid/inconsistent date formats and converted text dates to proper date format
- Standardized Gender, Department, Ward Type, and Payment Method values — including replacing an unclassified "Nc" gender value (24 records, 0.26%) with a clear "Unknown" label
- Fixed inconsistencies across categorical fields
- Created Full Name (First + Last Name)
- Extracted Year, Month, and Day from Admission Date
- Validated and corrected formatting issues

**Known data quality note:** One record (Patient ID 674-03-7037) has a corrupted date value bleeding into the Month and Day fields; this row is excluded from monthly/day-wise trend charts.

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

**Descriptive statistics:** Mean, median, and mode applied to wait times and hospitalization duration; Age vs. Risk Score, Risk Score vs. Length-of-Stay, and Risk Score vs. Satisfaction trends analyzed to uncover risk patterns.

#### Core KPI Snapshot

| Metric | Value |
|---|---|
| Total Patients | 9,216 |
| Average Wait Time | 35 mins |
| Average Satisfaction Score (rated patients only) | 5.47 / 10 |
| Satisfaction Response Rate | 24.9% (2,295 of 9,216 patients) |
| Admission Rate | 50% |

**Data quality note on Satisfaction Score:** 75.1% of records (6,921 of 9,216) have a blank Satisfaction Score — these patients did not leave a rating. Only 2,295 patients (24.9%) actually provided a satisfaction score. All satisfaction averages below are calculated on **rated patients only** (blanks are automatically excluded by AVERAGE/pivot calculations), with a Response Rate metric reported alongside so the reader can see how much data each average is based on.

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
| Age vs. Risk Score | ~0.31 | Weak positive — risk tends to rise with age, but age alone doesn't fully explain risk |
| Risk Score vs. Length of Stay | ~0.30 | Weak positive — higher-risk patients tend to stay longer, though other factors also drive length of stay |
| **Risk Score vs. Satisfaction (rated patients)** | **~-0.56** | **Moderate-to-strong negative — the strongest relationship in the dataset. Higher-risk patients report meaningfully lower satisfaction.** |
| Wait Time vs. Satisfaction | ~0.00 | No relationship — wait time does not meaningfully predict how satisfied a patient reports being |
| Age vs. Length of Stay | ~0.01 | No relationship — a patient's age does not predict how long they stay; Risk Score is the real driver |

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
Total Patients · Average Wait Time · Average Satisfaction Score (rated patients) · Satisfaction Response Rate · Admission Rate · Wait-Time Variability · Expected Admissions · Risk Distribution · Ward Distribution · Length of Stay Distribution

### Analysis Sections
Monthly Admission Trend · Department-wise Patient Distribution · Gender Distribution · Hospitalization Duration by Department · Age Group Distribution · Risk Category Distribution · Length of Stay Distribution · Ward Type Distribution · Day-wise Admission Analysis · Department Bottleneck Analysis · Department Satisfaction Analysis · Admitted Patients by Age Group · Risk vs Satisfaction Analysis

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
- Risk vs Satisfaction Correlation Analysis
- Gender Distribution Analysis
- Blood Group Analysis
- Day-of-Week Admission Pattern Analysis

---

# Key Insights

## Admission Trends
- Admissions rise steadily from March to August, peaking in August, then decline toward year-end — indicating seasonal patterns.
- Weekend admissions (Saturday: 1,368; Sunday: 1,361) run slightly higher than weekday admissions (lowest on Thursday: 1,268) — roughly an 8% gap, worth factoring into weekend staffing plans.

## Risk Patterns
- High-risk patients are concentrated in the 71–80 age group, followed by 61–70; risk severity increases with age.
- Low-risk patients are least represented in these older age groups.
- High-risk patients generally have longer hospitalization durations — 50% fall into Extended Stay (vs 17% of Medium-Risk and just 2% of Low-Risk), and High-Risk patients are also disproportionately represented in Critical Long Stay cases (3.84%, compared to 1.73% for Medium-Risk and only 0.12% for Low-Risk) — nearly 32x higher than Low-Risk patients.
- High-Risk concentration is fairly close across departments (12.9%–16.1% range) — General Practice has the highest share (16.14%), followed by Physiotherapy (15.94%) and Cardiology (15.73%), while Gastroenterology has the lowest (12.92%). The "None" (unspecified referral) group sits mid-range at 14.93% — it is not the highest, despite having the largest patient volume. Variation is more pronounced in the Low/Medium-Risk splits: Physiotherapy stands out with the lowest Low-Risk share (38.77%) and highest Medium-Risk share (45.29%), while Orthopedics has the highest Low-Risk share (46.23%).

## ICU & Critical Care
- ICU accounts for only **10%** of total admissions but carries disproportionate severity:
  - ~**35%** of ICU patients are High Risk
  - Average ICU stay: **10 days**
  - ~**63%** of ICU patients fall in the Extended Stay category (short stays are minimal)
- ICU pressure is driven by patient **severity**, not volume.

## Blood Group Patterns
- O+ has the highest patient volume overall (2,747 patients).
- By raw count, B+ has the highest number of High-Risk patients (403), followed by O+ (396) — B+ also leads in ICU admissions (271 vs O+'s 243).
- However, by percentage within each blood group, O- has the highest High-Risk rate (~19%), even though its overall volume is small — B+ (~16%) and A+ (~15%) follow. This means O- carries proportionally more risk per patient despite fewer total patients.
- Blood group distribution is otherwise fairly consistent — most groups have a similar High-Risk share (roughly 13–15%), except O- which stands out at ~19%.

## Wait-Time Pressure
- General Ward has the most high-wait-time cases (**1,986**) vs. ICU's **360**.
- The "None" referral category and General Practice see the highest concentrations of high-wait-time patients.
- Medium-Risk patients contribute the most high-wait-time cases (**2,136**); High-Risk contributes **1,195**.
- **~87%** of High-Risk patients experience High Wait-Time; **~57%** of Medium-Risk patients do.
- Despite this wait-time pressure, wait time itself does **not** correlate with satisfaction (correlation ~0.00) — patients aren't rating their experience lower simply because they waited longer. Something else is driving dissatisfaction (see Satisfaction Insights below).

## Length of Stay
- Most patients fall under Normal Stay; short Stay is the second-largest segment.
- Critical Long-Stay patients are few but resource-intensive.
- **~50%** of High-Risk patients are Extended Stay, vs. only **~17%** of Medium-Risk (**~56%** of Medium-Risk are Normal Stay).
- A small patient group accounts for a disproportionate share of hospital occupancy.
- A patient's **age does not predict** length of stay (correlation ~0.01) — Risk Score is the real driver of how long someone stays, not age alone.

## Ward-Level Patterns
- **General Ward:** Largest patient population and workload; highest number of Normal Stay patients and high-wait-time cases.
- **ICU:** Fewer patients but highest concentration of Extended Stay and prolonged hospitalization.
- **Private Ward:** Balanced stay distribution; lower prolonged-care pressure than ICU.

## Department-Level Patterns
- General Practice has the highest High-Risk concentration (16.14%) among departments, followed by Physiotherapy (15.94%) and Cardiology (15.73%); Gastroenterology has the lowest (12.92%).
- The "None" (unspecified referral) category has the largest patient volume (58% of all patients) and therefore contributes the most raw ICU admissions and Extended Stay cases — but its High-Risk rate (14.93%) is actually mid-range, not the highest.
- Orthopedics shows moderate long-duration recovery; Cardiology slightly longer treatment durations; Neurology is relatively stable.
- Renal and Gastroenterology have lower hospitalization intensity.
- **Gastroenterology has the highest patient satisfaction score (5.91/10 among rated patients, 29.8% response rate)**, and satisfaction stays fairly close across departments (5.25–5.91 range) — higher volume doesn't necessarily mean lower satisfaction.

## Satisfaction Insights (New)
- **Risk severity is the strongest predictor of satisfaction in the dataset** — correlation of **-0.56** between Risk Score and Satisfaction, well above the Age-Risk (0.31) and Risk-LOS (0.30) relationships.
- High-Risk patients report the lowest average satisfaction (**3.03/10**) and are also the least likely to leave a rating at all (**13.5% response rate**).
- Low-Risk patients report the highest average satisfaction (**6.31/10**) and respond at more than double the rate (**36.0%**).
- Medium-Risk patients sit in between on both measures (4.26/10, 17.0% response rate).
- This suggests satisfaction, wait-time burden, and extended hospitalization all compound for the same High-Risk patient group — they wait longer, stay longer, *and* report (and share) a worse experience.

---

# How These Patterns Connect

- **Age drives resource consumption:** The 61–80 age bracket dominates High/Medium-Risk categories and is more likely to need ICU care and longer stays.
- **High-Risk patients strain multiple fronts at once:** 50% land in Extended Stay and 87% in High Wait-Time — simultaneously affecting clinical workload, bed occupancy, and delays. They also report the lowest satisfaction of any risk group (3.03/10) — clinical burden and patient experience decline together.
- **ICU burden comes from severity, not volume:** ICU accounts for only 10% of total admissions, yet 35% of ICU patients are High Risk, average ICU stay is 10 days, and 63% fall in Extended Stay — showing ICU pressure is driven by patient severity rather than patient count.
- **Referral gaps concentrate pressure:** The "None" referral category and General Practice repeatedly show up across High-Risk, ICU, Extended Stay, and High-Wait-Time cases — largely because "None" is the single largest patient group by volume (58% of patients), not because it has an unusually high concentration of risk.
- **Risk severity and length of stay move together:** As risk rises, so does hospitalization duration (50% of High-Risk vs. 17% of Medium-Risk in Extended Stay).
- **Risk severity and satisfaction move in opposite directions:** As risk rises, satisfaction falls sharply (-0.56 correlation) — much more strongly than wait time or age influence satisfaction.

---

# Business Recommendations

## 1. Improve ICU Resource Planning
- Monitor Extended Stay patients more closely.
- Improve ICU bed allocation planning.
- Track prolonged-care cases proactively.

**Reason:** ICU patients stay longer and consume a larger share of hospital resources.

## 2. Reduce General Ward Congestion
- Improve patient-flow management.
- Optimize staffing during busy periods (note the weekend admission uptick).
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
- Improve referral documentation to reduce the "None"/unspecified referral bucket.
- Standardize patient-routing processes.

**Reason:** The "None" referral category's large volume makes it a major contributor to raw ICU and Extended Stay counts, even though its risk rate is average — better routing data would enable more precise department-level analysis.

## 6. High-Risk Patient Fast-Track Monitoring
- Prioritize High-Risk patients during admission and assessment.
- Create dedicated monitoring workflows.
- Improve early intervention practices.

**Reason:** 87% of High-Risk patients experience High Wait-Time, 50% belong to Extended Stay, and they report the lowest satisfaction of any risk group — this is the single group under the most compounding pressure.

## 7. Close the Satisfaction Response Gap
- Improve satisfaction survey capture, especially for High-Risk and long-stay patients (only 13.5% currently respond).
- Investigate *why* higher-risk patients rate lower — is it clinical outcome, wait time within their stay, communication, or something else? (Note: overall wait time does not correlate with satisfaction, so the driver is likely elsewhere.)
- Treat the 75% of patients with no rating as a data-collection gap to close, not as a true reflection of average patient sentiment.

**Reason:** Risk Score is by far the strongest predictor of satisfaction (-0.56) in the dataset, and the patients least likely to respond are the ones the hospital most needs feedback from.

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

Hospital operations face two core challenges: high patient volume in the General Ward, and prolonged, high-severity care in the ICU. General Ward drives the bulk of operational workload and wait-time pressure, while ICU — despite lower volume — demands significantly more resources due to higher patient risk and longer stays. A third, less obvious pattern ties these together: patient risk severity is the strongest predictor of satisfaction in the dataset (-0.56), stronger than wait time or age — meaning the same High-Risk patients driving clinical and operational strain are also the ones reporting (and least often sharing) the worst experience. Addressing patient-flow management, ICU capacity planning, referral tracking, and proactive monitoring of high-risk groups — alongside closing the satisfaction feedback gap for this group — offers the clearest path to improving overall hospital efficiency.
