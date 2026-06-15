# System Architecture

## Overview

The system follows a headless architecture.

Frontend and backend are developed independently and communicate through APIs.

## Components

### Frontend

Technology:

* Nuxt 4
* Vue 3
* Tailwind CSS
* Pinia

Responsibilities:

* UI Rendering
* Blend Builder
* Cart
* Checkout

---

### Backend

Technology:

* Laravel 12

Responsibilities:

* Business Logic
* Order Processing
* Pricing Calculation
* Nutrition Calculation
* Authentication

---

### Database

Technology:

* PostgreSQL

Responsibilities:

* User Data
* Orders
* Blend Configurations
* Inventory

---

### Authentication

Technology:

* Laravel Sanctum

Capabilities:

* Registration
* Login
* Session Management

---

### Payments

Technology:

* Razorpay

Capabilities:

* UPI
* Credit Cards
* Debit Cards
* Net Banking

---

## Request Flow

Customer

↓

Frontend (Nuxt)

↓

Laravel API

↓

PostgreSQL

↓

Response

↓

Frontend

---

## Future Integrations

* Subscription Engine
* AI Recommendation Engine
* Mobile Application
* ERP Integration
* Shipping Aggregator
