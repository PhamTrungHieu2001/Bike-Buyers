# Bike-Buyers

## Overview

## Data source
The data is sourced from this [GitHub repository](https://github.com/AlexTheAnalyst/Excel-Tutorial/blob/main/Excel%20Project%20Dataset.xlsx). The dataset contains detailed information about individuals who have or have not purchased bikes. The data includes various attributes that can be used to analyze patterns and factors influencing bike purchasing decisions.

Attributes:
- **ID**: Unique identifier for each individual.
- **Marital Status**: Marital status of the individual (_Single/Married_).
- **Gender**: Gender of the individual (_Male/Female_).
- **Income**: Annual income of the individual in USD.
- **Children**: Number of children in the household.
- **Education**: Level of education attained (_High School, Bachelors, Graduate Degree, Partial College, Partial High School_).
- **Occupation**: Job title or occupation of the individual.
- **Home Owner**: Home ownership status (_Yes/No_).
- **Cars**: Number of cars owned.
- **Commute Distance**: Distance to work (_0-1 Miles, 1-5 Miles, 5-10 Miles, 10+ Miles_).
- **Region**: Region of residence (_North America, Europe, Pacific_).
- **Age**: Age of the individual.
- **Purchased Bike**: Whether the individual purchased a bike (_Yes/No_).

## Workbook structure
The 'Excel Project.xlsx' consists of the following sheets:
* **Data**: raw data extracted from GitHub
* **Working Sheet**: cleaned data
* **PivotTables**: containing PivotTables created from the cleaned data
* **Dashboard**: containing all the created PivotTables and some filters

## Data cleaning
1. Remove duplicates
- Remove duplicates by going 'Data' -> 'Remove Duplicates'

2. Update 'Marital Status' and 'Gender'
- Find and replace 'M' and 'S' in 'Marital Status' with 'Married' and 'Single'
- Find and replace 'M' and 'F' in 'Gender' with 'Male' and 'Female'

<table>
<tr><th> Before </th><th> After </th></tr>
<tr><td>

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

</td><td>

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

</td></tr> </table>

3. Remove '.00' at the end of the 'Income' column
- Change the data type to 'Currency'

<table>
<tr><th> Before </th><th> After </th></tr>
<tr><td>

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

</td><td>

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

</td></tr> </table>

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
Males have a significantly higher income than females in both categories
<img>

2. Customer Commute Distance
The percentage of people purchasing a bike tends to drop as the commute distance increases.
The percentages of people with a commute distance of under 5 miles purchasing a bike are around 45 to 60 percent.
Only about 30% of people with a commute distance of over 10 miles purchase a bike.
<img>
3. Customer Age Group
Only in the 31-54 age group do people buying a bike outnumber those who don't.
<img>
  
## Create a dashboard
<img>

