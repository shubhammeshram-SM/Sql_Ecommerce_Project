# Sql_Ecommerce_Project
E‑commerce Database & Analytics – SQL Project
A complete SQL schema and query set for an online store, covering users, products, orders, payments, reviews, and shipping. Includes sample data, common analytics queries, performance tips, and transaction logic.

📂 Schema Overview
Tables
Users – Customer details (name, email, phone, DOB, gender).

Categories – Hierarchical product categories (parent/child).

Products – Product info (name, description, price, stock, category).

Orders – Order header (user, date, status, total amount).

Order_Items – Line items (order, product, quantity, price at purchase).

Payments – Payment records (order, date, amount, method, status).

Reviews – Product reviews (user, product, rating, comment, date).

Shipping – Shipping details (order, address, city/state/pincode, shipped/delivered dates, status).

Key Design Choices
All tables have created_at and updated_at timestamps for auditing and ETL.

Orders.total_amount and Order_Items.price_at_purchase store snapshot prices for reporting.

Categories supports nested categories via parent_category_id.

Reviews.rating has a CHECK constraint to enforce 1–5 stars.

