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
After cleaning the dataset and merging the datasets to form a new dataset. These are the questions are tried to give answers to using the dataset:
Key analysis questions:

- What is the gender distribution across Palmoria?
- Are performance ratings equally distributed by gender?
- Does a gender pay gap exist? Where is it most significant?
- How many employees earn below the $90,000 legal minimum?
- How are salaries distributed across $10,000 bands?
- How much bonus should be paid per employee, region, and department?
- - -

### Data Visuals
<img width="960" height="547" alt="Screenshot 2025-07-19 073958" src="https://github.com/user-attachments/assets/832a1dd1-042b-4073-94d4-9464f19f121c" />





<img width="961" height="555" alt="Screenshot 2025-07-19 074135" src="https://github.com/user-attachments/assets/73c185fb-75ec-4200-944d-4f9d24eca3d8" />






<img width="965" height="551" alt="Screenshot 2025-07-19 074314" src="https://github.com/user-attachments/assets/5576c4f1-6f71-4b54-8914-1519455d40ce" />






<img width="959" height="550" alt="Screenshot 2025-07-19 074717" src="https://github.com/user-attachments/assets/38379b07-9d9a-463a-8b9b-e24bbe54b7de" />






### Key Insights
- **Gender Imbalance**: Kaduna and Lagos have more male employees than female employees. In Abuja, we have same number of male and female
- **Pay Gaps**: After analyzing average salary across departments, i found that male employees earn more on average in 9 departments out of 12 departments, while female employees earn more in only 3 departments. This suggests a potential gender pay imbalance that requires further attention.
- **Performance Ratings**: Female employees outperform the male counterparts as they populate more of the average, good and very good ratings. On average, the female still beat the male in performance
- **Compliance Violations**: Out of 943 employees, only 292 employees earn up to $90,000 or more. This means that about 69% of employees earn less than the mandated $90,000 salary.
- **Salary Banding**: Most employees fall into >$90,000 band followed by $70,000-$80,000 and $80,000–$90,000 bands.
- - -

### Recommendations
- **Address Gender Pay Imbalance**: Conduct a detailed salary audit across all departments and roles to uncover root causes of the observed pay disparities. Implement pay equity policies and revise compensation structures to ensure fairness, especially in departments where males earn significantly more than their female counterparts.
- **Strengthen Performance Appraisal Systems**: Since female employees consistently outperform their male counterparts, ensure that performance evaluations are standardized, transparent, and regularly updated. High-performing employees, regardless of gender, should be rewarded appropriately to encourage retention and motivation.
- **Improve Gender Diversity in Key Regions**: Lagos and Kaduna show a strong male dominance. Launch targeted recruitment drives to attract and retain more female talent in these regions. Introduce inclusive workplace policies and mentorship programs to support gender balance.
- **Review Salary Structure for Compliance**: With over 69% of employees earning less than the mandated $90,000 minimum, the company risks regulatory non-compliance. An immediate salary structure review is recommended to phase in salary adjustments and bring all employees into compliance with the new regulation.
- **Optimize Salary Band Distribution**: Salary bands show concentration just above $90,000, which could indicate minimal compliance rather than value-based compensation. Consider implementing performance-based salary banding to reward high performers and align pay with role responsibilities and contributions.
- **Investigate Unspecified Gender Data**: Employees with unspecified gender may skew analysis and hinder diversity tracking. Encourage self-identification through confidential surveys or onboarding updates to strengthen the accuracy of diversity metrics.
- **Establish a Gender Equity Task Force**: Create a cross-functional team responsible for monitoring gender-related issues, promoting equity in hiring, promotions, pay, and retention, and providing regular reports to leadership.











