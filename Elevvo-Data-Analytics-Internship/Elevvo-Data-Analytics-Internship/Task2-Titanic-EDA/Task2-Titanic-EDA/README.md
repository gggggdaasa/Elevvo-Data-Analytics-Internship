# Task 2: Exploratory Data Analysis on the Titanic Dataset

**Level:** 1 · **Tools:** Python, pandas, seaborn, matplotlib

## Objective
Explore the classic Titanic dataset, clean it, generate summary statistics and
group-based insights (e.g. survival by gender/class), and visualize key patterns
and correlations.

## Dataset
891 real passengers from the Titanic's April 1912 voyage — the classic Kaggle
"Titanic: Machine Learning from Disaster" dataset, sourced from a public GitHub
mirror: `datasciencedojo/datasets`.

## What's inside
- **`Titanic_EDA.ipynb`** — the full analysis: cleaning, feature engineering,
  summary statistics, group-based insights, and 8 visualizations, fully executed
  with outputs embedded (open directly on GitHub to view results, no need to re-run)
- **`Titanic_EDA_Summary.xlsx`** — an organized Excel companion with 5 tabs, all
  built as real Excel Tables:
  - **Dashboard** — 5 KPI cards + 4 native charts (Survival by Sex×Class, by Age
    Group, by Family Size, and overall Died/Survived split), all formula-driven
  - **Data Cleaning** — before/after missing-value table + method used per column
  - **Raw Data** — the original 891-row dataset as a Table
  - **Clean Data** — the cleaned dataset with engineered features as a Table
  - **Summary Tables** — 7 group-based insight tables (by Sex, Class, Sex×Class,
    Age Group, Travel Status, Port, Family Size)
- **`titanic.csv`** — the original raw dataset
- **`titanic_clean.csv`** — the cleaned dataset with engineered features
- **`charts/`** — all 8 visualizations exported as standalone PNGs

## Cleaning approach
- **Age** (177 missing) — imputed with the median *within each Pclass + Sex group*
- **Embarked** (2 missing) — filled with the mode
- **Cabin** (687 missing, ~77%) — converted to a binary `Has_Cabin` flag instead
  of imputing, since it was too sparse to guess meaningfully

## Key Insights
1. **Sex was the strongest predictor of survival** — 74.2% for women vs. 18.9% for men
2. **Class amplified the effect** — 1st class women survived at 96.8%; 3rd class men at 13.5%
3. **Fare and class are tightly linked**, and both correlate with survival
4. **Small families survived more than solo travelers** (50.6% vs. 30.4%), but very large families saw survival drop again
5. **Children had a meaningfully higher survival rate** (57.9%) than adults or seniors
6. **`Has_Cabin` correlates with survival** — reinforcing the class effect

## Bonus items completed
- ✅ Survival rate visualized with bar plots (by sex, class, age group, family size)
- ✅ Survival rate heatmap (Sex x Passenger Class)
- ✅ Correlation heatmap across all numeric features
