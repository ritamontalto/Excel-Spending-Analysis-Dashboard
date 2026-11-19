# Excel Budget Tracker & Spending Analysis Dashboard

## Executive Summary

Good financial decisions start with the same discipline as good operations management: define the KPIs, track them consistently and look for the cost drivers. This project applies that approach to personal finance. I built a multi-sheet Excel workbook for a hypothetical household that records daily transactions, consolidates them into monthly and yearly views and turns them into an interactive dashboard with pivot tables, slicers, dynamic charts and dropdown lookups. The workbook covers 6 years of yearly income and expense history (2019-2024), a month-by-month view of 2019, a detailed transaction log and a separate trip budget.

## Business Problem

An individual wants to stop reacting to their bank balance and start managing their budget proactively. Spending is spread across many small transactions, so it is hard to see where the money actually goes, whether it is trending up or down and whether savings goals are being met. I assumed the user would like to understand:

- Where does the money go and which categories drive total spending?
- How has income and spending evolved over the years?
- Is the household saving consistently and is the surplus growing or shrinking?
- Which months are the most and least expensive?
- How can an event, such as a trip, be tracked without distorting the regular budget?

## Workbook Structure

| Sheet | Purpose |
|---|---|
| **Monthly Tracker** | Transaction log (date, item, amount, category) for income and expenses, with a monthly balance, a pivot table by category and a linked chart |
| **Year Expenses at a glance** | Monthly expense totals for 2019, with a yearly total, shown in a scrollable and zoomable chart |
| **Yearly income** | Income by type (Salary, Passive, Other) for 2019-2024, with a year selector |
| **Yearly expenses** | Expenses across 11 categories for 2019-2024, with a category and year lookup |
| **Trip expenses** | Itemized budget for a city trip, with a breakdown by payment method |
| **List** | Category master list that feeds the dropdown menus and keeps categories consistent |

## Methodology

```
Transaction Data Entry
        ↓
Standardized Categories (dropdown validation)
        ↓
Monthly & Yearly Consolidation
        ↓
Pivot Tables, Slicers & Dynamic Charts
        ↓
Insights & Recommendations
```

**Data Structure & Validation**
- Defined one master list of 11 expense categories and used data validation dropdowns so every transaction is classified consistently
- Separated income, expense and one trip data so each can be analyzed on its own
- Used `SUM` totals on every sheet to calculate balances for each period
- Checked that the monthly totals on the year-at-a-glance sheet add up to the 2019 yearly expense total (€34,483), and that the February log matches the February monthly figure

**Analysis & Reporting**
- Used pivot tables to summarize spending by category and filtered them with slicers
- Built `INDEX` / `MATCH` and `CHOOSE` / `MATCH` lookups, driven by dropdowns, to return any category and year combination instantly
- Calculated income, expense, balance and savings KPIs for each period
- Compared category weight and growth across the 6-year history

**Dashboard Design**
- Built dynamic charts on named ranges, with scroll and zoom controls to browse the year at a glance
- Added a pivot chart that updates when new transactions are added and the pivot is refreshed
- Added a payment method breakdown for the trip budget

## Key Findings

*Figures below come from the workbook (all amounts in €).*

**Where does the money go?**

Spending is concentrated in a few categories. In 2024, Utilities (rent, insurance and bills) made up 40.7% of total expenses, followed by Transport (16.9%), Groceries (10.4%) and Vacation (10.1%). These four categories account for roughly 78% of the budget. Discretionary categories such as Dining, Shopping and Leisure together represent less than 7%.

**How have income and spending evolved?**

Both are very stable. Total income moved from €39,536 (2019) to €39,667 (2024), +0.3%, with Salary consistently about 92% of the total. Total expenses moved from €34,483 to €34,215, -0.8%. The cost structure is largely fixed, so there is little room for savings from a few small adjustments.

**Is the household saving?**

The yearly surplus (income minus all expenses, savings contributions included) ranged from 10.9% of income in 2021 to 13.7% in 2024. However, the dedicated Savings category declined from €2,678 in 2021 to €2,006 in 2024 (-25%), while Vacation spending grew 12.9% between 2019 and 2024 (€3,064 to €3,459). Part of the improving surplus is therefore unallocated cash rather than money set aside.

**Which months are the most expensive?**

Monthly spending in the 2019 year-at-a-glance view averages about €2,874. July is the peak (€3,546, 23% above average), followed by December (€3,214) and March (€3,087), while June is the lowest (€2,539). The July spike lines up with summer travel and December with the holidays, so these predictable costs should be planned in advance rather than absorbed from the monthly balance.

**What does a typical month look like?**

In the February transaction log, income of €3,100 against €2,768 of expenses left a balance of €332 (10.7% of income). Utilities alone accounted for 48% of that month's spending, and the month's €2,768 total matches the February figure in the year-at-a-glance view.

**How can an event be tracked?**

The trip budget totals €767. Flight and hotel represent 58% of it. 75% of the spending went through debit card, with the remainder split between Apple Pay and cash. Tracking it on a separate sheet keeps these exceptional costs from distorting the regular monthly analysis.

## Recommendations

*Written for the hypothetical user of this budget.*

- **Focus on fixed costs first:** Utilities and Transport represent about 58% of spending, so a review of insurance, utility and transport contracts has more impact than cutting small discretionary purchases.
- **Automate savings:** Savings contributions fell while the surplus grew. Setting a fixed transfer at the start of each month, as a share of income, would protect the savings goal.
- **Budget for seasonality:** July and December run 12-23% above the monthly average. Setting aside a fixed monthly amount for them avoids drawing on that month's balance.
- **Plan vacation as a dedicated line:** Vacation is the fastest-growing major category, so it deserves its own annual target.
- **Keep tracking on a regular schedule:** Logging transactions weekly and refreshing the pivot tables keeps the dashboard reliable as a decision tool.

## Skills Demonstrated

**Analytics**
- KPI definition and monitoring
- Cost driver analysis
- Trend and variance analysis
- Seasonality analysis
- Insight generation and recommendations

**Excel**
- Pivot tables and pivot charts
- Slicers
- Dynamic named ranges and dynamic charts
- Form controls (scroll and zoom)
- Data validation and dropdown lists
- `INDEX` / `MATCH`, `CHOOSE`, `SUM` and lookup formulas
- Conditional formatting
- Dashboard design and data visualization

## Data

The data is illustrative and was created for portfolio purposes. It contains no real financial or personal information about any individual. It was built to simulate a realistic household budget, including recurring bills, daily purchases and a trip. All structure, formulas, pivot tables, charts, analysis and recommendations were independently designed and implemented by me.

## Project Files

- Budget_Tracker.xlsx: Complete workbook with all sheets, pivot tables and charts
- Screenshots: Preview of each dashboard sheet
