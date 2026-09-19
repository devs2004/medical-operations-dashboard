# Medical Operations Dashboard — Team B Batch 1

## Milestone 1 — Work Completed

Milestone 1 focused on establishing the core data foundation for the **Medical Operations Intelligence Dashboard**. During this milestone, the team generated a synthetic healthcare dataset, performed data cleaning and validation, and developed an initial set of operational and financial **Key Performance Indicators (KPIs)**.

---

### 1. Dataset Generation

A synthetic healthcare dataset was generated to represent realistic hospital operations, including patient, admission, staff, billing, insurance, bed, and operational information.

#### Dataset Overview

| Attribute         | Details                         |
| ----------------- | ------------------------------- |
| **Total Records** | 5,000                           |
| **Total Columns** | 32                              |
| **Dataset Type**  | Synthetic Healthcare Dataset    |
| **Primary Use**   | Hospital Operations & Analytics |

The dataset was designed to support healthcare operational analysis, KPI development, and dashboard development.

---

### 2. Data Cleaning & Preparation

The generated dataset was cleaned and prepared to ensure consistency, reliability, and analysis readiness.

The following data preparation activities were performed:

* Converted `Admission_Date` and `Discharge_Date` into appropriate datetime formats.
* Converted `Contact_Number` into string format to preserve complete contact information.
* Checked the dataset for missing values.
* Identified and reviewed duplicate records.
* Validated patient age values for logical consistency.
* Performed general data quality checks.
* Reviewed relevant fields for consistency and usability in downstream analysis.

These preprocessing steps helped improve the quality and reliability of the dataset before further analysis.

---

### 3. Data Validation

Business and logical validation rules were applied to verify the consistency of financial information within the dataset.

The following relationships were validated:

* `Paid_Amount` should not exceed `Total_Amount`.
* `Insurance_Coverage + Paid_Amount` should equal `Total_Amount`.

These validation checks helped ensure that the financial records were logically consistent and suitable for further analysis and reporting.

---

### 4. KPI Development

Initial **Key Performance Indicators (KPIs)** were identified and calculated to provide a high-level overview of hospital operations and financial performance.

#### KPIs Developed

| KPI                             | Purpose                                                            |
| ------------------------------- | ------------------------------------------------------------------ |
| **Total Admissions**            | Measures the total number of hospital admissions.                  |
| **Currently Admitted Patients** | Tracks the number of patients currently admitted.                  |
| **Average Length of Stay**      | Measures the average duration of patient hospitalization.          |
| **Bed Occupancy Percentage**    | Indicates the utilization level of available hospital beds.        |
| **Total Revenue**               | Represents the total revenue generated from hospital billing.      |
| **Collection Rate Percentage**  | Measures the proportion of billed revenue that has been collected. |

These KPIs provide an initial overview of important **operational, capacity, and financial metrics** and establish the foundation for the project dashboard.

---

### 5. Cleaned Dataset

After completing the data cleaning and validation process, the cleaned dataset was exported for further analysis and dashboard development.

#### Output Dataset

```text
medical_operations_dashboard_cleaned.csv
```

The data cleaning and preprocessing workflow is documented in the following Jupyter Notebook:

```text
notebooks/Data_Cleaning.ipynb
```

---

### 6. KPI Summary

The initial KPI calculations and summary were prepared using **Microsoft Excel**.

The KPI summary provides an initial overview of the hospital's operational and financial performance and will serve as a foundation for:

* Dashboard development
* Further data analysis
* KPI visualization
* Operational performance monitoring

---

## 🎯 Milestone 1 Outcome

By the end of **Milestone 1**, the team successfully established the initial project foundation by preparing and validating the healthcare dataset and developing the first set of operational and financial **Key Performance Indicators (KPIs)**.

### Completed Deliverables

* ✅ Generated a synthetic healthcare dataset containing **5,000 records and 32 columns**
* ✅ Performed data cleaning and preprocessing
* ✅ Checked missing values and duplicate records
* ✅ Validated patient age values
* ✅ Applied financial and business validation rules
* ✅ Developed initial operational KPIs
* ✅ Developed initial financial KPIs
* ✅ Exported the cleaned dataset
* ✅ Documented the cleaning process in a Jupyter Notebook
* ✅ Prepared the initial KPI summary in Microsoft Excel

---

## 🔍 Next Milestone

The prepared dataset and KPI definitions will be used in the next milestone for:

* 🔍 **Exploratory Data Analysis (EDA)**
* 📊 **Detailed Data Visualization**
* 📈 **Dashboard Development**
* 🏥 **Deeper Healthcare Operational Insights**

The next phase will focus on transforming the validated healthcare data into meaningful visual insights and actionable information for understanding hospital operations.

---

## 📁 Relevant Project Files

```text
medical-operations-dashboard-team-b-batch-1/
│
├── data/
│   └── medical_operations_dashboard_cleaned.csv
│
├── notebooks/
│   └── Data_Cleaning.ipynb
│
└── README.md
```

> **Note:** The project structure may be updated as additional notebooks, datasets, dashboards, and documentation are added in subsequent milestones.

---

## 📌 Conclusion

Milestone 1 established a reliable and validated data foundation for the **Medical Operations Intelligence Dashboard**.

Through dataset generation, data cleaning, validation, and KPI development, the project is now prepared to move into the next stage of **exploratory analysis, visualization, and dashboard development**.

The insights generated in the upcoming milestones will help provide a clearer understanding of **patient flow, hospital capacity, resource utilization, and financial performance**.


# 🏥 Milestone 2 — Patient Flow, Treatment Demand & Operational Bottleneck Analysis

> **Healthcare Operations Intelligence | Power BI Dashboard Module**

## 📌 Overview



**Milestone 2** focuses on transforming hospital medical operations data into meaningful insights related to **patient flow, treatment demand, departmental workload, bed utilization, and operational bottlenecks**.

The objective of this milestone is to convert patient-level operational data into an **interactive Power BI analytics solution** that enables hospital management to monitor demand patterns, understand departmental workload, evaluate resource utilization, and identify areas requiring further operational attention.

The analysis creates a clear operational flow:

**Patient Flow → Treatment Demand → Department Workload → Bed Utilization → Operational Bottlenecks**

---

## 🎯 Objectives

The primary objectives of this milestone are to:

* 📊 Analyze overall patient admissions and patient flow.
* 🏥 Identify departments with higher patient volumes.
* 💊 Analyze treatment demand and treatment trends.
* 🛏️ Examine bed-status distribution and utilization.
* ⏱️ Compare departmental **Length of Stay (LOS)**.
* 💰 Analyze departmental billing and operational workload.
* 🚨 Identify potential operational bottlenecks and high-demand areas.
* 📈 Provide management with data-driven insights for operational decision-making.

---

## ❓ Key Business Questions

The dashboard was designed around important hospital operations questions:

1. How is patient admission volume changing over time?
2. Which departments handle the highest number of patients?
3. Which treatments have the highest demand?
4. How is treatment demand changing over time?
5. What is the current distribution of bed statuses?
6. Which wards or departments have higher occupancy?
7. Which departments have higher average Length of Stay?
8. Where are potential operational bottlenecks and high-demand areas?
9. How do departmental billing and patient volume vary?

---

# 📊 Dashboard Structure

The Power BI solution is organized into **three analytical pages**, each focusing on a different aspect of hospital operations.

---

## 1️⃣ Patient Flow & Hospital Overview

### 📌 Purpose

This page provides a **high-level overview of patient activity and hospital operations**, allowing management to quickly understand the current operational picture.

### 📈 Key Performance Indicators

| KPI                           | Purpose                                |
| ----------------------------- | -------------------------------------- |
| 👥 **Total Patients**         | Measures overall patient volume        |
| 🏥 **Total Admissions**       | Tracks hospital admission activity     |
| 🛏️ **Occupied Beds**         | Indicates current bed utilization      |
| ⏱️ **Average Length of Stay** | Measures average patient stay duration |

### 📊 Visualizations

* **Quarterly Admission Trend**

  * Tracks changes in admission volume over time.

* **Admissions by Department**

  * Identifies departments handling the highest number of admissions.

* **Patient Distribution by Gender**

  * Provides an overview of patient population composition.

* **Bed Status Distribution**

  * Displays the distribution of beds across:

    * Occupied
    * Available
    * Reserved
    * Cleaning

### 🎯 Key Question Answered

> **"What is happening across the hospital overall?"**

---

# 2️⃣ Treatment Demand & Departmental Workload

### 📌 Purpose

This page analyzes **treatment demand and departmental workload** to identify services that consistently contribute to patient volume.

### 📊 Visualizations

#### 🔝 Top 5 Treatment Demand Trend

Tracks the demand for the five most frequently used treatments over time.

#### 🥧 Treatment Demand Share

Shows the contribution of different treatments to overall patient demand.

#### 👥 Total Patients by Treatment

Compares patient volume across treatments.

#### 📅 Yearly Top 5 Treatment Comparison

Provides a year-wise comparison of the most demanded treatments.

### 🎯 Key Insights Supported

The dashboard helps identify:

* High-demand treatments.
* Changes in treatment demand over time.
* Treatments that consistently contribute to patient volume.
* Services requiring additional operational planning.

### 💡 Operational Value

Treatment demand analysis can support decisions related to:

**Staffing → Treatment Capacity → Equipment → Service Planning**

---

# 3️⃣ Operational Bottlenecks & High-Demand Areas

### 📌 Purpose

The third dashboard focuses on identifying **departments and wards that may require greater operational attention**.

### 📈 Key Performance Indicators

| KPI                            | Purpose                                       |
| ------------------------------ | --------------------------------------------- |
| 🔝 **Highest Patient Volume**  | Identifies the area handling maximum patients |
| ⏱️ **Highest Average LOS**     | Identifies areas with longer patient stays    |
| 💰 **Average Billing**         | Measures average financial workload           |
| 🛏️ **Highest Ward Occupancy** | Highlights wards with higher bed utilization  |

### 📊 Visualizations

* **Patient Volume by Ward**
* **Bed Availability**
* **Average Length of Stay by Department**
* **Billing by Department**

### 🔎 Operational Analysis Framework

The dashboard connects four important operational dimensions:

**Patient Volume → Bed Capacity → Length of Stay → Financial / Operational Workload**

For example:

> A department experiencing **high patient volume and high bed occupancy** may indicate a potential capacity constraint and could require further investigation into staffing, bed capacity, or patient flow.

---

# 🔍 Key Insights

The analysis indicates that **patient demand and hospital resources are not evenly distributed** across departments and wards.

### 🏥 Departmental Demand

Some departments handle substantially higher patient volumes than others, indicating differences in service demand and workload.

### 💊 Treatment Demand

Treatment demand varies across services, with certain treatments contributing a larger share of overall patient activity.

### 🛏️ Bed Utilization

Bed availability and utilization differ across wards. The analysis identified relatively high occupancy in areas such as the **Cardiac Ward and General Ward**, while some other wards showed comparatively lower occupied-bed levels.

### ⏱️ Length of Stay

The overall **Average Length of Stay (LOS) was approximately 7.9 days**.

The differences in average LOS between departments were relatively small. This suggests that **patient volume and capacity utilization may provide more useful indicators of operational pressure than LOS alone**.

### 🚨 Operational Pressure

High patient volume combined with high occupancy can indicate a potential operational pressure point. These areas may require further investigation into:

* Bed capacity
* Staffing requirements
* Treatment capacity
* Patient flow
* Resource allocation

> **Note:** High occupancy or patient volume is treated as an indicator for further investigation, not as definitive proof of an operational bottleneck.

---

# 🛠️ Tools & Technologies

| Technology                 | Usage                                    |
| -------------------------- | ---------------------------------------- |
| 🟨 **Microsoft Power BI**  | Interactive dashboard development        |
| 📐 **DAX**                 | KPI calculations and analytical measures |
| 📄 **CSV Dataset**         | Hospital medical operations data source  |
| 📊 **Bar Charts**          | Department and treatment comparisons     |
| 📈 **Line Charts**         | Admission and treatment trends           |
| 🍩 **Donut Charts**        | Distribution and share analysis          |
| 🎯 **KPI Cards**           | High-level operational metrics           |
| 🔎 **Interactive Filters** | Dynamic dashboard exploration            |

---

# 📂 Project Structure

```text
Milestone-2/
│
├── 📊 PowerBI/
│   └── Patient_Flow_Operational_Bottleneck_Analysis.pbix
│
├── 📁 Dataset/
│   └── hospital_medical_operations.csv
│
├── 📸 Dashboard_Screenshots/
│   ├── patient_flow_overview.png
│   ├── treatment_demand.png
│   └── operational_bottlenecks.png
│
└── 📄 README.md
```

> Update the filenames above according to the actual files in your repository.

---

# 📈 Analytical Flow

The overall analytical workflow can be represented as:

```text
Hospital Medical Operations Dataset
                │
                ▼
        Patient-Level Data
                │
                ▼
      Data Analysis & Modeling
                │
                ▼
          DAX Measures
                │
                ▼
       Interactive Power BI
            Dashboards
                │
                ▼
       ┌─────────────────────┐
       │   Patient Flow      │
       ├─────────────────────┤
       │ Treatment Demand    │
       ├─────────────────────┤
       │ Department Workload │
       ├─────────────────────┤
       │ Bed Utilization     │
       ├─────────────────────┤
       │ Bottleneck Analysis │
       └─────────────────────┘
                │
                ▼
       Operational Insights
                │
                ▼
     Data-Driven Decision Making
```

---

# 🎯 Expected Outcome

The **Patient Flow, Treatment Demand & Operational Bottleneck Analysis Module** provides hospital management with a centralized analytical view of:

> **Patient Flow → Treatment Demand → Department Workload → Bed Utilization → Operational Bottlenecks**

By converting raw hospital operational data into interactive visual insights, the dashboard helps management:

* Understand patient admission patterns.
* Identify high-demand departments and treatments.
* Monitor bed utilization.
* Compare departmental workload.
* Evaluate Length of Stay.
* Analyze billing patterns.
* Identify areas requiring further operational investigation.
* Support resource and capacity planning.

---

# 💼 Business Impact

This milestone demonstrates how **Business Intelligence and Data Analytics** can support healthcare operations.

The dashboard moves beyond simply displaying numbers by connecting multiple operational indicators to provide a more complete view of hospital performance.

### From Data → Insights → Decisions

```text
Raw Hospital Data
       ↓
Data Analysis
       ↓
Interactive Visualization
       ↓
Operational Insights
       ↓
Resource & Capacity Planning
       ↓
Better Decision Support
```

---

# 🚀 Future Enhancements

Potential future improvements include:

* 🔮 Patient admission forecasting.
* 📊 Advanced capacity utilization analysis.
* 🚨 Automated bottleneck alerts.
* 📈 Predictive treatment-demand analysis.
* 👨‍⚕️ Staff workload analysis.
* 🛏️ Bed occupancy forecasting.
* 🗺️ Geographic healthcare demand analysis.
* 🤖 Machine Learning-based operational predictions.

---

# 👩‍💻 Project Focus

This milestone demonstrates practical application of:

**Healthcare Analytics • Business Intelligence • Power BI • DAX • Data Visualization • Operational Analytics • KPI Development • Data-Driven Decision Making**

---

## ⭐ Conclusion

Milestone 2 transforms hospital medical operations data into an **interactive operational intelligence solution**.

By combining **patient flow, treatment demand, departmental workload, bed utilization, LOS, and billing analysis**, the dashboard provides a structured view of where hospital demand is concentrated and which areas may require closer operational attention.

> **Turning healthcare data into actionable operational intelligence.** 🏥📊



# 🏥 Milestone 3 — Resource Utilization & Capacity Intelligence

> **Healthcare Resource Analytics | Capacity Planning | Power BI Dashboard Module**

## 📌 Overview

**Milestone 3** focuses on developing a **Resource Utilization & Capacity Intelligence Module** for healthcare operations.

The objective is to analyze how effectively critical hospital resources such as **beds and doctors** are being utilized and to identify departments experiencing potential **capacity or workload pressure**.

Using interactive **Power BI dashboards, KPIs, DAX measures, and analytical visualizations**, the module transforms hospital operational data into actionable insights that can support **resource planning, staffing decisions, and capacity management**.

The analysis follows the operational flow:

**Resource Utilization → Capacity Pressure → Departmental Needs → Resource Planning**

---

## 🎯 Objectives

The primary objectives of this milestone are to:

* 🛏️ Evaluate bed utilization across hospital departments.
* 👨‍⚕️ Analyze patient workload per doctor.
* 🚨 Identify departments experiencing potential resource pressure.
* 📊 Detect areas of high or low resource utilization.
* 🎯 Compare resource utilization against predefined operational benchmarks.
* 👥 Support informed staffing and workload decisions.
* 🏥 Support hospital capacity and resource planning.
* 🔄 Identify opportunities for better resource allocation.

---

# ❓ Key Business Questions

The dashboard was designed to answer important healthcare resource-management questions:

1. Which departments are closest to bed-capacity pressure?
2. How does bed utilization vary across departments?
3. How many patients are being handled per doctor?
4. Which departments may require additional resources?
5. Are hospital resources consistently utilized?
6. Which resources or departments may be underutilized?
7. Which departments show potential staffing pressure?
8. Which departments show potential bed-capacity pressure?
9. How can resource utilization be improved across departments?

---

# 📊 Dashboard Structure

The Resource Utilization & Capacity Intelligence module consists of **three analytical dashboard pages**.

---

# 1️⃣ Resource Overview

### 📌 Purpose

The **Resource Overview** page provides a high-level summary of hospital resource utilization.

It enables management to quickly understand the overall utilization of beds and the distribution of patient workload across doctors.

### 📈 Key Performance Indicators

| KPI                                         | Purpose                                                       |
| ------------------------------------------- | ------------------------------------------------------------- |
| 🛏️ **Overall Bed Utilization %**           | Measures overall hospital bed utilization                     |
| 📊 **Highest Department Bed Utilization %** | Identifies the department with the highest bed utilization    |
| 👨‍⚕️ **Average Patients per Doctor**       | Measures average patient workload per doctor                  |
| 🚨 **High Bed-Utilization Departments**     | Counts departments crossing the defined utilization threshold |

### 📊 Visualizations

#### Bed Utilization by Department

Compares bed utilization across departments and highlights departments operating closer to their available capacity.

#### Patient / Doctor Workload Analysis

Shows the relationship between patient volume and available doctors across departments.

### 🎯 Key Question Answered

> **"How effectively are hospital resources being utilized across departments?"**

---

# 2️⃣ Resource Pressure Analysis

### 📌 Purpose

This page combines **bed utilization and doctor workload** to provide a more comprehensive view of departmental resource pressure.

Instead of evaluating a single metric, the dashboard uses a **Department Resource Pressure Matrix** to identify different types of operational pressure.

---

## 📊 Department Resource Pressure Matrix

A scatter plot is used to compare two important operational indicators:

* **X-axis:** Bed Utilization %
* **Y-axis:** Patients per Doctor
* **Each Point:** Represents an individual department

Operational benchmarks divide departments into four analytical zones.

### 🔎 Pressure Classification

| Condition                                           | Interpretation                               |
| --------------------------------------------------- | -------------------------------------------- |
| 🔴 **High Bed Utilization + High Patient Workload** | Potential pressure on both beds and staffing |
| 🟠 **High Bed Utilization + Low Patient Workload**  | Potential bed-capacity pressure              |
| 🟡 **Low Bed Utilization + High Patient Workload**  | Potential staffing or workload pressure      |
| 🟢 **Low Bed Utilization + Low Patient Workload**   | Relatively lower resource pressure           |

### 💡 Why This Analysis Matters

The matrix helps management understand **not only whether a department has potential pressure, but also what type of resource may be contributing to it**.

For example:

> A department with high bed utilization but relatively low patient workload per doctor may require closer attention to **bed capacity rather than staffing**.

Similarly:

> A department with lower bed utilization but very high patients per doctor may require a **staffing or workload review**.

---

# 3️⃣ Capacity & Overload Analysis

### 📌 Purpose

The final dashboard focuses on identifying **over-utilized and under-utilized resources**.

This helps management understand where hospital capacity may need to be:

**Increased → Redistributed → Optimized → Monitored**

### 🎯 Operational Applications

The analysis can support decisions such as:

* 🛏️ Increasing bed availability in high-pressure departments.
* 👨‍⚕️ Reviewing staffing levels where patient workload is high.
* 📊 Identifying departments with available spare capacity.
* 🔄 Redistributing resources where operationally appropriate.
* 🚨 Monitoring departments repeatedly approaching utilization thresholds.
* 📈 Supporting future capacity planning decisions.

---

# 🔍 Key Insight

A major insight from this analysis is that **a single resource metric is not sufficient to understand operational pressure**.

For example:

### 🛏️ High Bed Utilization + Lower Patient/Doctor Workload

This combination may indicate that **bed capacity** is the more important area requiring attention rather than doctor staffing.

### 👨‍⚕️ Lower Bed Utilization + High Patient/Doctor Workload

This combination may indicate potential **staffing or workload pressure**, even though sufficient bed capacity may be available.

### 🚨 High Bed Utilization + High Patient/Doctor Workload

This represents the most significant potential pressure zone because both **bed capacity and staffing workload** may require attention.

Therefore, combining:

**Bed Utilization + Patient Workload + Operational Benchmarks**

provides a more meaningful picture of **department-level resource pressure** than analyzing individual metrics separately.

---

# 📐 Operational Benchmark Framework

The module uses predefined operational benchmarks to classify departments based on resource utilization.

```text
                    PATIENTS PER DOCTOR
                           HIGH
                            │
          Staffing         │        Dual Resource
          Pressure         │        Pressure
                            │
────────────────────────────┼────────────────────────
                            │
       Lower Resource       │        Bed Capacity
          Pressure          │        Pressure
                            │
                           LOW
                     BED UTILIZATION
              LOW                    HIGH
```

This framework enables management to move from simple monitoring toward **structured capacity intelligence**.

---

# 🛠️ Tools & Technologies

| Technology                    | Usage                                    |
| ----------------------------- | ---------------------------------------- |
| 🟨 **Microsoft Power BI**     | Interactive dashboard development        |
| 📐 **DAX**                    | KPI calculations and analytical measures |
| 📄 **CSV / Hospital Dataset** | Operational data source                  |
| 🎯 **KPI Cards**              | Resource performance monitoring          |
| 📊 **Bar Charts**             | Department-level comparisons             |
| 🔵 **Scatter Plot**           | Resource pressure analysis               |
| 🎯 **Operational Benchmarks** | Pressure-zone classification             |
| 📈 **Interactive Filters**    | Dynamic analysis                         |

---

# 📂 Project Structure

```text
Milestone-3/
│
├── 📊 PowerBI/
│   └── Resource_Utilization_Capacity_Intelligence.pbix
│
├── 📁 Dataset/
│   └── hospital_medical_operations.csv
│
├── 📸 Dashboard_Screenshots/
│   ├── resource_overview.png
│   ├── resource_pressure_analysis.png
│   └── capacity_overload_analysis.png
│
└── 📄 README.md
```

> Update the filenames according to the actual files available in the repository.

---

# 📈 Analytical Flow

The complete analytical process can be represented as:

```text
Hospital Operational Dataset
             │
             ▼
     Resource Data Analysis
             │
             ▼
       DAX Calculations
             │
             ▼
     Resource KPIs & Metrics
             │
             ▼
    ┌────────────────────────┐
    │    Resource Overview   │
    ├────────────────────────┤
    │ Resource Pressure      │
    │ Analysis               │
    ├────────────────────────┤
    │ Capacity & Overload    │
    │ Analysis               │
    └────────────────────────┘
             │
             ▼
    Operational Classification
             │
             ▼
     Capacity Intelligence
             │
             ▼
     Resource Planning
```

---

# 🎯 Expected Outcome

The **Resource Utilization & Capacity Intelligence Module** provides hospital management with a centralized view of:

> **Resource Utilization → Capacity Pressure → Departmental Needs → Resource Planning**

The dashboards transform raw operational data into actionable capacity intelligence by helping identify:

* Departments approaching high bed utilization.
* Patient workload per doctor.
* Potential staffing pressure.
* Potential bed-capacity pressure.
* Underutilized resources.
* Departments requiring closer monitoring.
* Opportunities for resource redistribution.
* Areas requiring future capacity planning.

---

# 💼 Business Impact

This milestone demonstrates how **Business Intelligence and Data Analytics** can support healthcare resource management.

Rather than analyzing beds or staffing independently, the module combines multiple operational indicators to provide a **multi-dimensional view of resource pressure**.

### From Data → Intelligence → Planning

```text
Raw Operational Data
        ↓
Resource Utilization Analysis
        ↓
KPI & DAX Measures
        ↓
Department Comparison
        ↓
Resource Pressure Matrix
        ↓
Capacity Intelligence
        ↓
Staffing & Capacity Planning
```

This approach can help management make more informed decisions regarding **bed capacity, staffing, workload distribution, and resource allocation**.

---

# 🚀 Future Enhancements

Potential future improvements include:

* 🔮 Bed occupancy forecasting.
* 👨‍⚕️ Doctor workload forecasting.
* 📈 Predictive resource-demand analysis.
* 🚨 Automated capacity-pressure alerts.
* 🛏️ Dynamic bed-capacity recommendations.
* 👥 Staff requirement forecasting.
* 🤖 Machine Learning-based resource optimization.
* 📊 Real-time hospital resource monitoring.
* 🔄 Automated resource allocation recommendations.

---

# 🧠 Key Takeaway

> **Resource utilization should not be evaluated using a single metric.**

By combining **bed utilization, patient workload, departmental capacity, and operational benchmarks**, the module provides a more comprehensive understanding of where hospital resources may be under pressure.

The result is a shift from:

**"How much are our resources being used?"**

to:

**"Where is resource pressure occurring, what may be causing it, and where should management focus?"**

---

# 👩‍💻 Project Focus

This milestone demonstrates practical application of:

**Healthcare Analytics • Resource Utilization • Capacity Intelligence • Power BI • DAX • Data Visualization • KPI Development • Operational Benchmarking • Capacity Planning • Business Intelligence**

---

## ⭐ Conclusion

Milestone 3 transforms hospital operational data into a **Resource Utilization & Capacity Intelligence solution**.

By combining **bed utilization, doctor workload, departmental capacity, and operational benchmarks**, the dashboard provides management with a structured way to identify potential pressure areas and support better resource planning.

> **Turning hospital resource data into capacity intelligence for smarter operational planning.** 🏥📊


## 📍 Milestone 4 — Geographical Analysis & Final Executive Dashboard

### 🎯 Objective

The objective of **Milestone 4** was to extend the hospital analytics solution with **geographical demand analysis** and integrate the key insights generated across the previous milestones into a comprehensive **executive-level Power BI dashboard**.

This milestone focuses on understanding the geographical distribution of patient demand, identifying high-demand regions, and presenting critical hospital performance and resource utilization insights from a management perspective.

---

### 🌍 Geographical Analysis

The available geographical attributes in the healthcare dataset were used to analyze patient demand across different locations.

Since the dataset contains **City** and **State** information but does not include latitude/longitude or district-level geographical data, the geographical analysis was performed at the **city and state levels**.

This approach enables the identification of major geographical patterns in patient demand while remaining consistent with the available dataset.

---

### ❓ Key Business Questions

The geographical analysis was designed to answer the following business questions:

- Which states have the highest patient demand?
- Which cities contribute the highest patient volume?
- How is patient demand distributed across different states?
- Which regions may require greater healthcare resources?
- What are the major geographical patterns in patient demand?
- How does geographical demand relate to available hospital capacity?

---

### 📊 Geographical Dashboard Components

The **Geographical Analysis** page includes the following visualizations and analytical components:

| Dashboard Component | Purpose |
|---|---|
| **Patient Volume by State** | Identifies states contributing the highest number of patients. |
| **Top 10 Cities by Patient Volume** | Highlights cities with the highest patient demand. |
| **Bed Type Demand by State** | Compares demand for different bed types across high-demand states. |
| **Gender Distribution by State** | Provides demographic distribution across major states. |
| **Geographical Demand Analysis** | Provides a location-based view of patient demand using available city and state information. |
| **Interactive Filters** | Enables users to explore geographical patterns using State, Year, and Gender filters. |

---

### 🏥 Final Executive Dashboard Integration

The final dashboard integrates the important analyses developed throughout the previous milestones into a **unified Power BI solution** rather than treating each milestone as an independent output.

The integrated dashboard brings together:

- Patient demand and admission analysis
- Treatment and service demand
- Hospital resource utilization
- Bed utilization
- Workforce deployment
- Patients per doctor
- Capacity and overload analysis
- Geographical patient demand
- Key operational KPIs

This integrated approach provides a consolidated view of hospital operations and enables management to analyze demand, capacity, and resource utilization together.

---

### 💡 Executive-Level Insights

The final dashboard enables hospital management to quickly identify:

- High-demand states and cities
- Departments experiencing higher resource pressure
- Bed utilization levels across departments
- Departments with higher patient-to-doctor workload
- Potential areas requiring additional resources
- Geographic concentration of patient demand
- Differences between patient demand and available operational capacity
- Areas with potential capacity or resource constraints

These insights can support data-driven understanding of hospital performance and help identify areas requiring further operational attention.

---

### 🎨 Dashboard Design

The final Power BI report was designed from an **executive and management perspective**, with emphasis on clarity, usability, and prioritization of important insights.

Key design principles include:

- Clear and meaningful KPI cards
- Business-focused visualizations
- Interactive slicers and filters
- Geographical analysis
- Resource utilization indicators
- Capacity and overload analysis
- Consistent dashboard navigation
- Logical organization of information
- Reduced visual clutter
- Prioritization of high-value business insights

---

### ✅ Dashboard Validation

The final Power BI dashboard was validated to ensure the accuracy, consistency, and usability of the analytical outputs.

The following validation checks were performed:

- KPI calculations produce correct results.
- Filters interact correctly with the relevant visuals.
- Date and geographical filters work as expected.
- Visualizations accurately represent the underlying dataset.
- Resource utilization and capacity metrics remain consistent.
- Dashboard interactions function as intended.
- Key insights are understandable from a hospital management perspective.

---

## 🏆 Milestone 4 Outcome

Milestone 4 completes the hospital analytics solution by integrating **patient demand, clinical and service utilization, resource utilization, capacity intelligence, and geographical analysis** into a unified **Power BI executive dashboard**.

The final dashboard provides a management-oriented view of hospital operations and enables stakeholders to:

- Understand geographical patterns in patient demand
- Identify high-demand states and cities
- Monitor hospital resource utilization
- Evaluate bed and workforce pressure
- Identify potential capacity constraints
- Compare demand with available operational resources
- Support data-driven operational decision-making

  ## Live Dashboard

[View Healthcare Operations Dashboard](https://medical-operations-dashboardgit-me5eunufwuk9efvkjkmrmz.streamlit.app/)

### 📌 Final Outcome

The completion of Milestone 4 represents the transition from individual analytical modules to a **comprehensive hospital operations intelligence solution**, bringing together data-driven insights across **demand, resources, capacity, workforce, financial performance, and geography**.

---

Copyright (c) 2026 Devashri Pavle

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in
all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN
THE SOFTWARE.
