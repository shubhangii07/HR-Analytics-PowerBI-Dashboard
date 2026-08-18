# Data Cleaning & Transformation

## Overview

The raw HR dataset was imported from **Microsoft Excel into Power BI**, where data cleaning and transformation were performed using **Power Query**.

The original Excel file was retained as the **raw source dataset**, while the data preparation and transformation were performed within Power BI for analysis and dashboard development.

---

## Source Dataset

- **Source:** Microsoft Excel
- **Dataset:** HR Analytics
- **Raw Records:** 1,480 rows
- **Raw Columns:** 37 columns
- **Transformation Tool:** Power Query in Microsoft Power BI

The raw dataset contains employee-level HR information such as:

- Employee ID
- Age
- Attrition
- Business Travel
- Department
- Job Role
- Job Satisfaction
- Salary Slab
- Years of Experience
- Gender
- And other employee-related attributes

---

## Power Query Transformation Process

The following transformations were applied to the raw dataset in Power BI:

### 1. Source

The raw HR dataset was connected to Power BI from the Excel source file.

### 2. Navigation

The required `HR_Analytics` sheet/table was selected from the source workbook.

### 3. Promoted Headers

The appropriate row was promoted to become the column headers so that the dataset could be correctly structured for further transformations.

### 4. Changed Type

Appropriate data types were assigned to the relevant columns to ensure correct handling of numerical, text, and categorical fields.

### 5. Sorted Rows

The dataset was sorted as part of the data preparation workflow.

### 6. Removed Top Rows

Unnecessary rows from the beginning of the source data were removed.

### 7. Removed Duplicates

Duplicate records were removed to prevent repeated records from affecting employee-level analysis and dashboard metrics.

### 8. Filtered Rows

The dataset was filtered to retain records relevant to the HR analysis.

### 9. Replaced Value

Selected values were replaced where required to maintain consistency within the dataset.

### 10. Changed Type1

Data types were reviewed and adjusted again after the preceding transformations to ensure the final dataset remained correctly formatted.

---

## Creating the AttritionCount Column

A conditional column named **`AttritionCount`** was created in Power Query.

The logic used was:

```text
If Attrition = "Yes" → 1
If Attrition = "No"  → 0
```

| Attrition | AttritionCount |
|---|---:|
| Yes | 1 |
| No | 0 |

This converts the categorical attrition status into a numeric indicator, making it easier to aggregate and analyze employee attrition in Power BI.

---

## Data Preparation Outcome

After applying the Power Query transformations, the dataset was prepared for analysis and visualization within Power BI.

The transformed dataset supports analysis of:

- Employee attrition
- Department-wise employee distribution
- Salary slab-wise attrition
- Age group analysis
- Gender-wise attrition
- Job role analysis
- Job satisfaction
- Employee experience

---

## Dashboard Metrics

The prepared dataset was used to build the HR Analytics Dashboard and analyze key metrics including:

- Total Employees
- Active Employees
- Attrition Count
- Attrition Rate
- Average Age
- Average Experience

The dashboard also provides interactive filtering using:

- **Age Group**
- **Department**

---

## Tools Used

- **Microsoft Excel** — Raw data source
- **Microsoft Power BI** — Dashboard development
- **Power Query** — Data cleaning and transformation
- **DAX** — Data analysis and calculations

---

## Data Preparation Flow

```text
Raw Excel Dataset
       ↓
Import into Power BI
       ↓
Power Query
       ↓
Promote Headers
       ↓
Change Data Types
       ↓
Sort Rows
       ↓
Remove Unnecessary Rows
       ↓
Remove Duplicates
       ↓
Filter Rows
       ↓
Replace Values
       ↓
Create AttritionCount
       ↓
Analysis-Ready Dataset
       ↓
HR Analytics Dashboard
```

---

## Summary

The raw HR dataset was kept unchanged in Excel and used as the source for the Power BI project.

All major data preparation and transformation activities were performed within **Power Query in Power BI**. This workflow helped prepare the data for reliable HR analytics, KPI reporting, and interactive dashboard visualization.
