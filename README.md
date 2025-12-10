# Data Science Job Salaries Analysis

Exploratory data analysis and machine learning project analyzing salary trends in the data science job market using 607 job records from 2020-2022.

## Project Overview

This project analyzes data science job salaries to uncover trends, identify key salary drivers, and build predictive models. The analysis covers salary distributions across experience levels, work types, company sizes, and geographic locations.

## Key Findings

| Metric | Value |
|--------|-------|
| Average Salary | $110,610 |
| Median Salary | $100,000 |
| Salary Range | $2,859 - $600,000 |

### Experience Level Impact
- **Executive**: $199,392 avg
- **Senior**: $138,375 avg
- **Mid**: $87,793 avg
- **Entry**: $61,643 avg

### Work Type Analysis
- Remote jobs pay highest (~$120,763 avg)
- 61% of positions are fully remote
- Hybrid positions have lowest average salary

### Top Insights
1. Executive-level earns roughly 3x more than entry-level
2. Remote work dominates the market and pays better
3. Large companies pay slightly higher salaries
4. US has the most job opportunities
5. Data Scientist is the most common job title

## Project Structure

```
├── DS_Salaries_Analysis.ipynb    # Main analysis notebook
├── ds_salaries.csv               # Raw dataset
├── cleaned_data/
│   └── ds_salaries_cleaned.csv   # Processed dataset
├── visualizations/
│   ├── 01_salary_distribution.png
│   ├── 02_salary_by_experience.png
│   ├── 03_salary_by_worktype.png
│   ├── 04_salary_by_company_size.png
│   ├── 05_top_job_titles.png
│   ├── 06_yearly_trends.png
│   ├── 07_geographic_analysis.png
│   ├── 08_distributions.png
│   ├── 09_correlation_heatmap.png
│   ├── 10_worktype_size_salary.png
│   ├── 11_ml_evaluation.png
│   └── 12_dashboard.png
└── README.md
```

## Dataset

The dataset contains 607 data science job records with the following features:

| Column | Description |
|--------|-------------|
| work_year | Year of the salary data (2020-2022) |
| experience_level | Entry, Mid, Senior, Executive |
| employment_type | Full-time, Part-time, Contract, Freelance |
| job_title | Specific job role |
| salary_in_usd | Annual salary in USD |
| remote_ratio | Remote work percentage (0, 50, 100) |
| company_location | Country of the company |
| company_size | Small, Medium, Large |

## Machine Learning Models

Two models were trained for salary prediction:

| Model | R² Score | MAE |
|-------|----------|-----|
| Linear Regression | 0.319 | $37,216 |
| Random Forest | 0.282 | $33,513 |

**Top Predictors:**
1. Company Location
2. Job Title
3. Experience Level


Running all cells will automatically:
- Create `visualizations/` and `cleaned_data/` folders
- Generate all 12 visualization PNGs
- Save the cleaned dataset
- Train and evaluate ML models

## Technologies Used

- Python 3.8+
- Pandas
- NumPy
- Matplotlib
- Seaborn
- Scikit-learn

