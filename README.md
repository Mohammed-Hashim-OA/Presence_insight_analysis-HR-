👨‍💼 HR Presence Insights Dashboard

A comprehensive Human Resources Analytics project developed using **Power BI** to analyze employee attendance, work-from-home patterns, leave trends, and overall workforce presence.

The project transforms raw attendance sheets into an interactive dashboard that helps HR teams monitor workforce behavior and make data-driven decisions.

-----------------------------------------------------------------------------------------------------------------------------------

🚀 Project Overview

Organizations often struggle to track employee attendance efficiently when attendance records are maintained in multiple monthly sheets.

This project solves that challenge by:

- Consolidating attendance data from multiple months
- Transforming complex spreadsheet structures
- Automating data preparation using Power Query Functions
- Creating meaningful HR KPIs
- Building an interactive dashboard for workforce monitoring

----------------------------------------------------------------------------------------------------------------------------------------

🎯 Business Problem

The attendance data was stored across multiple Excel sheets:

- April 2022
- May 2022
- June 2022

Each date existed as a separate column, making analysis difficult.

Example:

| Employee   | 1-Apr  | 2-Apr  | 3-Apr  | 4-Apr  |
|------------|--------|--------|--------|--------|
| Employee A | P      | WO     | WO     | P      |

This structure is not suitable for reporting and dashboard development.

--------------------------------------------------------------------------------------------------------

🛠 Tools & Technologies Used

| Tool            | Purpose                        |
|-----------------|--------------------------------|
| Power BI        | Dashboard Development          |
| Power Query     | Data Cleaning & Transformation |
| DAX             | KPI & Measure Creation         |
| Microsoft Excel | Data Source                    |
| Data Modeling   | Analytical Reporting           |

--------------------------------------------------------------------------------------------------------------------------

📂 Dataset Information

The dataset consists of:

Attendance Sheets
- April 2022
- May 2022
- June 2022

Attendance Key
Contains definitions for attendance statuses.

Examples:

| Code   | Meaning        |
|--------|----------------|
| P      | Present        |
| WO     | Weekly Off     |
| WFH    | Work From Home |
| SL     | Sick Leave     |
| PL     | Paid Leave     |
| HPL    | Half Pay Leave |

-----------------------------------------------------------------------------------------------------------------

🧹 Data Cleaning & Transformation

The raw dataset required significant transformation before analysis.

Step 1: Process a Single Monthly Sheet

The transformation process was first created on one sheet.

- Operations Performed

✔ Removed unnecessary rows

✔ Promoted first row as headers

✔ Renamed columns

✔ Corrected data types

✔ Retained Employee Code and Employee Name

✔ Converted date columns into rows using Unpivot


- Before Transformation
Employee | 1-Apr | 2-Apr | 3-Apr | 4-Apr


- After Transformation
Employee Code | Name | Date | Value

This structure is more suitable for analysis and reporting.


Step 2: Create a Reusable Function

Instead of repeating the same transformation process for all sheets:

- A Power Query Function was created
- The function automated the cleaning process
- The function was invoked across all monthly sheets

Benefits

- Reduced manual effort
- Improved scalability
- Ensured consistency across months



Step 3: Apply Function to All Sheets

The custom function was applied to:

- April 2022
- May 2022
- June 2022

The transformed outputs were combined into a single consolidated table.


Step 4: Merge Monthly Data

All transformed sheets were appended into one final dataset.

Final Structure:

| Sheet Name | Employee Code | Name | Date | Value |
|------------|---------------|-------|-------|--------|

This created a clean attendance fact table for reporting.


📊 Data Model

A centralized attendance table was used for analysis.

### Key Columns


Sheet Name
Employee Code
Employee Name
Date
Attendance Status

This structure enabled efficient DAX calculations and dashboard performance.



📐 DAX Measures Created

Several measures were created to calculate workforce metrics.

- Presence %
Presence % = DIVIDE([Present Days],[Total Working Days])



WFH %
WFH % =DIVIDE([WFH Count],[Total Working Days])


- Sick Leave %
SL % =DIVIDE( [SL Count] [Total Working Days])



📊 Dashboard Features

1️⃣ Month Slicer

Interactive filtering across:

- April
- May
- June

Allows HR teams to analyze attendance trends month-wise.


2️⃣ KPI Cards

Key workforce indicators displayed at a glance.

Metrics

- Total Working Days
- Presence Percentage
- Sick Leave Percentage
- Work From Home Percentage

Results


Total Working Days : 4K Presence % : 91.55%
SL % : 1.08%
WFH % : 11.15%




3️⃣ Employee Attendance Analysis

Visual representation of:

- Present Days
- Work From Home Days
- Sick Leave Days

for each employee.


Business Value

- Identify attendance behavior
- Monitor workforce productivity
- Detect unusual absence patterns



4️⃣ Attendance Status Distribution

Displays frequency of:

- Present
- Work From Home
- Sick Leave
- Paid Leave
- Half Pay Leave
- Weekly Off



Business Value

- Understand workforce attendance patterns
- Evaluate leave utilization



5️⃣ Presence Trend Analysis

Tracks daily workforce presence percentage over time.

Business Value

- Identify attendance fluctuations
- Monitor employee engagement
- Detect seasonal attendance changes



6️⃣ Attendance Matrix

Detailed employee attendance tracker.

Displays attendance status for:

- Every employee
- Every day

Using conditional formatting for easier visualization.

Business Value

- Employee-level attendance monitoring
- Quick identification of leave patterns



📈 Key Business Insights

Workforce Attendance

- Overall employee presence remains above 90%.

Remote Work Adoption

- Employees utilized Work From Home options regularly.

Leave Trends

- Sick leave percentage remains low, indicating healthy workforce attendance.

Attendance Monitoring

- Daily tracking enables HR teams to identify attendance anomalies quickly.

--------------------------------------------------------------------------------------------------------------------------------


🎯 Skills Demonstrated

- Data Cleaning
- Data Transformation
- Power Query
- Data Modeling
- Unpivoting Data
- Function Creation in Power Query
- DAX Calculations
- Power BI Dashboard Development
- HR Analytics
- Data Visualization
- Business Intelligence



💡 Future Improvements

- Employee Attrition Analysis
- Department-Level Attendance Tracking
- Attendance Forecasting
- Automated Alerts for Low Presence
- HR Performance Dashboard Integration

-----------------------------------------------------------------------------------------------------------------------------------

👨‍💻 Author

Mohammed Hashim O A

Aspiring Data Analyst | Power BI Developer | SQL Enthusiast

Skills

- Power BI
- SQL
- Python
- Excel
- Data Visualization
- Data Analytics
- Business Intelligence

Connect With Me

- LinkedIn: https://www.linkedin.com/in/mohammed--hashim
- GitHub: https://github.com/Mohammed-Hashim-OA

-----------------------------------------------------------------------------------------------------------------------

⭐ Support

If you found this project useful, please consider giving it a star on GitHub.

Project Outcome

This project successfully transformed raw attendance records into a scalable HR Analytics solution, enabling better workforce monitoring, attendance tracking, and data-driven HR decision-making through interactive Power BI visualizations.
