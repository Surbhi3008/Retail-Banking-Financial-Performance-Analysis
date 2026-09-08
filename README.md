# Retail Banking Financial Performance & Benchmarking Dashboard

**Power BI | DAX | Power Query | Excel | Financial Analytics**

## Project Overview

The **Retail Banking Financial Performance & Benchmarking Dashboard** is an interactive Power BI analytics solution developed to analyse and compare the financial performance of selected Indian banks across multiple financial years and key banking metrics.

The project brings together financial information from publicly available bank reports, organizes the information into a structured analytical dataset, and presents the analysis through an interactive three-page Power BI dashboard.

The dashboard supports:

- Historical KPI analysis
- Year-over-year performance analysis
- Peer bank comparison
- Project-level benchmark analysis
- Bank ranking
- Performance gap analysis
- Category-level analysis
- Dynamic analytical insights and recommendations

The solution is intended as an analytical reporting and decision-support project rather than a live banking production system.

---

## Business Problem

Financial information published by banks is often distributed across annual reports and financial disclosures. Although this information is publicly available, comparing multiple banks across several financial years can be time-consuming when performed manually.

A structured analytical solution can help answer questions such as:

- How has a selected financial KPI changed over time?
- How does one bank compare with its peer banks?
- Which bank performs strongest on a selected metric?
- How does a selected bank compare with the calculated peer benchmark?
- What is the year-over-year change in a KPI?
- Where is a bank performing above or below the benchmark?
- Which areas may require further analysis?

The objective of this project was to organize relevant banking financial metrics into a consistent analytical model and develop an interactive dashboard for comparative financial analysis.

---

## Project Objectives

1. Consolidate financial performance data for selected Indian banks across multiple financial years.
2. Standardize financial metrics into a structured dataset suitable for comparative analysis.
3. Clean, organize and transform the financial data for analytical use.
4. Build a structured data model in Power BI using fact and dimension tables.
5. Develop dynamic DAX measures for KPI analysis, year-over-year calculations, rankings and benchmarking.
6. Enable interactive analysis using bank, financial year, category and KPI selections.
7. Compare individual bank performance with peer banks and calculated benchmarks.
8. Identify performance gaps and relative strengths or weaknesses.
9. Present financial information through an interactive and structured dashboard.

---

## Banks Covered

The project dataset includes the following selected Indian banks:

- Axis Bank
- HDFC Bank
- ICICI Bank
- Kotak Mahindra Bank
- State Bank of India

The exact metrics available for analysis depend on the financial information incorporated into the project dataset.

---

## Data Sources

The financial information used in the project was collected from publicly available bank financial reports and disclosures.

Relevant financial metrics were identified from these reports and organized into a structured dataset for comparative analysis.

The source information was organized and standardized before being incorporated into the Power BI analytical model.

### Data Flow

**Bank Financial Reports → Data Organization & Standardization → Data Consolidation → Power Query Transformation → Power BI Data Model → DAX Analysis → Dashboard**

---

## Data Preparation

The data preparation process involved organizing financial information into a consistent structure across banks, financial years, categories and KPIs.

Key preparation activities included:

- Organizing bank-level data
- Standardizing bank names
- Standardizing financial year information
- Standardizing KPI names
- Structuring metric values
- Consolidating bank-level datasets
- Preparing data for Power BI
- Maintaining consistent units for comparable metrics

**Power Query** was used for data transformation and consolidation before analysis in Power BI.

**Excel** was used during the data organization, validation and preparation process.

---

## Data Model

The Power BI solution uses a structured analytical data model consisting of fact tables, dimension tables and supporting tables.

### Core Analytical Tables

| Table | Purpose |
|---|---|
| `Fact_Bank_Metrics` | Consolidated bank financial metrics |
| `Dim_Bank` | Bank information and bank selection |
| `Dim_Date` | Financial-year and time-based analysis |
| `Dim_Metrics` | KPI and metric information |
| `KPI_Details` | KPI-level analytical presentation |
| `Executive_Insights` | Dynamic insight generation |
| `Bank Selector` | Selected-bank analysis and comparison |
| `Measures 2` | Analytical measures used by the report |
| `Variance_Steps` | Variance-related analytical calculations |
| `Waterfall Steps` | Waterfall and variance presentation logic |

The model also contains bank-specific source tables used during data preparation and modelling.

### Fact Table

The central analytical table is `Fact_Bank_Metrics`.

It contains consolidated financial metrics used by the dashboard and allows financial values to be analysed across dimensions such as:

- Bank
- Financial Year
- Category
- KPI

This structure supports reusable calculations and filtering across the report.

### Dimension Tables

**`Dim_Bank`**  
Contains bank-level information used for filtering, selection and peer comparison.

**`Dim_Date`**  
Supports financial-year analysis and year-over-year calculations.

**`Dim_Metrics`**  
Contains KPI and metric information used to organize and filter financial measures.

---

## DAX & Analytical Logic

DAX was used to create dynamic measures for KPI analysis, trend analysis, comparisons, rankings and benchmarking.

The calculations respond to the filter context selected by the user.

### Total Value

```DAX
Total Value =
SUM(Fact_Bank_Metrics[Metric_Value])
