
# Power Query Steps — Supply Chain Data

1. Loaded tbl_SupplyChain into Power Query, verified data types (dates were text-displayed-as-date in Excel; confirmed true date type in Power Query)
2. Verified column quality - 100% valid, no duplicates on Order ID
3. Renamed 'Delivery Time Days' to 'Shipment to Delivery Days' (found it measures shipment-to-delivery, not order-to-delivery)
4. Added custom column 'Order to Delivery Days' = Delivery Date - Order Date
5. Added custom column 'Delivery Performance':
   - Not Yet Delivered (if Order Status != Delivered)
   - On Time (if Order to Delivery Days <= 7)
   - Delayed (if Order to Delivery Days > 7)
6. Validated: 407 On Time, 829 Delayed, 264 Not Yet Delivered (totals 1500, matches full dataset)


## PivotTable Findings — Supply Chain

### Delivery Performance
- Delayed: 829 (55%)
- On Time: 407 (27%)
- Not Yet Delivered: 264 (18%)

### Profit by Transportation Mode
- Rail: $1,966,012.59 (highest)
- Sea: $1,836,152.83
- Air: $1,788,199.46
- Road: $1,666,838.01 (lowest)

### Average Delivery Time by Transportation Mode (Days)
- Air: 6 (fastest)
- Road: 9
- Rail: 12
- Sea: 20 (slowest)

**Note:** Rail is the most profitable mode despite being the second-slowest — profitability and delivery speed are not directly aligned in this data.

### Order Status by Region
| Region | Delivered | In Transit | Delayed | Cancelled | Total |
|---|---|---|---|---|---|
| North America | 271 | 25 | 22 | 12 | 330 |
| Middle East | 251 | 25 | 16 | 11 | 303 |
| Asia | 245 | 26 | 21 | 9 | 301 |
| Africa | 240 | 25 | 13 | 9 | 287 |
| Europe | 229 | 22 | 16 | 12 | 279 |

- Asia has the highest proportion of Delayed orders (~7.0%)
- Europe has the highest proportion of Cancelled orders (~4.3%)
- Differences across regions are relatively small (within a few percentage points) — no single region stands out dramatically

### Chart Design Note
Chart 4 (Orders by Status per Region) was switched from plain Stacked Column to 100% Stacked Column for readability — comparing proportions across 5 regions was hard to read with raw counts.

