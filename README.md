📊 HR Analytics Dashboard — Power BI

An interactive Power BI dashboard built to analyze employee attrition patterns and workforce demographics. The dashboard provides insights into employee turnover, job satisfaction, age distribution, and education backgrounds to support data-driven HR decisions.

📊 Key Performance Indicators (KPIs)
KPI	Description
Total Employees	Total number of employees in the organization
Active Employees	Employees currently working in the company
Attrition Count	Number of employees who left the organization
Attrition Rate	Percentage of employees who left
Average Age	Average age of employees
🗂️ Repository Structure
HR-Analytics-Dashboard/
│
├── 📁 assets/                          # Dashboard screenshots
│   └── dashboard_overview.png
│
├── 📁 data/
│   └── HR_Analytics.csv                # Raw dataset (if shareable)
│
├── 📁 docs/
│   └── DAX_Measures.md                 # DAX measures used in the project
│
├── HR_Analytics_Dashboard.pbix         # Power BI report file
├── .gitignore
└── README.md
📁 Dataset

The dataset contains employee-related information used to analyze workforce trends and attrition.

Key Columns
Column	Description
Age	Employee age
Attrition	Indicates whether an employee left the company
Department	Employee department
Gender	Employee gender
EducationField	Educational background
JobRole	Employee designation
JobSatisfaction	Satisfaction rating (1–4)
MonthlyIncome	Monthly salary
YearsAtCompany	Years spent in the organization
🛠️ Tools & Technologies
Tool	Purpose
Power BI Desktop	Dashboard development
Power Query	Data cleaning and transformation
DAX	KPI calculations and measures
Data Modeling	Relationship management
Excel / CSV	Source dataset
📐 Dashboard Components
KPI Cards
Total Employees
Active Employees
Attrition Count
Attrition Rate
Average Age
Attrition by Department
Horizontal bar chart showing employee turnover across departments.
Employee Distribution by Age
Stacked column chart representing workforce distribution by age group and gender.
Job Satisfaction Matrix
Matrix visual displaying satisfaction ratings across different job roles.
Attrition by Education Field
Column chart highlighting attrition across educational backgrounds.
Attrition Rate by Gender Across Age Groups
Donut charts comparing attrition patterns between male and female employees.
⚙️ Setup & How to Run
Prerequisites
Power BI Desktop
Dataset file (HR_Analytics.csv)
Steps
Clone the repository
git clone https://github.com/your-username/HR-Analytics-Dashboard.git
cd HR-Analytics-Dashboard
Open the Power BI report
File → Open Report → HR_Analytics_Dashboard.pbix
Reconnect the data source (if required)
Home → Transform Data → Data Source Settings
Refresh the report and interact with the dashboard.
🧮 DAX Measures
Employee Count =
COUNT(Employee[EmployeeNumber])

Attrition Count =
CALCULATE(
    [Employee Count],
    Employee[Attrition] = "Yes"
)

Attrition Rate =
DIVIDE([Attrition Count],[Employee Count],0)

Active Employees =
[Employee Count] - [Attrition Count]

Average Age =
AVERAGE(Employee[Age])
🔍 Key Insights

📌 Research & Development department experienced the highest attrition.

📌 Employees aged 25–34 formed the largest workforce segment.

📌 Life Sciences and Medical backgrounds showed relatively higher attrition.

📌 Job satisfaction varied significantly across job roles.

📌 Overall employee attrition rate stood at 16.12%.

🎯 Business Objective

The objective of this project is to understand employee attrition patterns and transform HR data into actionable insights that help organizations improve employee retention and workforce planning.

📷 Dashboard Preview
📄 License

This project is licensed under the MIT License.

🙏 Acknowledgements

Dataset sourced from the IBM HR Analytics Employee Attrition dataset, widely used for business intelligence and analytics practice.

Built with ❤️ using Microsoft Power BI.
