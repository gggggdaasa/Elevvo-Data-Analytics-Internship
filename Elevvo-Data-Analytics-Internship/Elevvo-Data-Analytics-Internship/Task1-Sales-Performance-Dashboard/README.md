# Task 1: Sales Performance Dashboard Using Excel

**Level:** 1 · **Tools:** Microsoft Excel

## Objective
Import a raw sales dataset into Excel, clean and organize it, summarize key metrics
(total revenue, units sold, monthly trends) using pivot-style formula tables, and
visualize overall performance with clean, readable charts.

## Dataset
9,800 US retail orders (2015–2018), the classic "Sample Superstore" schema:
Order ID, Order Date, Ship Date, Ship Mode, Customer, Segment, Region, Product,
Category, Sub-Category, and Sales.

**Note:** the source file did not include `Quantity`, `Discount`, or `Profit` —
three columns the task explicitly requires. These were modeled statistically
using realistic category-level margins and common retail discount tiers, with
every assumption documented in the workbook's **Data Notes** tab. All profit/margin
figures should be read as illustrative for practicing the dashboard build, not as
real financial results.

## What's inside `Sales_Performance_Dashboard.xlsx`
- **Dashboard** — executive KPI cards (Revenue, Profit, Units Sold, Order Lines,
  Avg Sale/Line) + 4 charts: Monthly Revenue Trend, Revenue by Region,
  Revenue by Category, Month-over-Month Change %
- **Pivot Summary** — formula-driven summary tables (SUMIFS/COUNTIFS) by Region,
  Category, and Month (48 months), with MoM and YoY % change — fully live, zero
  hardcoded numbers
- **Raw Data** — the cleaned 9,800-row dataset as a native Excel Table
- **Data Notes** — full cleaning log and methodology for the estimated columns

## Key Results
- **$2,261,536.78** total revenue analyzed across 9,800 order lines
- **51,574** units sold
- **$195,818.82** total (modeled) profit
- Clear seasonal pattern in the monthly trend, consistent with retail buying cycles

## Bonus items completed
- ✅ Month-over-month (MoM) and year-over-year (YoY) % change columns
- ⬜ Slicers (native Excel feature — add manually via Insert → Slicer if needed for submission)
