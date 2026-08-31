
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
