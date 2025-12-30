# SaaS-E-Commerce-Analytics
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
## Tools
Microsoft Power BI
## Modelling
A star schema was implemented, with the Events table serving as the fact table and the Products and Customers tables as dimension tables. The model is also connected to a Date dimension to enable robust time-based analysis.
## Exploratory Data Analysis
### Pre Analysis Questions
-	How do total sales change by month?
-	Which channels bring in the most sales?
-	Which channels bring the most repeat (loyal) customers?
-	What percent of monthly sales comes from loyal customers?
-	Which products or plans sell the most?
-	Which products are most popular with loyal customers?
-	How long do customers wait before their second purchase?
-	Which discount codes are used most, and do they increase repeat purchases?
-	What is the average selling price (ASP) by country or currency?
-	Where do refunds happen most (by product or channel)?
-	Do annual plans bring higher revenue per customer than monthly plans?
-	Which add-ons are most often bought with core products (attach rate)?
## Insights
1. Revenue Performance

   Revenue grew from $4.29M (2024) to $5.09M (2025), driven by strong mid-year sales. Q2–Q3 remain the core revenue engine, while early-year and late-year months underperform.

   In 2025, Q1 rebounded strongly, Q2 became the peak quarter, and Q4 collapsed, signaling changing seasonality and the need for improved late-year marketing or retention strategies.

   June consistently emerged as the top month, highlighting mid-year as the critical period for acquisition and retention.

2. Pricing & Volume Synergy

   ASP +3.54% and Quantity Sold +14.40% in 2025 indicate a strong price-volume growth synergy.

   Customers are willing to pay more while buying more units, demonstrating both high perceived value and robust demand.

3. Billing Cycle and Discount Strategy
   Annual Plans dominate with over $8.2M, confirming the effectiveness of long-term, high-value commitments for cash flow and revenue stability.

   Monthly Plans ($853K) and One-Time Plans ($256K) contribute less, mainly providing flexible entry points.

   Discount Codes: Annual-plan codes have similar redemption volumes as monthly codes but generate far greater revenue impact. Monthly-plan codes are high-volume, low-return, opportunities to reduce discount depth and boost margins without hurting adoption. 
    
   One-time codes have minimal impact, indicating discounts aren’t key drivers.

4. Customer Loyalty & Segmentation

   99.83% of customers return for at least a second purchase.

   Consumer segment dominates, with Consumer and SOHO together contributing over 78% of total revenue, confirming a primarily B2C-driven business.

   Developer and Design Tools have universal appeal across segments, forming the core product growth drivers.

5. Vendor & Product Focus

   Microsoft ($2.99M) is the largest revenue driver, followed by AI Tools ($1.62M) and Adobe.
 
   Top revenue comes from annual subscriptions of Microsoft 365, Azure AI, and creative tools; reinforcing the Annual Plan strategy.
   
6. Acquisition Channels & Loyalty

   Organic acquisition drives the highest long-term loyalty, followed by Paid Search and Social.

   Retail Media contributes the least to repeat purchases.



