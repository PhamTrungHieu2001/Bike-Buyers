# Bike-Buyers

## Overview

## Data source
The data is sourced from this [GitHub repository](https://github.com/AlexTheAnalyst/Excel-Tutorial/blob/main/Excel%20Project%20Dataset.xlsx). The dataset contains detailed information about individuals who have or have not purchased bikes. The data includes various attributes that can be used to analyze patterns and factors influencing bike purchasing decisions.

Attributes:
- **ID**: Unique identifier for each individual.
- **Marital Status**: Marital status of the individual (Single/Married).
- **Gender**: Gender of the individual (Male/Female).
- **Income**: Annual income of the individual in USD.
- **Children**: Number of children in the household.
- **Education**: Level of education attained (High School, Bachelors, Graduate Degree, Partial College, Partial High School).
- **Occupation**: Job title or occupation of the individual.
- **Home Owner**: Home ownership status (Yes/No).
- **Cars**: Number of cars owned.
- **Commute Distance**: Distance to work (0-1 Miles, 1-5 Miles, 5-10 Miles, 10+ Miles).
- **Region**: Region of residence (North America, Europe, Pacific).
- **Age**: Age of the individual.
- **Purchased Bike**: Whether the individual purchased a bike (Yes/No).

## Workbook structure
The 'Excel Project.xlsx' consists of the following sheets:
* Data: raw data extracted from GitHub
* Working Sheet: cleaned data
* PivotTables: containing PivotTables created from the cleaned data
* Dashboard: containing all the created PivotTables and some filters

## Data cleaning
1. Remove duplicates
- Remove duplicates by going 'Data' -> 'Remove Duplicates'

2. Update 'Marital Status' and 'Gender'
- Find and replace 'M' and 'S' in 'Marital Status' with 'Married' and 'Single'
- Find and replace 'M' and 'F' in 'Gender' with 'Male' and 'Female'
<table>
  <tr>
    <td>

### Before

| Marital Status | Gender |
|----------------|--------|
| M              | F      |
| M              | M      |
| M              | M      |
| S              | M      |
| S              | M      |
| M              | F      |
| S              | M      |
| M              | M      |
| M              | M      |

    </td>
    <td>

### After

| Marital Status | Gender |
|----------------|--------|
| Married        | Female |
| Married        | Male   |
| Married        | Male   |
| Single         | Male   |
| Single         | Male   |
| Married        | Female |
| Single         | Male   |
| Married        | Male   |
| Married        | Male   |

    </td>
  </tr>
</table>

3. Remove '.00' at the end of the 'Income' column
- Change the data type to 'Currency'
<table>
  <tr>
    <td>

### Before

| Income       |
|--------------|
| $40,000.00   |
| $30,000.00   |
| $80,000.00   |
| $70,000.00   |
| $30,000.00   |
| $10,000.00   |
| $160,000.00  |
| $40,000.00   |
| $20,000.00   |

    </td>
    <td>

### After

| Income    |
|-----------|
| $40,000   |
| $30,000   |
| $80,000   |
| $70,000   |
| $30,000   |
| $10,000   |
| $160,000  |
| $40,000   |
| $20,000   |

    </td>
  </tr>
</table>

4. Divide 'Age' into 'Age group'
- Use the IF function to divide into 3 age groups: '0-30', '31-54', '55+'

| Age | Age Group |
|-----|-----------|
| 42  | 31 - 54   |
| 43  | 31 - 54   |
| 60  | 55+       |
| 41  | 31 - 54   |
| 36  | 31 - 54   |
| 50  | 31 - 54   |
| 33  | 31 - 54   |
| 43  | 31 - 54   |
| 58  | 55+       |

## Create PivotTables
1. Average Income By Gender
2. Customer Commute Distance
3. Customer Age Group

## Create a dashboard

