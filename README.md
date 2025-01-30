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

## Iteration 2: Identify and Remove Duplicates
- **Find Duplicates**: Use the combination of 'Name' and 'Email' columns to find duplicates.
- **Delete Duplicate Entries**:

## Iteration 3: Department Name Standardization
- **Replace 'HR' with 'Human Resources'**: In the 'Department' column, replace all instances of 'HR' with 'Human Resources'.

## Iteration 4: Date Component Extraction
- **Separate Day, Month, and Year**: Split the 'Date of Joining' into separate columns for day, month, and year.

## Iteration 5: Handling Missing Values
- **Fill Missing Salaries**: For missing salaries, calculate the average salary per department and use that value to fill the missing entries. Use:
- **Address Missing Performance Scores**: For missing 'Performance Score' values, use the median of the respective department.

## Iteration 6: Data Validation
- **Validate Age Range**: Ensure that employee ages are within a reasonable range (e.g., between 18 and 65).
- **Email Format Check**: Implement data validation rules to verify that email addresses contain an '@' symbol and a dot.

## Iteration 7: Data Analysis Using Lookup Functions
- **Salary Analysis by Department**: Use `VLOOKUP` to create a table showing the salary range in each department.

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
