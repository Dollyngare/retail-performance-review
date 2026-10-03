# Cleaning Log

Every change made to the raw data, in order.
Raw file: data/raw/Online Retail.xlsx | Tool: Excel Power Query | Query: sales_clean

| # | Issue found | Rows affected | Action taken | Reason |
|---|---|---|---|---|
| 1 | Wrong column types | All | InvoiceNo, StockCode, CustomerID set to Text | IDs are labels, not numbers |
| 2 | Extra spaces/hidden characters in Description | 12 product names merged | Trim + Clean | Same product was counted as different products |
| 3 | Exact duplicate rows | 5,268 | Removed | Duplicates double-count revenue |
| 4 | Cancellations and adjustments mixed with sales | 9,254 (9,251 cancellations, 3 adjustments) | Added TransactionType column (Sale / Cancellation / Adjustment) | Flag instead of delete, so we can include or exclude them per question |
| 5 | Non-product codes (POST, D, M, B, AMAZONFEE, etc.) | 2,944 | Added ProductFlag column (Product / Non-product) | Exclude from product analysis |
| 6 | Rows with UnitPrice = £0 (stock adjustments, staff notes, blank descriptions) | 2,510 | Removed | Not sales; inflated row and order counts |
| 7 | No revenue column | All | Added Revenue = Quantity × UnitPrice | Check: order 581483 (+£168,469.60) and cancellation C581484 (-£168,469.60) cancel out |
| 8 | No month grouping | All | Added YearMonth (first day of month) | Monthly trends; keeps Dec 2010 and Dec 2011 separate |

## Row count check
| Stage | Row count |
|---|---|
| Raw data | 541,909 |
| After removing duplicates | 536,641 |
| After removing £0 price rows | 534,131 |
| Total rows removed | 7,778 (1.4%) |

## Known issues (not fixed)
- 25% of rows have no CustomerID (likely guest checkouts). Kept for revenue, excluded from customer analysis.
- Some StockCodes have more than one Description (4,070 codes vs 4,212 descriptions).
- December 2011 is a partial month (data ends 9 Dec 2011).
