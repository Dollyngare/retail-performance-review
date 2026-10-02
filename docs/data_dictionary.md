## First look findings

- Total rows: 541,909
- Date range: 1 Dec 2010 – 9 Dec 2011 (Dec 2011 is not a full month)
- CustomerID: 25% empty, probably guest checkouts. Keep for revenue, exclude for customer analysis.
- Description: <1% empty. Some rows have no description and price 0 (junk).
- Quantity: min -80,995, max 80,995. One order of 80,995 units (£168,470) was cancelled 12 minutes later (581483 / C581484).
- Cancellations: InvoiceNo starting with "C".
- UnitPrice: min -11,062.06 ("Adjust bad debt", StockCode B), max 38,970 ("Manual", StockCode M). Not real sales.
- UnitPrice = 0: 2,515 rows. Need to check.
- Non-product StockCodes exist (B, M, others). Separate them from product sales.
- Countries: 38
