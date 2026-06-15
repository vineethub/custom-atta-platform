# API Design

Base URL

/api/v1

---

# Authentication

## Register

POST /auth/register

Request:

{
"name": "Vineet",
"email": "[vineet@example.com](mailto:vineet@example.com)",
"password": "password"
}

Response:

{
"user": {},
"token": ""
}

---

## Login

POST /auth/login

---

## Logout

POST /auth/logout

---

# Grains

## List Grains

GET /grains

Response:

[
{
"id": 1,
"name": "Wheat",
"protein_per_100g": 12
}
]

---

# Blend Builder

## Calculate Blend

POST /blends/calculate

Request:

{
"grains": [
{
"grain_id": 1,
"percentage": 40
},
{
"grain_id": 2,
"percentage": 20
}
]
}

Response:

{
"protein": 14.5,
"fiber": 7.2,
"calories": 356,
"price_per_kg": 78
}

---

## Save Blend

POST /blends

---

## Get Blend

GET /blends/{id}

---

# Cart

## Add To Cart

POST /cart/items

## Update Cart Item

PUT /cart/items/{id}

## Remove Cart Item

DELETE /cart/items/{id}

## View Cart

GET /cart

---

# Orders

## Create Order

POST /orders

## List Orders

GET /orders

## Order Details

GET /orders/{id}

---

# Addresses

## List Addresses

GET /addresses

## Create Address

POST /addresses

## Update Address

PUT /addresses/{id}

---

# Payments

## Create Payment

POST /payments/create

## Verify Payment

POST /payments/verify

---

# Admin APIs

/admin/grains

/admin/orders

/admin/payments

/admin/inventory

/admin/customers
