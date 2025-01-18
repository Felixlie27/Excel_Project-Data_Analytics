# Excel Salary Dashboard

![1_Salary_Dashboard_Final_Dashboard](https://github.com/user-attachments/assets/bedd5b22-78c4-44b7-b4e6-97c88b2e9435)

## Introduction

This salary dashboard project is my first Excel project that I created after learning from [Luke Barousse's](https://github.com/lukebarousse) YouTube Excel course. 

The dashboard is designed to help job seekers explore salary information for various data-related job titles. It provides insights into salaries based on job roles, locations, and required skills.

### Dashboard File
ou can download my final dashboard here: [1_Salary_Dashboard.xlsx](https://github.com/user-attachments/files/18461952/1_Salary_Dashboard.xlsx).

### Excel Skills Used

Here are the key Excel skills I used while creating the dashboard:

- **📉 Charts**: Creating different charts to visualize salary data.
- **🧮 Formulas and Functions**: Using formulas like `MEDIAN()`, `IF()`, `FILTER()`, and more.
- **❎ Data Validation**: Ensuring the data input is correct using validation rules.

### Data Jobs Dataset

The dataset I used for this project contains real-world salary information from 2023 for data science-related jobs. It includes:

- **👨‍💼 Job titles**
- **💰 Salaries**
- **📍 Locations**
- **🛠️ Skills**

## Dashboard Build

### 📉 Charts

#### 📊 Data Science Job Salaries - Bar Chart

<img src="https://github.com/user-attachments/assets/f392411a-98d7-4410-ad65-6c4d5c6083c9" alt="Salary Dashboard Chart1" width="850" height="550">

- I used a **horizontal bar chart** to compare salaries for different job titles. 
- The chart helps to quickly see which roles, like Senior positions, pay more than Analyst roles.

#### 🗺️ Country Median Salaries - Map Chart

![1_Salary_Dashboard_Country_Map](https://github.com/user-attachments/assets/8fddaea7-c9cb-46de-b872-bd78417b724a)

- I created a **map chart** to show how median salaries differ across different countries.
- The map is color-coded to help easily spot regions with high or low salaries.

### 🧮 Formulas and Functions

#### 💰 Median Salary by Job Titles

```
=MEDIAN(
IF(
    (jobs[job_title_short]=A2)*
    (jobs[job_country]=country)*
    (ISNUMBER(SEARCH(type,jobs[job_schedule_type])))*
    (jobs[salary_year_avg]<>0),
    jobs[salary_year_avg]
)
)
```

- 🔍 **Multi-Criteria Filtering:** Checks job title, country, schedule type, and excludes blank salaries.
- 📊 **Array Formula:** Utilizes `MEDIAN()` function with nested `IF()` statement to analyze an array.
- 🎯 **Tailored Insights:** Provides specific salary information for job titles, regions, and schedule types.
- **🔢 Formula Purpose:** This formula populates the table below, returning the median salary based on job title, country, and type specified.

🍽️ Background Table

![1_Salary_Dashboard_Screenshot1](https://github.com/user-attachments/assets/a3fdfed5-4c96-4576-a408-cd87b2488a87)

📉 Dashboard Implementation

<img src="https://github.com/user-attachments/assets/0f2cfb40-61d9-4191-b883-a2c337ab64d8" alt="Salary Dashboard Title" width="400" height="500">

#### ⏰ Count of Job Schedule Type

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- 🔍 **Unique List Generation:** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
- **🔢 Formula Purpose:** This formula populates the table below, which gives us a list of unique job schedule types.

🍽️ Background Table

![1_Salary_Dashboard_Screenshot2](https://github.com/user-attachments/assets/a786c05a-59e5-4505-a290-b664d98c1f85)

📉 Dashboard Implementation:

<img src="https://github.com/user-attachments/assets/27347028-cbef-4823-8559-84d29acf7459" alt="Salary Dashboard Type" width="350" height="500">

### ❎ Data Validation

#### 🔍 Filtered List

- 🔒 **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job Title`, `Country`, and `Type` option in the Data tab ensures:
    - 🎯 User input is restricted to predefined, validated schedule types
    - 🚫 Incorrect or inconsistent entries are prevented
    - 👥 Improves dashboard usability

<img src="https://github.com/user-attachments/assets/a6797ee7-5d8b-4316-8bf3-9081e95f710c" alt="Salary Dashboard Data Validation" width="425" height="400">

## Conclusion

This Excel project, my first of its kind, helped me explore salary trends across various data-related job titles and better understand how location and job type influence compensation. 
I built this dashboard using data from [Luke Barousse's](https://github.com/lukebarousse) Excel course, which provided me with the foundational knowledge of using Excel for data analysis.

## Skills I Gained:
Advanced Excel Functions: Mastered using array formulas, MEDIAN(), IF(), FILTER(), and SEARCH() to handle complex datasets.
Data Visualization: Improved my ability to create and customize charts and dashboards for clear data storytelling.
Data Integrity and Validation: Gained experience in creating data validation rules to ensure data accuracy and usability.

## Insights:
Through this project, I learned how salary disparities across job titles and geographic locations can be analyzed. I also saw the power of Excel as a tool for making informed career decisions based on real-world data.

This project has sharpened my Excel skills, provided valuable insights into the world of data analytics, and improved my ability to create dynamic, user-friendly dashboards. I look forward to applying these skills in future data analysis projects!

