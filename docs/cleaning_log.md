| 1 | Wrong column types | All | InvoiceNo, StockCode, CustomerID set to Text | IDs are labels, not numbers |
| 2 | Extra spaces/hidden characters in Description | 12 product names merged | Trim + Clean | Same product was counted as different products |
| 3 | Exact duplicate rows | 5,268 | Removed duplicates | Duplicates double-count revenue |
