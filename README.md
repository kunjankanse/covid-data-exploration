# 🦠 COVID-19 Data Exploration with SQL

## 📌 Overview

This project explores global COVID-19 data using SQL to derive insights about infection rates, mortality, and vaccination trends across different countries and continents. It uses Microsoft SQL Server and demonstrates various SQL techniques for data analysis and reporting.

## 🧰 Tools & Skills Used

- Microsoft SQL Server
- Joins
- Common Table Expressions (CTEs)
- Temporary Tables
- Window Functions
- Aggregate Functions
- Data Type Conversion
- Creating Views

## 🌍 Data Source

- **Source**: [Our World in Data – COVID-19](https://ourworldindata.org/covid-deaths)
- **Files Used**:
  - `CovidDeaths.xlsx`
  - `CovidVaccinations.xlsx`
- These files were downloaded locally and imported into SQL Server using the **Import Wizard**.

## 🛠 Database Tables

After import, the data was stored in the `PortfolioProject` database as:
- `CovidDeaths`
- `CovidVaccinations`

## 🔍 Key Analysis Performed

### 📌 Initial Data Review
- Filtered out rows where the continent value is null
- Selected key columns: location, date, total_cases, total_deaths, population

### ⚰️ Total Cases vs Total Deaths
- Calculated the **death percentage**: `(total_deaths / total_cases) * 100`
- Assessed the likelihood of dying if infected with COVID-19 per country

### 🧪 Total Cases vs Population
- Calculated the **percentage of population infected**: `(total_cases / population) * 100`
- Identified countries with the highest infection rates

### 🌎 Death Count by Country and Continent
- Used aggregate functions to find maximum death counts by location
- Converted string to integer where necessary for accurate calculations

### 📊 Global Statistics
- Summed total new cases and new deaths globally
- Computed the **global death rate** over time

### 💉 Vaccination Analysis
- Joined `CovidDeaths` and `CovidVaccinations` tables
- Used window functions to calculate **cumulative vaccination counts**
- Calculated **% population vaccinated** using temporary tables and CTEs

### 📁 Data Optimization
- Created a **view** (`PercentPopulationVaccinated`) for downstream visualization or reporting

## 📈 Sample Insights

- Some small countries showed high infection percentages due to low population.
- High death percentages in certain countries highlighted regional healthcare disparities.
- Rolling vaccination analysis helped identify leaders and laggards in vaccine distribution.

## 📊 Visualization & Extension

This dataset and analysis can be extended using BI tools such as:
- **Power BI**
- **Tableau**
- **Excel Dashboards**

The view `PercentPopulationVaccinated` is particularly useful for tracking vaccination trends in BI tools.

## 🙏 Acknowledgements

- 📊 Data Source: [Our World in Data – COVID-19](https://ourworldindata.org/covid-deaths)
- **Note**: Due to schema changes online, data was analyzed using Excel exports downloaded from the above source.

---
