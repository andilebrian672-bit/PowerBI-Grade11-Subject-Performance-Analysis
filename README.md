Project Overview

This project presents an interactive Power BI dashboard for analysing Grade 11 subject performance across schools, circuits and districts.

The objective was to transform raw school assessment data into an interactive business intelligence dashboard that allows users to identify performance patterns, compare districts and subjects, and investigate school-level results.

The project demonstrates a complete Power BI workflow, including:

Data import and cleaning
Data preparation
Data validation
Data visualisation
DAX measure creation
KPI development
Interactive filtering
Dashboard design
Performance analysis
Dataset

The dataset contains Grade 11 subject performance information for schools during 2025.

Key fields include:

Column	Description
District	Education district
Circuit	Education circuit
SchoolName	Name of the school
Subject	Subject being analysed
Marks	Marks obtained
TotalMarks	Total available marks
Percentage	Percentage achieved
Term	Academic term

The dataset was imported into Power BI from an Excel workbook.

1. Data Import and Cleaning

The first stage of the project involved importing the Excel dataset into Power BI Desktop.

After importing the data, the columns were reviewed to ensure that the dataset was correctly structured and suitable for analysis.

Data cleaning steps

The following checks and transformations were performed:

Reviewed column names and renamed fields where necessary.
Checked the data types of numerical and categorical columns.
Verified that marks and percentages were stored as numerical values.
Checked for duplicate records.
Checked for missing or inconsistent values.
Reviewed school, district, circuit and subject names for consistency.
Ensured that the dataset was structured correctly for visualisation and analysis.

The purpose of this stage was to ensure that the dashboard was based on reliable and consistently structured data.

2. Data Preparation

After cleaning the dataset, the data was prepared for analysis.

The main analytical fields used in the dashboard were:

District
Circuit
SchoolName
Subject
Term
Marks
TotalMarks
Percentage

These fields allowed the dashboard to analyse performance at different levels, from overall district performance down to individual schools and subjects.

3. DAX Measures

DAX was used to create calculated measures that provide dynamic performance indicators.

Average Percentage
Average_Percentage = AVERAGE(Sheet2[Percentage])

This measure calculates the average percentage across the selected data.

It responds dynamically to filters such as District, Circuit, Term and Subject.

Pass Rate
Pass_Rate =
DIVIDE(
    CALCULATE(
        COUNTROWS(Sheet2),
        Sheet2[Percentage] >= 50
    ),
    COUNTROWS(Sheet2),
    0
)

This measure calculates the percentage of records where the learner achieved at least 50%.

It provides an overall view of the proportion of results meeting the defined pass threshold.

Performance Gap
Performance_Gap =
MAX(Sheet2[Percentage]) - MIN(Sheet2[Percentage])

This measure calculates the difference between the highest and lowest percentage in the selected data.

It can be used to understand the spread of performance.

Total Marks Obtained
Total_Marks_Obtained = SUM(Sheet2[Marks])

This measure calculates the total marks obtained across the selected records.

4. Dashboard Design

The dashboard was designed as an interactive multi-page Power BI report.

The report contains three main analytical sections:

Page 1 — District Overview

The District Overview page provides a high-level view of academic performance across districts.

Visualisations include:

Average Percentage by District
Distribution of schools by District
KPI cards
Interactive filters

The page allows users to compare district-level performance and identify differences between districts.

Page 2 — Subject Insights

The Subject Insights page focuses on performance across different subjects.

Visualisations include:

Average Marks by Subject
Performance trends by Term
Subject contribution to total marks
Subject-level comparisons

This page allows users to investigate which subjects have higher or lower average performance and how performance changes across terms.

Page 3 — School Comparison

The School Comparison page provides more detailed school-level analysis.

The dashboard includes:

School
Subject
Marks
Percentage
Conditional formatting
Performance comparisons

Conditional formatting is used to highlight results below 40%, making lower-performing areas easier to identify.

5. Interactive Slicers

Interactive slicers were added to allow users to dynamically filter the dashboard.

The main slicers include:

District
Circuit
Term
Subject

For example, selecting a particular district updates the dashboard visuals to display information related only to that district.

This allows users to move from an overall view to a more detailed analysis without changing the underlying dataset.

6. Key Performance Indicators

KPI cards were used to present important performance indicators at a glance.

The dashboard focuses on:

Average Percentage
Pass Rate
Total Marks Obtained
Performance Gap
Best-performing district
Lowest-performing subject

These indicators provide a quick summary before users explore the detailed visualisations.

7. Visualisations

The dashboard uses multiple Power BI visualisation types to communicate different aspects of the data.

Bar Chart

Used to compare average percentage across districts.

Column Chart

Used to compare average marks across subjects.

Line Chart

Used to analyse performance trends across academic terms.

Donut Chart

Used to show the contribution of subjects to total marks.

Map

Used to visualise the distribution of schools across districts.

Table

Used to provide detailed school and subject-level results.

KPI Cards

Used to communicate key performance indicators.

8. Dashboard Navigation

Navigation buttons were incorporated into the report to allow users to move between the main dashboard sections:

District Overview → Subject Insights → School Comparison

This creates a more user-friendly dashboard experience and allows users to navigate between different levels of analysis.

9. Key Analytical Questions

The dashboard was designed to help answer questions such as:

Which districts have the highest average performance?
Which subjects have the highest average marks?
How does performance change between terms?
Which schools have lower-performing subjects?
What percentage of results meet the 50% pass threshold?
How large is the performance gap between the highest and lowest results?
How does performance change when filtering by district, circuit or subject?
10. Business Intelligence Skills Demonstrated

This project demonstrates practical experience in:

Power BI

Dashboard development
Interactive reporting
Data visualisation
KPI development
Dashboard navigation

DAX

AVERAGE
SUM
COUNTROWS
CALCULATE
DIVIDE
MAX
MIN

Data Preparation

Data cleaning
Data validation
Data type management
Duplicate checking

Data Analysis

Performance comparison
Trend analysis
KPI analysis
Filtering and segmentation
11. Tools Used
Power BI Desktop
DAX
Microsoft Excel
12. Project Structure
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
    ├── district-overview.png
    ├── subject-insights.png
    └── school-comparison.png
13. Portfolio Purpose

This project was developed as part of my Data Science and Business Intelligence learning journey.

It demonstrates my ability to take a structured dataset, prepare it for analysis, develop analytical measures using DAX, and communicate findings through an interactive Power BI dashboard.

The project forms part of my broader data portfolio, alongside projects involving Python, R, SQL, machine learning and statistical analysis.

Author

Andile Brian Sithole

Data Science Graduate
