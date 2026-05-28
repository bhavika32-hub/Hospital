# Dynamic Healthcare Operational Analysis Dashboard & Automated Reporting

---

## Problem Statement

The objective of this project was to analyze hospital operational and patient management data to identify critical healthcare patterns, operational bottlenecks, patient risk trends, and hospitalization behavior. The analysis focuses on improving hospital resource utilization, patient flow efficiency, wait-time management, and critical-care operations through data-driven insights.

---

## Business Objective

The objective of this analysis is to understand hospital operational behavior and improve overall healthcare service efficiency using analytical insights. The focus areas include:

* Identifying high-risk patient groups and critical-care dependency patterns
* Improving patient flow efficiency and reducing operational congestion
* Analyzing wait-time pressure across wards and departments
* Understanding hospitalization duration and extended-stay behavior
* Optimizing ICU resource utilization and prolonged care management
* Monitoring ward-level operational workload and patient distribution
* Supporting healthcare decision-making through dynamic KPI reporting and operational analytics

---

## Tools Used

* Microsoft Excel
* Pivot Tables
* Power Query
* Excel Formulas
* Dynamic KPI Reporting
* Interactive Dashboarding

---

## Dataset

* 9K+ patient records
* Data included:

  * Patient demographics
  * Ward type
  * Department referrals
  * Risk score & risk category
  * Length of stay
  * Length of stay segments
  * Patient wait time
  * Wait-time categories
  * Patient satisfaction
  * Blood group
  * Admission information
  * Payment methods

---

## Custom Features & Data Engineering

* Created custom **Risk Score** and **Risk Category** logic using Excel formulas
* Built dynamic **Length of Stay Segments** for hospitalization analysis
* Designed custom **Age Group classifications** for demographic segmentation
* Created operational categories for patient wait-time analysis
* Automated KPI calculations and dynamic reporting workflows
* Structured healthcare operational data for interactive analysis

---

## KPI Tracking

* Total Patients Treated
* Average Patient Wait Time
* Patient Satisfaction Score
* Admission Rate
* Wait-Time Variability
* Expected Admissions
* Ward-Level Patient Distribution
* Risk Category Distribution
* Length of Stay Distribution
* ICU Extended-Stay Contribution

---

## Key Analysis Performed

* Analyzed patient risk distribution across age groups and wards
* Evaluated ICU dependency and prolonged hospitalization behavior
* Studied wait-time burden across ward types and operational workflows
* Identified extended-stay and critical long-stay patient patterns
* Compared hospitalization duration across departments and wards
* Evaluated department-level operational pressure and referral behavior
* Studied patient satisfaction trends across hospital departments
* Performed demographic analysis using age, gender, race, and blood group distributions
* Built dynamic Pivot Table reports and refreshable KPI dashboards
* Automated healthcare operational reporting using Power Query transformations

---

## ⚡ Dashboard Automation Features

* Built dynamic Pivot Table and KPI reporting workflows
* Used Power Query for automated data transformation and refresh
* Dashboard updates dynamically when new healthcare data is added
* Implemented slicers and filters for interactive operational reporting
* Enabled dynamic analysis by Year, Month, and Age Group selections
* Automated category segmentation using Excel formulas

---

## Dynamic Reporting Workflow

* Raw patient data can be updated directly in the source sheet
* Power Query automatically refreshes transformed healthcare data
* Pivot Tables and KPIs update dynamically after refresh
* Dashboard visuals reflect updated operational and patient insights automatically
* Interactive slicers enable dynamic operational analysis

---

## Key Insights

### Risk & Critical Care Insights

* High-risk patients are predominantly concentrated in the **60–80 age group**
* Low-risk patients are primarily observed between the **20–40 age range**
* ICU patients exhibit significantly higher risk intensity compared to other wards
* Approximately **35% of ICU cases belong to the high-risk category**
* Blood group **B+** shows the highest concentration of high-risk and ICU patients
* High-risk patients tend to experience longer hospitalization durations

---

### ICU & Extended Stay Insights

* ICU patients represent only **10% of total admissions**, yet require significantly higher clinical attention
* ICU patients record an average hospitalization duration of **10 days**
* Approximately **66% of ICU patients fall under the Extended Stay category**
* ICU contributes disproportionately to prolonged hospitalization burden despite lower patient volume
* Short-stay admissions are minimal in ICU, reflecting elevated patient severity levels

---

### Wait-Time & Operational Insights

* General Ward records the **highest number of high wait-time cases (1,975 patients)**
* Operational congestion is concentrated more heavily in General Ward workflows
* Lower-risk patients account for most operational waiting pressure
* High wait-time cases are more frequently observed during weekdays
* ICU contributes fewer high wait-time cases but requires operational attention due to patient severity

---

### Length of Stay Insights

* The majority of patients fall under the **Normal Stay category**
* Extended Stay cases contribute significantly to operational resource utilization
* Critical long-stay patients remain limited in volume but represent high-intensity care dependency
* ICU records the highest concentration of Extended Stay patients
* A relatively small segment of patients contributes disproportionately to hospital resource occupancy

---

### Department-Level Insights

* Patients without a specified referral department (“None”) account for the highest concentration of Extended Stay and Critical Long-Stay cases
* General Practice contributes significantly to prolonged hospitalization cases
* Cardiology records comparatively longer treatment durations
* Gastroenterology maintains the highest patient satisfaction performance
* Department-level hospitalization distribution remains operationally stable overall

---

### Satisfaction Insights

* Gastroenterology records the highest patient satisfaction performance among all departments
* Patient satisfaction remains relatively stable despite fluctuating admission volumes
* Higher patient load does not always correspond to lower satisfaction levels

---

## Interconnected Operational Insights

### 1. Age-Driven Critical Care Dependency

The analysis indicates a strong relationship between patient age, risk severity, and critical-care dependency. High-risk patients are predominantly concentrated within the 60–80 age group, while lower-risk patients are mostly observed between 20–40 years of age. This increasing risk severity with age directly contributes to higher ICU dependency, prolonged hospitalization durations, and extended recovery cycles among senior patients.

As a result, senior-age patient groups contribute disproportionately to high-intensity healthcare utilization and long-duration hospital occupancy.

---

### 2. ICU Resource Intensity vs Patient Volume

Although ICU patients account for only a small proportion of total admissions, ICU operations demonstrate significantly higher clinical severity and operational dependency. ICU patients exhibit higher average risk scores, longer hospitalization durations, and the highest concentration of Extended Stay cases.

Nearly two-thirds of ICU patients fall under the Extended Stay category, indicating that ICU resource utilization is driven more by prolonged care intensity than patient volume. This suggests that even limited ICU occupancy can create substantial operational pressure on hospital resources, staffing, and bed availability.

---

### 3. Operational Congestion Is Concentrated Outside ICU

Despite ICU patients requiring higher clinical attention, the largest operational congestion is observed in General Ward workflows. General Ward handles the majority of low-risk and normal-stay patients but simultaneously records the highest number of high wait-time cases.

This indicates that operational delays are being driven more by patient volume imbalance and workflow pressure rather than patient severity. Lower-risk patients contribute disproportionately to waiting burden, especially during weekday admission peaks.

---

### 4. Extended-Stay Patients Drive Resource Utilization

Most patients fall within stable hospitalization ranges; however, a relatively small proportion of Extended Stay and Critical Long-Stay patients contribute disproportionately to hospital resource occupancy.

This extended hospitalization burden is heavily concentrated within ICU operations and unspecified referral cases, indicating that severe clinical dependency and inefficient referral allocation both contribute to prolonged patient retention.

---

### 5. Referral Inefficiencies May Be Increasing Prolonged Hospitalization

Patients categorized under unspecified referral departments (“None”) demonstrate the highest concentration of Extended Stay and Critical Long-Stay cases.

This pattern may indicate operational inefficiencies in referral allocation, delayed diagnosis workflows, incomplete patient-routing processes, or potential data-quality inconsistencies.

---

### 6. Critical-Care Burden Is Concentrated Within Specific Patient Groups

The analysis reveals that critical-care dependency is not evenly distributed across the patient population. Senior-age, high-risk, and B+ blood group patients contribute disproportionately to ICU admissions and prolonged hospitalization patterns.

This concentration indicates that hospital resource-intensive operations are being driven by a relatively limited but clinically severe patient segment.

---

### 7. Wait-Time Pressure and Patient Severity Follow Different Operational Patterns

The analysis shows that high wait-time pressure is concentrated primarily among lower-risk General Ward patients, while ICU patients experience lower waiting pressure but substantially longer treatment cycles.

This indicates that hospital workflows operate under two distinct operational burdens:

* High-volume workflow congestion
* High-severity prolonged-care dependency

---

### 8. Hospitalization Duration Reflects Severity-Based Recovery Cycles

Length-of-stay distribution patterns demonstrate that hospitalization duration is strongly linked to patient severity and ward dependency. ICU and high-risk patients consistently exhibit longer treatment cycles, while General Ward patients show comparatively stable discharge patterns.

This indicates that hospitalization duration is heavily influenced by critical-care dependency, recovery complexity, and patient severity levels.

---

## Actionable Business Recommendations

### 1. ICU Resource Optimization Strategy

* Increase monitoring and resource planning for Extended Stay ICU patients
* Improve critical-care bed allocation efficiency
* Strengthen prolonged-care management workflows

**Reason:**
ICU patients contribute disproportionately to prolonged hospitalization durations and resource utilization despite lower admission volume.

---

### 2. General Ward Congestion Reduction

* Optimize patient flow management in General Ward
* Improve operational scheduling during peak weekday admissions
* Introduce workload-balancing strategies for high-volume patient intake

**Reason:**
General Ward experiences the highest wait-time burden and operational congestion despite handling predominantly low-risk patients.

---

### 3. Senior High-Risk Patient Monitoring

* Implement proactive monitoring for senior-age high-risk patients
* Prioritize early intervention programs for critical-risk groups
* Improve preventive healthcare tracking for vulnerable demographics

**Reason:**
Senior-age patients contribute disproportionately to ICU dependency and prolonged hospitalization patterns.

---

### 4. Extended Stay Management Strategy

* Create specialized monitoring workflows for Extended Stay patients
* Improve discharge planning and recovery coordination
* Monitor long-duration occupancy trends more proactively

**Reason:**
A relatively small segment of patients contributes disproportionately to operational occupancy and prolonged resource utilization.

---

### 5. Referral Workflow Optimization

* Improve referral tracking and department allocation accuracy
* Reduce dependency on unspecified referral classifications
* Strengthen patient-routing workflows and operational documentation

**Reason:**
Unspecified referral categories show unusually high concentrations of Extended Stay and Critical Long-Stay cases.

---

### 6. Wait-Time Optimization Strategy

* Introduce operational balancing during weekday peak loads
* Improve queue and patient handling efficiency in General Ward operations
* Strengthen staffing allocation during high-volume operational periods

**Reason:**
Weekday admission pressure contributes significantly to operational delays and wait-time escalation.

---

## Success Measurement (Expected Impact)

* Improved ICU resource utilization and prolonged-care management
* Reduction in operational congestion and patient wait times
* Better identification and monitoring of high-risk patient groups
* Enhanced visibility into hospitalization duration and patient-flow behavior
* Improved operational decision-making through dynamic healthcare KPI reporting
* Better patient-routing and referral allocation efficiency
* Reduced manual reporting effort with automated and refreshable dashboard workflows

---

## Executive Summary

Hospital operational analysis indicates that healthcare resource pressure is being driven by two parallel operational burdens: high-volume workflow congestion within General Ward operations and prolonged treatment dependency within ICU environments. While lower-risk patients contribute most of the operational waiting pressure, senior-age and high-risk patients contribute disproportionately to ICU occupancy, Extended Stay cases, and prolonged hospitalization durations. The findings suggest that improving workflow efficiency, referral accuracy, and proactive monitoring of high-risk demographic groups could significantly enhance hospital operational performance, patient-flow efficiency, and critical-care resource utilization.
