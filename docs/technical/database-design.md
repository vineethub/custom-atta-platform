# Database Design

## Overview

The database stores users, grains, custom blends, orders, payments, and inventory information.

Database Engine: PostgreSQL

---

# users

Stores customer accounts.

| Column     | Type      |
| ---------- | --------- |
| id         | bigint    |
| name       | varchar   |
| email      | varchar   |
| phone      | varchar   |
| password   | varchar   |
| status     | boolean   |
| created_at | timestamp |
| updated_at | timestamp |

---

# grains

Master table containing nutritional and pricing information.

| Column            | Type      |
| ----------------- | --------- |
| id                | bigint    |
| name              | varchar   |
| slug              | varchar   |
| description       | text      |
| protein_per_100g  | decimal   |
| fiber_per_100g    | decimal   |
| calories_per_100g | decimal   |
| price_per_kg      | decimal   |
| stock_kg          | decimal   |
| is_active         | boolean   |
| created_at        | timestamp |
| updated_at        | timestamp |

Examples:

* Wheat
* Ragi
* Jowar
* Bajra
* Oats
* Chana
* Soybean
* Barley

---

# blends

Stores custom blend definitions.

| Column         | Type            |
| -------------- | --------------- |
| id             | bigint          |
| user_id        | bigint nullable |
| name           | varchar         |
| total_protein  | decimal         |
| total_fiber    | decimal         |
| total_calories | decimal         |
| price_per_kg   | decimal         |
| created_at     | timestamp       |
| updated_at     | timestamp       |

---

# blend_items

Stores grain composition.

| Column     | Type    |
| ---------- | ------- |
| id         | bigint  |
| blend_id   | bigint  |
| grain_id   | bigint  |
| percentage | decimal |

Example:

Blend #1

* Wheat 40%
* Ragi 20%
* Oats 15%
* Chana 15%
* Soybean 10%

Total must equal 100%.

---

# addresses

Stores delivery addresses.

| Column         | Type    |
| -------------- | ------- |
| id             | bigint  |
| user_id        | bigint  |
| full_name      | varchar |
| phone          | varchar |
| address_line_1 | varchar |
| address_line_2 | varchar |
| city           | varchar |
| state          | varchar |
| postal_code    | varchar |
| is_default     | boolean |

---

# orders

Stores customer orders.

| Column          | Type           |
| --------------- | -------------- |
| id              | bigint         |
| user_id         | bigint         |
| address_id      | bigint         |
| order_number    | varchar unique |
| status          | varchar        |
| subtotal        | decimal        |
| shipping_amount | decimal        |
| total_amount    | decimal        |
| payment_status  | varchar        |
| notes           | text nullable  |
| created_at      | timestamp      |
| updated_at      | timestamp      |

Status:

* Pending
* Confirmed
* Processing
* Packed
* Shipped
* Delivered
* Cancelled

---

# order_items

Stores purchased blends.

| Column      | Type    |
| ----------- | ------- |
| id          | bigint  |
| order_id    | bigint  |
| blend_id    | bigint  |
| quantity_kg | decimal |
| unit_price  | decimal |
| total_price | decimal |

---

# payments

Stores payment information.

| Column          | Type               |
| --------------- | ------------------ |
| id              | bigint             |
| order_id        | bigint             |
| payment_gateway | varchar            |
| transaction_id  | varchar            |
| amount          | decimal            |
| status          | varchar            |
| paid_at         | timestamp nullable |

---

# inventory_transactions

Tracks stock movement.

| Column     | Type      |
| ---------- | --------- |
| id         | bigint    |
| grain_id   | bigint    |
| type       | varchar   |
| quantity   | decimal   |
| notes      | text      |
| created_at | timestamp |

Types:

* Purchase
* Consumption
* Adjustment

---

# Relationships

User
→ hasMany Orders

User
→ hasMany Addresses

Blend
→ hasMany BlendItems

Order
→ hasMany OrderItems

Order
→ hasOne Payment

Grain
→ hasMany BlendItems

Grain
→ hasMany InventoryTransactions
