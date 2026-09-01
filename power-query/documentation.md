
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
- Delivery Performance: The analysis shows that 55% of orders were delayed, while 27% were delivered on time and 18% had not yet been delivered.

- Most and Least Profitable Transport Modes: Railway is the most profitable transport mode, whereas Road is the least profitable.

- Average Delivery Time by Transport Mode: Sea transport has the fastest average delivery time, while Air transport has the slowest average delivery time.

- Region with the Highest Number of Delays and Cancellations: North America recorded the highest number of delays and cancellations, with 22 delays and 12 cancellations.

- Chart Recommendation: The Order Status by Customer Region chart should be presented as a 100% Stacked Column Chart. This format provides a clearer comparison of the proportional distribution of order statuses across the five regions, whereas a standard stacked column chart makes proportional differences more difficult to assess.
