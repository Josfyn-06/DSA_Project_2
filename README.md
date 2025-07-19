# DSA_Project_2
This is my application of data analysis concepts learnt during the Data Skillup Africa training taught by the Incubator Hub which include data cleaning, data querying,visualization and insights extraction using Excel, SQL and Power BI.
- - -

## Project Title: Palmoria Group HR Analysis
- - -

## Table of Contents 
[Project Overview](#project-overview)

[Dataset](#dataset)

[Data Source](#data-source)

[Tools Used](#tools-used)

[Data Cleaning and Preparation](#data-cleaning-and-preparation)

[Exploratory Data Analysis](#exploratory-data-analysis)

[Data Visuals](#data-visuals)

[Key Insights](#key-insights)

[Recommendation](#recommendation)
- - -

### Project Overview
This project analyses HR data from the **Palmoria Group**, a Nigerian manufacturing company to uncover gender-related inequalities and recommend solutions. The goal is to assist the CHRO and executive team in making data-driven decisions on pay equity, performance and employee bonuses.
- - -

### Dataset
Two datasets were given, the data set includes:

- **Palmoria Employee Data**: This contains the employee-level information from Palmoria's Group's three regions.
  
  - **Total Rows**: 1,015 rows

  - **Total Fields**: 6 columns which include:

    - *Name*: Full name of the employee
    - *Gender*: Gender of the employee
    - *Department*: The functional area where the employee works
    - *Salary*: Salary of the employee
    - *Location*: Region employee is based
    - *Rating*: Performance rating of the employee

- **Palmoria Bonus Rules**: This contains the following columns:

  - **Total Rows**: 12 rows
  
  - **Total Fields**: 6 columns which include:

    - *Department*: The name of the department for which the bonus structure applies
    - *Very Poor*: Bonus rate (in %) to award employees with "Very Poor" performance rating
    - *Poor*: Bonus rate percentage for "Poor" performance
    - *Average*: Bonus rate percentage for "Average" performance
    - *Good*: Bonus rate percentage for "Good" performance
    - *Very Good*: Bonus rate percentage for "Very Good" performance

### Data Source
The dataset was handed to us by the Incubator Hub to practice and showcase what we've learnt so far in the Data Skillup Africa Training. The dataset is available upon request
- - -

### Tools Used
- Microsoft Power BI for:
  - Data cleaning
  - End-to-end analysis
  - Visualisation
  - Filtering
  - Dashboard and visualisation
- - -

### Data Cleaning and Preparation
To ensure the dataset was ready for meaningful analysis in Power BI, the following data cleaning steps were carried out in **Power Query Editor**:

- **Removal of Blanks and Nulls**: Some employees had no salary indicating they were no longer part of the company. Thus, those rows were removed. The number of rows removed were 43 rows, leaving us with 972 rows. Null values were seen in department column and were removed leading to 26 more rows being removed and leaving us with 946 rows
- **Standardised Missing/Undisclosed Gender**:  Some employees did not specify their gender and gender analysis is a core focus of this project. Thus, a generic name "Undisclosed" was given to replace the blank.
- **Ensured Correct Data Types**: I ensured each columns had the correct data type
- **Duplicates Removal**: 3 duplicates were found and removed leaving us with 943 rows
- **Loaded Bonus Rules Table Separately**: Imported Bonus Rules Table, transformed it by unpivoting other columns except the Department leading to the dataset increasing from 12 rows to 60 rows with 3 columns
- **Merged the Two Datasets**: I merged the both datasets using Department and Rating as key, leaving me with a clean data of 943 rows and 7 columns with the Bonus Percentage Column being the new column
- **Created More Columns**: I created two calculated columns and one conditional column. The columns include:
  
  - *Salary Band*: This is the conditional column created to show the salary in the band of tens; `10k-20k`, `20k-30k`, `30k-40k`, `40k-50k`, `50k-60k`, `60k-70k`, `70k-80k`, `80k-90k`, `>90k`
  - *Bonus Amount*= `[Salary]*[Bonus Perecentage]`
  - *Total Pay* = `[Salary]+[Bonus Amount]`
- - -

### Exploratory Data Analysis




