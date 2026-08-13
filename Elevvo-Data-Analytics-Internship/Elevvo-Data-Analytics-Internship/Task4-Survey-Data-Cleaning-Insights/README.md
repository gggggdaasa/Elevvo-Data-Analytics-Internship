# Task 4: Data Cleaning and Insight Generation from Survey Data

**Level:** 2 · **Tools:** Python, pandas, seaborn, matplotlib

## Objective
Work with real-world survey data containing missing values, duplicates, and
inconsistent formatting. Clean the dataset, apply label encoding/mapping for
categorical variables, and extract meaningful insights about respondent behavior
and preferences.

## Dataset
[2021 Kaggle Machine Learning & Data Science Survey](https://www.kaggle.com/c/kaggle-survey-2021) —
25,973 real responses to a 42-question industry survey, sourced from a public GitHub
mirror of the original Kaggle competition data.

## Data Quality Issues Found & Fixed
| Issue | Found | Fix |
|---|---|---|
| Question-text row | Row 0 of the raw file is question text, not a response | Dropped before analysis |
| Duplicates | Checked across all 369 raw columns | 0 true duplicates found |
| Inconsistent formatting | Compensation mixed `"$0-999"` and `"25,000-29,999"` | Standardized by stripping `$` |
| Missing values | Industry/CompanySize/Compensation 37-41% missing | Filled with `"Not Specified"` instead of dropping ~40% of rows |
| Outlier durations | Some respondents show survey durations of hours | Flagged (not deleted) as `"Left Idle (>3hrs)"` — 1,047 rows |

**Label encoding applied to 5 ordinal fields:** Education, CodingExperience,
MLExperience, CompanySize, Compensation — each mapped to an ordered integer code.

## What's inside
- **`Survey_Insights.ipynb`** — full analysis: cleaning, label encoding, insight
  extraction, 7 visualizations (including a Top-5-Insights summary dashboard), fully
  executed with outputs embedded
- **`Survey_Insights_Summary.xlsx`** — organized Excel companion with 4 tabs:
  - **Dashboard** — 5 KPI cards + 4 native charts, all formula-driven
  - **Insights** — the Top 5 insights write-up + supporting Top-10-Countries and
    Language-Usage tables
  - **Data Cleaning** — full cleaning log and label-encoding documentation
  - **Clean Data** — all 25,973 respondents as a filterable Excel Table
- **`survey_clean.csv`** — the cleaned, encoded dataset
- **`charts/`** — all 7 visualizations exported as standalone PNGs

## Top 5 Insights
1. **India leads respondents** — 28.6% of all respondents, nearly 3x the United States (10.2%)
2. **Python dominates** — recommended as the first language by 78%, used regularly by 84%
3. **The field remains heavily male-skewed** — 79.3% Man vs. 18.8% Woman
4. **"Student" is the single most common role** — 26% of respondents, ahead of any employed title
5. **More coding experience predicts higher pay** — median compensation rises almost monotonically with experience
