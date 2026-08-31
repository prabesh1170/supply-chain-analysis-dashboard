# Data Dictionary — Supply-chain
| Column | Description | Data Type |
|---|---|---|
| order_number| Unique identifier for each order | Number |
| order_date | Date the order was placed | Date |
| shipment_date | Date the order was sent for delivery | Date |
| delivery_date | Date the order was delivered | Date |
| customer_id | Unique identifier for each customer | Text |
| customer_region | From which region the customer is from | Text |
| customer_country | From which country the customer is from | Text |
| product_id | Unique identifier for each product | Text |
| product_name | Name of the product | Text |
| product_category | Category or type of product  | Text |
| supplier_id | Unique identifier for the supplier | Text |
| supplier_name | Name of the Supplier who provides the product | Text |
| supplier_region | From which region the supplier is from | Text |
| warehouse_id | Unique identifier for each warehouse | Text |
| warehouse_location | Place the warehouse is located | Text |
| transportation_mode | Medium of transport used for delivery | Text
| order_quantity | Order quantity from the customer |  Number |
| unit_Price | Price per product | Number |
| total_cost | Total cost of the product | Number |
| shipping_cost | Cost to deliver the product | Number | 
| delivery_time_days | Time it takes to deliver the product | Number |
| inventory_level | Number of stock that is in the warehouse | Number |
| order_status | Status of the order that is sent for delivery | Text |
| profit | Profit from the products that were delivered | Number |



Note: Delivery Days in the table are from the shipment date to the delivery date.
