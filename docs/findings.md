# Findings

Data: UCI Online Retail, Dec 2010 – 9 Dec 2011 (cleaned: 534,131 rows)
Definitions: real products only (non-products excluded). Dec 2011 is a partial month (1–9 Dec).

## Answers to the COO's questions

| COO's question | Answer |
|---|---|
| Are we busier? | Yes. Orders more than doubled from Jan to Nov 2011 (+137%), mostly driven by the Christmas season. Sep–Nov brought in 35% of the year's sales. |
| Are we making more money? | Gross sales grew in line with orders. The average order value stayed about the same (£436 in Jan → £453 in Nov, +4%). Profit cannot be measured (no cost data). |
| Are cancellations out of control? | No. Cancellations are about 3–5% of sales, below the 5% threshold. The spikes in Jan (13.7%) and Dec (28.3%) were each caused by one huge order cancelled within minutes, likely typing errors. |
| Have big customers gone quiet? | 20 of the top 436 customers (top 10%) have not ordered in 90+ days, about £157K of past revenue. The Netherlands and Ireland customers mentioned by the COO are still active. |
| Other finding | About 15% of revenue (£1.5M) comes from guest buyers with no Customer ID, so we cannot identify or follow up with them. |

## Key numbers

| Metric | Value |
|---|---|
| Gross sales (Dec 2010 – Dec 2011) | £10,247,219 |
| Cancellations (whole period) | 4.6% of sales (3.0% excluding one £168K error) |
| Top 10% of customers' share of identified revenue | 60% |
| Big customers gone quiet (90+ days) | 20 (£156,855 of past revenue) |

## Hypotheses scorecard

| # | Hypothesis | Result |
|---|---|---|
| 1 | Customers are placing smaller orders | Not supported (AOV +4%) |
| 2 | New small customers drive order growth | Not tested yet |
| 3 | Growth is mainly Christmas season | Supported |
| 4 | A few big customers bring most of the revenue | Supported (top 10% = 60%) |
| 5 | Cancellations come from a few orders | Supported (2 orders caused the spikes) |
