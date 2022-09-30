# study_projects
Product manager Vasily asked you to decide on the purchases made and to answer possible questions:

1. How many users do we have who lost a purchase only once?

2. How many orders per month, on average, are not delivered for different sets (display details for the set)?

3. At estimated prices, on which day of the week the goods are most often purchased.

4. How many of each user on average makes purchases per week (by months)? It is not necessary that there may not be an integer number of weeks within a month. For example, November 2021 has 4.28 weeks. And within the metrics, this must be taken into account.

5. Purpose of pandas, conduct a cohort analysis of users. Between January and December, identify the cohort with the highest retention rate for the 3rd month. Description can be found here.

6. Segmentation-based approaches are often used for qualitative analysis. python, build RFM user segmentation to qualitatively evaluate your audience. In clustering, you can choose possible metrics: R - time from the last purchase of the user to the increase in speed, F - the total number of purchases from the user for all time, M - the number of purchases for all time. Describe in detail how you built the clusters. For each RFM-segment on the structure of the boundaries of the metrics recency, frequency and monetary value for a combination of these clusters. An example of such a description: RFM-segment 132 (prescription = 1, frequency = 3, monetary = 2) has boundaries of prescription metrics from 130 to 500 days, frequency from 2 to 5 orders per week, monetary from 1780 to 3560 rubles per week. Description can be found here.

To solve the problem, preliminary data were proved and what was to be considered as obtaining was formulated. You can justify your choice with the help of payment facts, order statuses and other available data.

Files:

 olist_customers_datase.csv - table with the assignment of user IDs
customer_id - custom user ID

customer_unique_id - user ID (similar to passport number)

customer_zip_code_prefix - user's zip code

customer_city — user delivery city

customer_state - user's delivery state

olist_orders_dataset.csv - table of orders
order_id — order identifier (receipt number)

customer_id - custom user ID

order_status — order status

order_purchase_timestamp — order creation time

order_approved_at — order payment confirmation time

order_delivered_carrier_date - time of transferring the order to the logistics service

order_delivered_customer_date — order delivery time

order_estimated_delivery_date - estimated delivery date

olist_order_items_dataset.csv - commodity items included in orders
order_id — order identifier (receipt number)

order_item_id - item identifier within one order

product_id - product id (analogue of a barcode)

seller_id — id of the product manufacturer

shipping_limit_date - maximum date of delivery by the seller to transfer the order to the logistics partner

price - unit price

load_value — weight of goods

- An example of a data structure can be visualized by order_id == 00143d0f86d6fbd9f9b38ab440ac16f5

Unique order statuses in the olist_orders_dataset table:

created - created
approved - approved
billed - billed
processing - in the process of order assembly
shipped - shipped from warehouse
delivered - delivered
unavailable - unavailable
canceled - canceled
