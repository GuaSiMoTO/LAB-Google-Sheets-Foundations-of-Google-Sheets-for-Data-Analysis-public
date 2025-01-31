# LAB-Google-Sheets-Foundations-of-Google-Sheets-for-Data-Analysis

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
   - Take note of any apparent inconsistencies, errors, or missing values.

## Iteration 2: Identify and Remove Duplicates
Duplicate records can lead to inaccurate analysis and reporting. Your next step is to ensure that no duplicate entries are present in the dataset.
1. **Find Duplicates**: 
   - Use a combination of the 'Name' and 'Email' columns to identify duplicate entries.
   - Highlight these duplicates for review.
2. **Delete Duplicate Entries**: Once identified, remove the redundant records while preserving at least one unique entry per employee.

## Iteration 3: Department Name Standardization
Data consistency is crucial, especially when working with categorical variables.
- Locate the 'Department' column and identify any inconsistencies in naming conventions.
- Specifically, replace all instances of 'HR' with 'Human Resources' to maintain uniformity.

## Iteration 4: Date Component Extraction
Dates are often useful for analysis, especially when broken down into individual components.
1. Extract Day, Month, and Year:
   - Take the 'Date of Joining' column and split it into three separate columns: 'Day', 'Month', and 'Year'.
   - Ensure the extracted values remain in the correct format.

## Iteration 5: Handling Missing Values
Missing data can lead to gaps in analysis. It is important to address these missing values logically.
1. **Fill Missing Salaries**:
- Identify missing values in the 'Salary' column.

- Compute the average salary per department and use these averages to fill in the missing values accordingly.
2. **Address Missing Performance Scores**:
- Locate missing values in the 'Performance Score' column.
- Instead of using the mean, calculate and apply the median performance score within each department to fill in the gaps.

## Iteration 6: Data Validation
Ensuring the integrity of your data is critical before proceeding with analysis.
1. Validate Employee Ages:

- Check the 'Age' column to ensure that all values fall within a reasonable range (e.g., between 18 and 65 years old).
- Flag and correct any anomalies found.

2. Check Email Format:

- Implement a data validation rule to verify that all email addresses include an '@' symbol and a domain (e.g., .com, .org).
- Highlight any incorrectly formatted emails for correction.

## Iteration 7: Data Analysis Using Lookup Functions
Now that the data is cleaned, you can begin performing basic analysis.

1. Salary Analysis by Department:

- Use the VLOOKUP function to create a summary table displaying the salary range for each department.
- Ensure that the table provides meaningful insights into salary distribution across departments.

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
