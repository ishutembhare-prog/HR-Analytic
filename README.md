# HR-Analytic

📌 HR Analytics — Employee Attrition Dashboard (Power BI Project)

🔍 Project Overview
This project focuses on analyzing employee attrition to help HR departments understand why employees leave, which employee segments are most at risk, and what factors influence turnover.
Using Power BI, the dashboard provides actionable insights to support employee retention strategies and workforce planning.

🎯 Business Objectives
1. Identify key factors contributing to employee attrition
2. Analyze attrition by department, job role, salary, age group, work-life balance, overtime, and satisfaction metrics
3. Enable HR teams to predict and prevent employee churn
4. Reduce hiring and training cost through data-driven decision making

🗂️ Project Files in Repository
File Name	Description
HR_Analytics.csv	Raw dataset used for dashboard
HR ANALYSIS DASHBORD.pbit	Power BI dashboard template
Dashboard_Screenshot.png	Snapshot of final dashboard
README.md	Project documentation (this file)

📊 KPIs & Metrics Displayed in Dashboard
KPI	Description
Total Employees	Count of active employees
Attrition Count	Number of employees who left the company
Attrition Rate	Percentage of employees who left
Avg Monthly Income	Average salary of employees
Avg Job Satisfaction Score	Mean satisfaction level
Tenure Distribution	Years spent in the company
Overtime Impact	Attrition among overtime workers


🖥 Power BI Dashboard Visuals
Visual Type	Business Insight
KPI Cards	Overall workforce metrics
Donut Chart	Attrition rate
Bar Chart	Attrition by Department
Clustered Bar	Attrition by Job Role
Line Chart	Attrition by Age Group
Heatmap	Job Satisfaction vs Attrition
Histogram	Monthly Income vs Attrition
Slicers	Department, Gender, Job Role, Age Group, Overtime


🔑 Key Insights
📌 Employees with Overtime are 2× more likely to leave
📌 Highest attrition is observed in age group 26–35
📌 Sales and R&D departments face maximum employee exits
📌 Lower salary hike + low job satisfaction strongly drive attrition
📌 Employees with <2 years tenure are at highest churn risk


🧮 DAX Measures Used
Total Employees = COUNT(Employee_Data[Employee ID])
Attrition Count = CALCULATE(COUNT(Employee_Data[Employee ID]), Employee_Data[Attrition] = "Yes")
Attrition Rate = DIVIDE([Attrition Count],[Total Employees],0)
Avg Salary = AVERAGE(Employee_Data[Monthly Income])
Avg Job Satisfaction = AVERAGE(Employee_Data[Job Satisfaction])
Overtime Attrition = CALCULATE([Attrition Count], Employee_Data[OverTime] = "Yes")

🧾 Dataset — Data Dictionary
Column Name	Description
Employee ID	Unique ID assigned to each employee
Age	Age of employee
Gender	Male / Female
Department	Department of employment (HR / Sales / R&D / etc.)
Job Role	Specific job position
Business Travel	Frequency of official travel
Education	Education level (1–5)
Education Field	Academic field
Monthly Income	Employee salary
Percent Salary Hike	Latest salary increase percentage
Total Working Years	Total industry experience
Years at Company	Tenure at current company
Years in Current Role	Tenure in current role
Years Since Last Promotion	Time since previous promotion
Job Satisfaction	Job satisfaction score (1–4)
Work-Life Balance	Rating of balance between job and personal life
Environment Satisfaction	Workplace environment rating
Performance Rating	Performance evaluation score
Overtime	Yes / No (working extra hours)
Distance from Home	Daily commute distance
Attrition	Yes / No (target variable)


📁 Repository Folder Structure
/HR-Analytic
│── HR_Analytics.csv
│── HR ANALYSIS DASHBORD.pbit
│── Dashboard_Screenshot.png
└── README.md

🚀 Future Enhancements

🔹 Employee attrition prediction using ML model
🔹 Power BI online publishing for public dashboard link
🔹 Integration of HRMS live data using API or SQL server
