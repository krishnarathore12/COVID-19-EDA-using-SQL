# COVID-19-Data-Analysis-using-SQL

## Project Overview

This project involves exploratory data analysis (EDA) on COVID-19 data using SQL. The dataset is sourced from Our World in Data and contains comprehensive information on COVID-19 metrics across various countries and continents. The analysis focuses on cleaning, transforming, and querying the data to extract meaningful insights.

## Data Source

- **Primary Dataset:** [Our World in Data COVID-19 Dataset](https://covid.ourworldindata.org/data/owid-covid-data.xlsx)
- **GitHub Repository:** [OWID COVID-19 Data Repository](https://github.com/owid/covid-19-data/tree/master/public/data)

## Dataset Specifications

- **Rows:** 87,743
- **Columns:** 59
- **Notable Features:**
  - Contains many null values that are handled during the analysis.
  - `continent` column contains names of continents.
  - `location` column contains names of both continents and countries.

## Data Cleaning and Preparation

1. **Null Values:** The dataset contains numerous null values that have been considered and appropriately handled during analysis.
2. **Column Distinction:**
   - Ensure to differentiate between `location` entries that are continents and those that are countries.
   - Example SQL to exclude continent rows:
     ```sql
     SELECT location, MAX(total_cases)
     FROM covid19timeseries
     WHERE continent IS NOT NULL;
     ```
3. **Data Type Correction:** Many columns are imported as `varchar` and need to be converted to `float` for accurate analysis.

## Importing Dataset Into SQL Server

To import the dataset into SQL Server, it is recommended to use the SQL Server Import and Export Data (64-bit) wizard:

1. Launch the wizard from the Start Menu.
2. Avoid using the inbuilt import option available within SQL Server Management Studio (SSMS).

## Visualisations
![Stringency Index and New Cases](https://github.com/krishnarathore12/COVID-19-EDA-using-SQL/assets/86671142/f474a776-43a9-4c0d-809d-9a814b258310)
![Most people vaccinated](https://github.com/krishnarathore12/COVID-19-EDA-using-SQL/assets/86671142/9803b7b7-4a9a-4077-b338-00b17924b3fb)
![Infected Pop Perc](https://github.com/krishnarathore12/COVID-19-EDA-using-SQL/assets/86671142/58a7c5cf-5820-4998-80cc-90e6e057d525)
![Infected Pop Perc  Map](https://github.com/krishnarathore12/COVID-19-EDA-using-SQL/assets/86671142/48aa790a-18b5-4021-b0f8-048f88bc9141)
![Continent Wise Death Count](https://github.com/krishnarathore12/COVID-19-EDA-using-SQL/assets/86671142/1cb42c81-7e9d-444d-b04f-3c8fa616012e)
![Continent Wise Death Count - bubble](https://github.com/krishnarathore12/COVID-19-EDA-using-SQL/assets/86671142/1773d1f0-bae3-4b42-9b7e-bba6e8342808)

