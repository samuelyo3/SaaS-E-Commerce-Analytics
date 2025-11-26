<img width="925" height="21" alt="image" src="https://github.com/user-attachments/assets/d0ad49b3-8fb0-4e0b-a93d-3d2732cc617c" /># SaaS-E-Commerce-Analytics
## Introduction
This project analyzes customer behaviour, and revenue performance for a software retail company offering subscription-based digital products such as Tableau Creator, Zendesk Suite, Figma Professional, and Microsoft 365 plans. The analysis covers years 2024 and 2025, with a goal of uncovering key insights that can support smarter marketing allocation, better pricing decisions, improved customer retention, and stronger revenue strategy.
## Dataset
The dataset (from the Onyx Data Challenge – November Edition) contains detailed SaaS e-commerce transactions for 2024–2025. It is organized into three related tables: Events, Products, and Customers.
#### Events Table
- event_id:	Unique identifier for each event/transaction record.
- event_type:	Type of event (e.g., order, invoice, renewal).
- event_date:	Timestamp when the event occurred.
- customer_id:	ID linking the event to a customer.
- product_id:	ID linking the event to a product.
- country:	Country of the customer at the time of purchase.
- latitude:	Latitude of customer location.
- longitude:	Longitude of customer location.
- region:	Region grouping (NA, EU, APAC, LATAM).
- channel:	Sales channel (Website, Direct Sales, Partner, Marketplace, etc.).
- payment_method:	Payment type (Credit Card, Invoice, PayPal, Wire).
- currency:	Transaction currency.
- quantity:	Number of units/seats purchased.
- unit_price_local:	Unit price in local currency before discounts.
- discount_code:	Discount or promo code applied.
- discount_local:	Total discount amount in local currency.
- tax_local:	Tax or VAT applied in local currency.
- net_revenue_local:	Net revenue after tax/discounts in local currency.
- fx_rate_to_usd: Exchange rate used to convert local currency to USD.
- net_revenue_usd:	Net revenue converted to USD.
- is_refunded:	Indicates if the transaction was refunded (True/False).
- refund_datetime:	Timestamp of refund event.
- refund_reason:	Explanation for the refund.
#### Products Table
- product_id:	Unique identifier for each product or plan.
- product_name:	Name of the software product or plan.
- category:	Product category (Analytics, AI Tools, Productivity, Design, Security, etc.).
- is_subscription:	Indicates subscription vs one-time purchase.
- billing_cycle:	Billing frequency (Monthly, Annual, One-Time).
- base_price_usd:	Standard list price in USD.
- first_release_date:	First release/availability date of the product.
- vendor	Product: vendor (Microsoft, Adobe, OpenAI, etc.).
- resale_model:	Sales model (Direct Resale, Marketplace, Affiliate).
- brand_safe_name:	Clean/standardized product name for reporting.
- product_name_orig:	Original product name from raw source.
- base_price_usd_orig:	Original list price before cleaning/normalisation.
- base_key:	Internal product grouping key.
- product_version:	Specific product version if available.
#### Customers Table
- customer_id:	Unique ID representing a customer.
- signup_date:	Date the customer first registered or joined.
- region:	Customer’s region (geographical category).
- currency_preference:	Preferred currency selected by the customer.
- segment:	Customer segment (Consumer, SOHO, SMB, Enterprise).
- acquisition_channel:	How the customer was acquired (Organic, Paid Search, Social, Email, Affiliate, Retail Media).
- age_band:	Customer age group (e.g., 18–24, 25–34).
- country:	Customer’s country of residence.
- country_latitude:	Latitude of the customer’s country centroid.
- country_longitude:	Longitude of the customer’s country centroid.
## 

