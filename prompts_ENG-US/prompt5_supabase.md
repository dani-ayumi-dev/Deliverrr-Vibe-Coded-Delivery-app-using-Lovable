## ⚠️ IMPORTANT

This project is cumulative.

All existing and future features must use this database structure.

---

# SUPABASE

Create the complete database structure for Deliverrr.

---

## PROFILES

id

name

email

phone

role

Allowed values:

- admin
- customer

preferred_language

receive_whatsapp_notifications

created_at

---

## ESTABLISHMENTS

id

restaurant_name

cnpj

phone

email

address

zip_code

latitude

longitude

delivery_radius_km

logo_url

created_at

---

## CUSTOMERS

id

profile_id

address

zip_code

latitude

longitude

created_at

---

## CATEGORIES

id

establishment_id

name_pt

name_en

description_pt

description_en

display_order

---

## PRODUCTS

id

category_id

name_pt

name_en

description_pt

description_en

image_url

price

active

featured

created_at

---

## PROMOTIONS

id

product_id

discount_percentage

start_date

end_date

---

## ORDERS

id

customer_id

establishment_id

status

Allowed values:

- pending
- queued
- preparing
- delivering
- completed
- cancelled

subtotal

delivery_fee

discount

total

distance_km

created_at

---

## ORDER_ITEMS

id

order_id

product_id

quantity

unit_price

---

## CUSTOMER_REVIEWS

id

order_id

customer_id

establishment_id

rating

Allowed values:

- 0
- 1
- 2
- 3
- 4
- 5

comment

created_at

---

## WHATSAPP_LOGS

id

order_id

destination_phone

message

delivery_status

created_at

---

## ADMIN_ALERTS

id

establishment_id

customer_review_id

alert_type

Allowed values:

- low_rating
- delivery_issue
- complaint
- system

message

read

created_at

---

## CHAT_MESSAGES

id

customer_id

establishment_id

sender_type

Allowed values:

- customer
- admin

message

created_at

Allows restaurant owners to communicate directly with customers through the WhatsApp Chat section.

---

## METRICS

Create automatic database views for:

- Orders Per Day
- Orders Per Week
- Orders Per Month
- Average Ticket Size
- Best-Selling Product
- Least-Selling Product
- Daily Revenue
- Monthly Revenue
- Average Customer Rating
- Total Reviews Received
- Positive Reviews
- Negative Reviews
- Customer Satisfaction Trend

---

## CUSTOMER FEEDBACK ANALYTICS

Automatically calculate:

- Overall Average Rating
- Rating Distribution
- Percentage of 5-Star Reviews
- Percentage of 4-Star Reviews
- Percentage of 3-Star Reviews
- Percentage of 2-Star Reviews
- Percentage of 1-Star Reviews
- Percentage of 0-Star Reviews

These metrics must feed:

- Dashboard
- Elvisys (Admin Mode)
- Customer Satisfaction Reports

---

## BUSINESS RULES

When a customer submits a review:

- Save the rating.
- Save the optional comment.
- Associate the review with the completed order.
- Update restaurant rating metrics.
- Update dashboard statistics.

If the customer submits:

⭐ 0 Stars

Automatically:

- Create a record in ADMIN_ALERTS.
- Display an alert in the Dashboard.
- Display a notification in Elvisys (Admin Mode).
- Mark the review as requiring attention.

---

## SECURITY

Implement:

- Foreign Keys
- Database Indexes
- Row-Level Security (RLS)
- Access Policies
- Migrations
- Seed Data

---

## INITIAL SEED DATA

Restaurant:

Bella Napoli

Categories:

- Appetizers
- Pasta
- Pizzas
- Desserts
- Drinks

Sample Products:

- Traditional Bruschetta
- Bolognese Lasagna
- Spaghetti Carbonara
- Margherita Pizza
- Calabrese Pizza
- Tiramisù
- Panna Cotta
- Canned Soft Drink
- Fresh Juice

Create placeholder images for all products.

Create sample promotions.

Generate sample orders, reviews, dashboard metrics, and customer feedback so the administrative area is immediately usable for testing.