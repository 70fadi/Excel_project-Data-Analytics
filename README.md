# Excel_project-Data Analytics
My project demonstrating my Excel skills

# Excel Salary Dashboard

<img width="740" height="281" alt="Screenshot 2026-09-14 135017" src="https://github.com/user-attachments/assets/602fc676-573e-41dd-9267-4d1634b0c1db" />

## Introduction

This data salary dashbaord was created to assist people who are looking for a job to investigate salaries for their desired jobs and ensure they are getting paid what the market offers. 

### Dashboard File 
My final dashboard is in [project_1](Project_1)

### Excel Skills Used

The following Excel skills were used for analysis: 

- **📊 Charts**

- **Formulas and Functions**

- **Data Validation**

### Data Jobs Dataset 

The dataset used for this project contains real-word data scinece job information from 2023. It includes detailed information on:

- **Job titles**
- **Salaries**
- **Locations**
- **Skills**

## Dashboard Build

### Charts

#### Data Science Job Salaries - Bar Chart 

<img width="496" height="253" alt="Screenshot 2026-09-14 151424" src="https://github.com/user-attachments/assets/e6979765-7123-4378-ae0b-515530b43883" />


- **Excel Features:** Used the bar chart feature with formatted salary values and enhanced layout for clarity.

- **Design Choice**: Horizontal bar chart for visual comparison or median salaries.

- **Data Organization**: Sorted job titles by descending salary for improved readability 

- **Insights Gained**: This enables quick identification of salary trends, noting that senior roles and engineers are higher-paying than the Analyst role.

#### Country Median Salary - Map Chart 

<img width="406" height="239" alt="Screenshot 2026-09-15 151913" src="https://github.com/user-attachments/assets/06660cf1-9e12-4b50-8591-c9e65d791cd8" />


- **Excel Features**: Used Excel's map chart feature to show the median salaries globally.

- **Design Choice**: Colour-coded map to visually differentiate salary levels across regions. 

- **Data representation**: Showed Median salary for each country with available data. 

- **Visual Enhancement**: Improved readability and immediate understanding of geographic salary trends.

- **Insights Gained**: Enables a quick grasp of global salary disparities and highlights high/low salary regions. 


### Formulas and Functions 

#### Median Salary by Job Titles

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

- **Multi-Criteria Filtering**: Check job title, country, schedule type, and exclude blank salaries.

- **Array Formula**: Used `Median()` function with `if()` inside it to analyze an array. 

- **Tailored Insights**: Provide specific salary information for job title, regions, and schedule types. 

- **Formula Purpose**: This formula populates the table below, returning the median salary based on job title, country, and type specified 


Background Table 

<img width="265" height="220" alt="1_Salary_Dashboard_Screenshot1" src="https://github.com/user-attachments/assets/81b322e0-57cb-47ea-b63b-c9796eda9f13" />



Dashboard implementation

<img width="242" height="269" alt="Screenshot 2026-09-16 152559" src="https://github.com/user-attachments/assets/b83e99b3-1e8c-4deb-afc8-b40455c160eb" />


Count of Job Schedule Type 

```
=FILTER(J2#,(NOT(ISNUMBER(SEARCH("and",J2#))+ISNUMBER(SEARCH(",",J2#))))*(J2#<>0))
```

- **Unique List Generation** This Excel formula below employs the `FILTER()` function to exclude entries containing "and" or commas, and omit zero values.
 
- **Formula Purpose**: This formula creates the table below, which gives us a list of unique job schedule types. 


<img width="195" height="119" alt="1_Salary_Dashboard_Screenshot2" src="https://github.com/user-attachments/assets/a5c9c27b-3d0f-4741-9e83-c46d1fb8944b" />


Dashboard Implementation: 


<img width="942" height="1212" alt="1_Salary_Dashboard_Type" src="https://github.com/user-attachments/assets/711fa098-72c7-4082-8352-6e735c0f50a3" />


### Data Validation 

#### Filter List 

- **Enhanced Data Validation:** Implementing the filtered list as a data validation rule under the `Job title`, `Country`, and `Type` options in the Data tab ensures:

 - 🎯 User input is restricted to predefined, validated schedule types
 - 🚫 Incorrect or inconsistent entries are prevented
 - 👥 Overall usability of the dashboard is enhanced 




https://github.com/user-attachments/assets/f95d6b7f-fe1b-49cb-821e-2954d8b9d305


## Conclusion 

I created this dashboard to showcase insights into salary trends across various data-related job titles. Utilizing data from my Excel course, this dashboard allows users to make informed decisions about their career paths. Exploring the functionalities to understand how location and job type influence salaries.

















