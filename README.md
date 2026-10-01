# 📊 Grade 11 Subject Performance Analysis | Power BI

> **Interactive Business Intelligence Dashboard | Education Analytics | Power BI & DAX**

---

## **📌 Project Overview**

This project presents an **interactive Power BI dashboard designed to analyse Grade 11 academic performance across schools, circuits, districts, subjects, and academic terms.**

The project demonstrates an end-to-end **Business Intelligence workflow**, starting with raw Excel data and progressing through **data cleaning, preparation, analysis, DAX measure development, visualisation, and interactive dashboard design.**

The dashboard transforms raw academic results into meaningful visual insights that can be used to understand performance patterns and identify areas requiring further attention.

---

## **🎯 Project Objective**

The main objective was to develop a professional and interactive dashboard capable of answering important performance-related questions, including:

* **How does academic performance differ across districts?**
* **Which subjects have the highest and lowest average performance?**
* **How does performance change across academic terms?**
* **Which schools or subjects require further attention?**
* **What proportion of results meet the 50% pass threshold?**
* **What is the performance gap between the highest and lowest results?**

---

# **🗂️ Dataset**

The analysis was conducted using a Grade 11 school performance dataset for **2025**.

### **Key Data Fields**

| Field          | Description           |
| -------------- | --------------------- |
| **District**   | Education district    |
| **Circuit**    | Education circuit     |
| **SchoolName** | Name of the school    |
| **Subject**    | Academic subject      |
| **Term**       | Academic term         |
| **Marks**      | Marks obtained        |
| **TotalMarks** | Total available marks |
| **Percentage** | Percentage achieved   |

The dataset was originally provided in **Microsoft Excel** and imported into Power BI for preparation and analysis.

---

# **🧹 1. Data Cleaning & Preparation**

Before developing the dashboard, the raw dataset was reviewed and prepared for analysis.

### **Data preparation included:**

* Reviewing and standardising column names
* Checking data types
* Identifying potential duplicate records
* Checking for missing or inconsistent values
* Ensuring numerical fields were correctly recognised
* Validating percentage and marks fields
* Reviewing categorical fields such as district, circuit, school and subject
* Preparing the dataset for Power BI visualisations and calculations

This stage was important because **accurate analysis depends on clean and consistently structured data.**

---

# **📐 2. Data Analysis & DAX**

To make the dashboard interactive and dynamic, **DAX (Data Analysis Expressions)** was used to create custom measures.

### **Average Percentage**

```DAX
Average_Percentage = AVERAGE(Sheet2[Percentage])
```

Calculates the average percentage across the selected records.

---

### **Pass Rate**

```DAX
Pass_Rate =
DIVIDE(
    CALCULATE(
        COUNTROWS(Sheet2),
        Sheet2[Percentage] >= 50
    ),
    COUNTROWS(Sheet2),
    0
)
```

Calculates the proportion of results achieving **50% or above**.

---

### **Performance Gap**

```DAX
Performance_Gap =
MAX(Sheet2[Percentage]) - MIN(Sheet2[Percentage])
```

Measures the difference between the highest and lowest percentage within the selected data.

---

### **Total Marks Obtained**

```DAX
Total_Marks_Obtained = SUM(Sheet2[Marks])
```

Calculates the total marks obtained across the selected records.

---

# **📊 3. Dashboard Development**

The final Power BI report was structured into **three interactive dashboard pages**, each focusing on a different level of academic performance.

---

## **🏫 Page 1 — District Performance Overview**

The District Overview page provides a high-level view of academic performance across different districts.

### **Visualisations include:**

* **Average Percentage by District**
* **School Distribution by District**
* **Performance KPIs**
* **Interactive filtering**

The page allows users to compare districts and quickly identify differences in overall academic performance.

---

## **📚 Page 2 — Subject Performance Analysis**

The Subject Insights page focuses on understanding performance across different academic subjects.

### **Visualisations include:**

* **Average Marks by Subject**
* **Performance Trends by Term**
* **Subject Contribution to Total Marks**
* **Subject-level comparisons**

This page allows users to investigate how subjects perform relative to one another and how performance changes across academic terms.

---

## **🏢 Page 3 — School-Level Performance**

The School Comparison page provides a more detailed view of individual school and subject performance.

### **The analysis includes:**

* School
* Subject
* Marks
* Percentage
* Performance comparison
* Conditional formatting

Results below **40%** are highlighted to make lower-performing areas easier to identify.

---

# **🎛️ 4. Interactive Dashboard Features**

To make the dashboard dynamic and user-friendly, interactive slicers were incorporated.

### **Available Filters**

* **District**
* **Circuit**
* **Term**
* **Subject**

Users can select different combinations of filters and immediately see how the dashboard changes.

For example, selecting a specific district allows the user to investigate the performance of schools and subjects within that district.

---

# **📈 5. Visualisation Techniques**

Different visualisation types were selected according to the analytical question being addressed.

| Visual           | Purpose                                     |
| ---------------- | ------------------------------------------- |
| **Bar Chart**    | Compare average percentage across districts |
| **Column Chart** | Compare average marks by subject            |
| **Line Chart**   | Analyse performance trends across terms     |
| **Donut Chart**  | Show subject contribution to total marks    |
| **Map**          | Visualise school distribution by district   |
| **Table**        | Examine detailed school and subject results |
| **KPI Cards**    | Present important performance indicators    |

The combination of these visualisations allows users to move from **high-level performance summaries to detailed school-level analysis.**

---

# **🔢 6. Key Performance Indicators**

The dashboard uses KPI cards to provide a quick overview of important performance measures.

### **Key indicators include:**

* **Average Percentage**
* **Pass Rate**
* **Total Marks Obtained**
* **Performance Gap**
* **Best-performing District**
* **Lowest-performing Subject**

These indicators provide a summary of the dataset before users explore the detailed visualisations.

---

# **🧭 7. Dashboard Navigation**

Navigation buttons were implemented to provide a structured user experience.

### **Dashboard Navigation**

**District Overview → Subject Insights → School Comparison**

This allows users to move easily between different levels of analysis while maintaining a consistent dashboard experience.

---

# **🔎 8. Analytical Insights**

The dashboard can be used to investigate patterns such as:

* Differences in academic performance between districts
* Variation in performance between subjects
* Changes in performance across academic terms
* Schools with lower-performing subjects
* Overall pass rates
* Differences between the highest and lowest results

The interactive nature of the dashboard allows these patterns to be explored dynamically by applying different filters.

---

# **🛠️ 9. Tools & Technologies**

### **Business Intelligence**

* **Microsoft Power BI**

### **Data Analysis**

* **DAX**
* **Microsoft Excel**

### **Data Skills**

* Data Cleaning
* Data Preparation
* Data Analysis
* Data Visualisation
* KPI Development
* Interactive Dashboard Design

---

# **📁 10. Project Structure**

```text
PowerBI-Grade11-Subject-Performance-Analysis/
│
├── README.md
├── TOOLS.md
├── .gitignore
│
├── data/
│   └── Gr11SubjectSch2025.xlsx
│
├── dashboard/
│   └── Grade11_Subject_Performance.pbix
│
└── screenshots/
    ├── 01-district-overview.png
    ├── 02-subject-insights.png
    └── 03-school-comparison.png
```

---

# **💡 Skills Demonstrated**

This project demonstrates practical skills in:

**Data Preparation**
Cleaning, validating and preparing structured data for analysis.

**Data Analysis**
Analysing performance across multiple dimensions including district, school, subject and term.

**DAX**
Creating calculated measures using functions such as `AVERAGE`, `SUM`, `COUNTROWS`, `CALCULATE`, `DIVIDE`, `MAX` and `MIN`.

**Data Visualisation**
Selecting appropriate visualisations to communicate different analytical findings.

**Business Intelligence**
Transforming raw data into an interactive dashboard that supports data-driven analysis.

**Dashboard Design**
Creating a structured, interactive and user-friendly reporting environment.

---

# **🚀 Portfolio Value**

This project forms part of my broader **Data Science and Business Intelligence portfolio** and demonstrates my ability to move from **raw data to an interactive analytical solution.**

It complements my other projects involving:

* **Python**
* **R**
* **SQL**
* **Machine Learning**
* **Statistical Analysis**
* **Power BI**

Together, these projects demonstrate my growing ability to work across different stages of the **data analytics lifecycle**.

---

# **👤 Author**

### **Andile Brian Sithole**

**Data Science Graduate | Data Analytics | Business Intelligence**

🔗 **GitHub:**
https://github.com/andilebrian672-bit

🔗 **LinkedIn:**
https://www.linkedin.com/in/andile-brian-sithole-696994237/

---

## **📌 Project Status**

**Completed | Portfolio Project**

The GitHub repository will be updated as additional analysis, dashboard improvements and documentation are added.
