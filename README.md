# Sales Performance Dashboard (Excel)

A data cleaning and dashboard project in Microsoft Excel. It turns a messy raw sales file of 51 order records (January – May 2026) into a cleaned dataset, a set of PivotTables and an interactive sales dashboard, and ends with five business insights and recommendations.


## Business Questions

- How much revenue and profit is the business making, and where does it come from?
- Which categories, products, cities and salespeople perform best, on revenue and on profit?
- Where are margins being lost, and what should the business do about it?

## Dataset

- **Raw data:** 51 order records with order and ship dates, salesperson, town and city, product, category, quantity, unit price, discount %, unit cost, customer type and payment method
- **Cleaned data:** 45 records, 7 cities, 8 products, 3 categories (Accessories, Electronics, Furniture), 10 salespeople
- **Period:** January – May 2026

## Tools and Excel Skills Used

- Data cleaning (removing blanks and duplicates, trimming text, fixing formats)
- Excel Tables with structured references
- Calculated columns: Gross Sales, Discount Amount, Revenue, Total Cost, Profit, Order Value Category, Profit Status
- Summary formulas: `SUMIF`, `COUNTIF`, `COUNTIFS`, `SUM`, `AVERAGE`, `MAX`, `MIN`
- PivotTables and PivotCharts
- Slicer and an interactive dashboard

## Data Cleaning Summary

| Issue | Action |
| --- | --- |
| 4 records with missing Order IDs | Excluded from the cleaned dataset |
| 2 duplicate orders (ORD044, ORD046) | Removed one copy of each |
| Inconsistent Order ID format (`ORD0 06`) | Standardised to `ORD006` |
| Extra spaces in salesperson, town and product fields | Trimmed and standardised |
| Unit Price recorded as `35  000` | Converted to a numeric value, 35000 |
| 3 orders shipped before they were ordered (ORD033, ORD034, ORD045) | Flagged for verification against the source |

The full log is in the `Cleaning Log` sheet.

## Key Results


| Metric | Result |
| --- | --- |
| Total revenue | 40,249,900 |
| Total profit | 8,655,900 |
| Orders | 45 |
| Units sold | 559 |

## Business Insights

1. **Electronics earns the most revenue but has the weakest margin.** It brings in 55.0% of revenue at a 15.4% margin, while Accessories contributes 21.4% of revenue but 35.9% of profit (36.1% margin).
2. **Laptops lead revenue, but Mouse is the most profitable per unit of sales.** Laptops have a 10.6% margin, while Mouse earns 43.1%.
3. **Revenue is concentrated in two cities.** Lagos and Abuja provide 56.4% of revenue. Ibadan and Port Harcourt have the lowest margins (15.1% and 16.9%).
4. **The top salesperson by revenue is not the top by profit.** Tolu leads on revenue but ranks 5th on profit. Emeka earns the highest profit at a 26.9% margin.
5. **Large orders drive revenue but dilute profit.** The 12 High Value orders bring in 44.9% of revenue at a 15.2% margin, compared with 26.6% for Standard orders.

## Recommendations

- Review supplier costs, pricing and discounts on Electronics and laptops, and bundle Accessories with Electronics sales.
- Protect Lagos and Abuja, review pricing in Ibadan and Port Harcourt, and grow Kaduna, where margins are strong.
- Evaluate salespeople on profit as well as revenue.
- Set discount approval limits or minimum margins on large orders.

## Limitations

- The analysis rests on 45 orders over five months, so the patterns should be confirmed with more data.
- Three shipping-date anomalies are still pending verification. They do not affect the revenue and profit figures.

## Repository Structure

```
├── data/            # Raw data and cleaned data
├── analysis/        # Excel workbook (Raw Data, Cleaned Data, Pivots, Dashboard, Summary, Cleaning Log, Business Insights)
├── images/          # Dashboard screenshots
└── README.md
```

## Author

**Ibraheem Tunde Lawal**
Microbiology graduate and data analyst, Kwara State University
