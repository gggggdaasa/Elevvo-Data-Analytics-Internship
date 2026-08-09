# Task 3: Customer Segmentation Using RFM Analysis

**Level:** 2 · **Tools:** Python, pandas, seaborn, matplotlib

## Objective
Analyze customer behavior using Recency, Frequency, and Monetary (RFM) metrics, score
and group customers into segments, and suggest simple marketing ideas for each group.

## Dataset
[Online Retail Dataset (UCI)](https://archive.ics.uci.edu/ml/datasets/online+retail) —
541,909 e-commerce transactions from a UK-based online retailer, Dec 2010 – Dec 2011
(the same dataset used in the Tata x Forage Data Visualisation project).

## Cleaning
- Removed returns (`Quantity < 1`) and pricing errors (`UnitPrice < 0`)
- Dropped rows with no `CustomerID` (~24.6% of rows — guest checkouts that can't be
  attributed to a customer, so they're excluded from this customer-level analysis only)
- Result: **397,924 clean transaction rows across 4,339 unique customers**

## What's inside
- **`RFM_Analysis.ipynb`** — full analysis: cleaning, RFM calculation, quintile scoring,
  8-segment classification, 6 visualizations, and marketing recommendations, fully
  executed with outputs embedded
- **`RFM_Analysis_Summary.xlsx`** — organized Excel companion with 3 tabs, all built as
  real Excel Tables:
  - **Dashboard** — 5 KPI cards + 3 native charts (customers by segment, revenue by
    segment, revenue share), all formula-driven
  - **Segment Profile** — one row per segment with size, % of customers, % of revenue,
    average R/F/M, total revenue, and a suggested marketing action per segment
  - **RFM Customers** — all 4,339 customers with their individual R/F/M scores and
    assigned segment, as a filterable Excel Table
- **`rfm_customers.csv`** — the customer-level RFM dataset
- **`charts/`** — all 6 visualizations exported as standalone PNGs

## Segments & Key Numbers

| Segment | Customers | % of Revenue |
|---|---|---|
| Champions | 962 (22.2%) | **65.2%** |
| Loyal Customers | 498 (11.5%) | 10.0% |
| Potential Loyalists | 414 (9.5%) | 7.0% |
| Hibernating | 915 (21.1%) | 5.6% |
| At Risk | 276 (6.4%) | 4.9% |
| Can't Lose Them | 130 (3.0%) | 3.6% |
| Lost | 824 (19.0%) | 2.1% |
| New Customers | 320 (7.4%) | 1.6% |

## Key Takeaway
Champions are only 22% of customers but drive nearly two-thirds of revenue —
protecting and rewarding this group matters more than acquiring new customers. Lost
customers are the largest segment by count (19%) but contribute almost nothing to
revenue, so marketing spend is better redirected toward At Risk and Can't Lose Them,
where meaningful revenue is still recoverable.

## Bonus items completed
- ✅ RFM segments visualized with bar charts (segment size, revenue by segment)
- ✅ RFM segments visualized with heatmaps (customer count and avg spend, Recency x Frequency)
