# LAB-Google-Sheets-Foundations-of-Google-Sheets-for-Data-Analysis

![PILL_WHITE](https://github.com/user-attachments/assets/c04c5b8e-bc95-4e32-8213-613e82ebc5a8)

## Introduction

> ***Note:*** _This can be a pair programming activity or done independently._

Hello everyone, welcome to this lab where we will apply fundamental Google Sheets concepts through a practical case study. We'll learn how to import and export data, clean data, and perform basic data analysis using a CSV file. Imagine you are part of a small team at a company, and you need to manage and clean the team's data.

## Initial Setup

### Fork The Repository
First things first, head over to GitHub and click the `fork button` to create a copy of this repository in your personal account. This will allow you to make changes and save your progress.

## Scenario

You've been hired as a data analyst for a small company. They have given you a CSV file with employee data that needs cleaning and analysis. Your task is to clean this data and provide insights to the HR and Finance departments.

## Iteration 1: Data Profiling

Alright, let’s get started by getting a sense of what our data looks like. This first step is all about understanding the structure and content of your data.

1. **Analyze Data**
   - Start by importing the provided `sample_data.csv` file into Google Sheets.
   - Take a good look at the data to understand its structure, content, and quality.
   - Identify the types of data in each column (e.g., numeric, text, date). This step is crucial to get a sense of what you're dealing with.

## Iteration 2: Identify and Remove Duplicates
- **Find Duplicates**: Use the combination of 'Name' and 'Email' columns to find duplicates.
- **Delete Duplicate Entries**:
  - Select your data range.
  - Click on `Data` > `Data cleanup` > `Remove duplicates`.
  - Ensure that all relevant columns are selected to avoid removing non-duplicate data that only matches in name and email.

## Iteration 3: Department Name Standardization
- **Replace 'HR' with 'Human Resources'**: In the 'Department' column, replace all instances of 'HR' with 'Human Resources'.
  - Use `CTRL + H` (or `CMD + H` on Mac) to open the "Find and Replace" tool.
  - Enter "HR" in the "Find" box and "Human Resources" in the "Replace with" box.
  - Click "Replace All" to apply this change throughout the entire 'Department' column.

## Iteration 4: Date Component Extraction
- **Separate Day, Month, and Year**: Split the 'Date of Joining' into separate columns for day, month, and year.
  - Use `=DAY(A2)` to extract the day.
  - Use `=MONTH(A2)` to extract the month.
  - Use `=YEAR(A2)` to extract the year.
  - Add these as new columns labeled 'Join Day', 'Join Month', and 'Join Year' respectively.

## Iteration 5: Handling Missing Values
- **Fill Missing Salaries**: For missing salaries, calculate the average salary per department and use that value to fill the missing entries. Use:
  - `=AVERAGEIF(B:B, B2, C:C)` where B is the department column and C is the salary column.
  - Use `=IF(ISBLANK(C2), VLOOKUP(B2, Salary_Avg_Table, 2, FALSE), C2)` to fill missing values.
- **Address Missing Performance Scores**: For missing 'Performance Score' values, use the median of the respective department.
  - Use `=MEDIAN(FILTER(D:D, B:B=B2))` where B is the department column and D is the performance score column.

## Iteration 6: Data Validation
- **Validate Age Range**: Ensure that employee ages are within a reasonable range (e.g., between 18 and 65).
  - Select the age column.
  - Click `Data` > `Data validation`.
  - Set criteria to "Number" between "18" and "65".
- **Email Format Check**: Implement data validation rules to verify that email addresses contain an '@' symbol and a dot.
  - Use `=IF(AND(ISNUMBER(SEARCH("@", A2)), ISNUMBER(SEARCH(".", A2))), "Valid", "Invalid")`.

## Iteration 7: Data Analysis Using Lookup Functions
- **Salary Analysis by Department**: Use `VLOOKUP` or `QUERY` to create a table showing the salary range in each department.
  - Find the minimum salary: `=MINIFS(C:C, B:B, "HR")`.
  - Find the maximum salary: `=MAXIFS(C:C, B:B, "HR")`.
  - Find the average salary: `=AVERAGEIFS(C:C, B:B, "HR")`.
- **Retrieve Specific Data**: Use `XLOOKUP` to find specific information, such as the email and joining date of employees with a 'Performance Score' above 4.
  - Example: `=FILTER(A:B, C:C>4)`.

## Iteration 8: Data Summarization and Visualization
- **Create a Summary Table**: Use functions like `SUMIF` and `COUNTIF` to summarize data such as the total number of employees per department and average performance score.
  - `=COUNTIF(B:B, "HR")` to count employees in HR.
  - `=AVERAGEIF(B:B, "HR", D:D)` to find the average performance score in HR.

## Bonus

### Hint

#### Data Cleaning Simulation Plan

To make the bonus we will use “Ask A Manager Salary Survey 2021 .csv” uploaded in this lab.

- **Remove Duplicates**: Verify if there are duplicate records and remove them.
- **Standardize Column Values**: Standardize the names of the countries.
- **Handle Missing Values**: Fill or remove null values in critical columns.
- **Convert Data Types**: Ensure that columns like `What is your annual salary?` and `Additional Compensation` are numeric.
- **Create New Columns**: Create a column that combines `Job title` and `Industry` for a more detailed analysis.

## How to Submit

To submit this LAB, upload the file to your forked repository.

## Additional Resources

- [Google Sheets documentation](https://support.google.com/docs/topic/9054606?hl=en&ref_topic=1382883)
- [Conditional Formatting in Google Sheets](https://support.google.com/docs/answer/78413?hl=en)
- [Google Sheets Formulas and Functions](https://support.google.com/docs/answer/3093197?hl=en)
