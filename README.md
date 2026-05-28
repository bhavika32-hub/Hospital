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

## Actionable Business Recommendations

### 1. ICU Resource Optimization Strategy

* Increase monitoring and resource planning for Extended Stay ICU patients
* Improve critical-care bed allocation efficiency

**Reason:**
ICU patients contribute disproportionately to prolonged hospitalization durations and resource utilization despite lower admission volume.

---

### 2. General Ward Congestion Reduction

* Optimize patient flow management in General Ward
* Improve operational scheduling during peak weekday admissions

**Reason:**
General Ward experiences the highest wait-time burden and operational congestion despite handling predominantly low-risk patients.

---

### 3. High-Risk Patient Monitoring Strategy

* Implement proactive monitoring for senior-age high-risk patients
* Prioritize early intervention programs for critical-risk groups

**Reason:**
High-risk cases are strongly concentrated among senior-age patients and are associated with prolonged hospitalization durations.

---

### 4. Extended Stay Management Strategy

* Create specialized monitoring workflows for Extended Stay patients
* Improve discharge planning and recovery coordination

**Reason:**
A small proportion of patients contributes disproportionately to operational occupancy and long-duration hospitalization pressure.

---

### 5. Operational Workflow Improvement

* Improve referral tracking and department allocation accuracy
* Reduce dependency on unspecified referral classifications

**Reason:**
Patients with unspecified referral departments show unexpectedly high extended-stay concentrations, indicating operational or data-quality inconsistencies.

---

### 6. Wait-Time Optimization Strategy

* Introduce operational balancing during weekday peak loads
* Improve queue and patient handling efficiency in General Ward operations

**Reason:**
Weekday admission pressure contributes significantly to operational delays and wait-time escalation.

---

## Success Measurement (Expected Impact)

* Improved ICU resource utilization and prolonged-care management
* Reduction in operational congestion and patient wait times
* Better identification and monitoring of high-risk patient groups
* Enhanced visibility into hospitalization duration and patient-flow behavior
* Improved operational decision-making through dynamic healthcare KPI reporting
* Reduced manual reporting effort with automated and refreshable dashboard workflows

---

## Executive Summary

Hospital operational analysis indicates that while ICU handles a relatively smaller proportion of total admissions, it carries significantly higher clinical severity and prolonged hospitalization dependency. Nearly two-thirds of ICU patients fall under the Extended Stay category, emphasizing elevated care intensity and resource utilization. General Ward experiences the highest operational wait-time burden despite managing predominantly low-risk patients, while extended hospitalization pressure is heavily concentrated among high-risk and senior-age patient groups.
