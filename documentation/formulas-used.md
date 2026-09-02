
# Excel Functions Used

| Function | Purpose | Where Used |
|---|---|---|
| XLOOKUP + IFERROR | Look up supplier name/region by ID | SupplierSummary sheet |
| SUMIFS / COUNTIFS / AVERAGEIFS | Aggregate profit, order count, avg delivery time per supplier | SupplierSummary sheet |
| Nested IF | Classify orders as Profitable/Break-even/Loss | cleaned_data, Profit Classification column |
| FILTER | Dynamic live list of loss-making orders | LossWatchlist sheet |
| NETWORKDAYS | Calculate delivery time excluding weekends | cleaned_data, Business Days to Deliver column |
