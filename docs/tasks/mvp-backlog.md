# MVP Backlog

## Overview

This backlog contains all tasks required to launch the MVP of the Personalized Atta Platform.

Priority Levels:

* P0 = Must Have
* P1 = Should Have
* P2 = Nice To Have

---

# Epic 1: Project Setup

Priority: P0

## Backend Setup

* [ ] Create Laravel project
* [ ] Configure PostgreSQL
* [ ] Configure environment variables
* [ ] Setup Laravel Sanctum
* [ ] Setup API versioning (/api/v1)
* [ ] Setup queue configuration
* [ ] Setup mail configuration

## Frontend Setup

* [ ] Create Nuxt project
* [ ] Setup TailwindCSS
* [ ] Setup Pinia
* [ ] Setup API client
* [ ] Setup authentication store

## DevOps

* [ ] Create GitHub repository
* [ ] Configure branch protection
* [ ] Setup CI pipeline
* [ ] Setup deployment environments

Definition of Done:

* Frontend and backend running locally.

---

# Epic 2: Authentication

Priority: P0

## Backend

* [ ] Register API
* [ ] Login API
* [ ] Logout API
* [ ] Current User API

## Frontend

* [ ] Register page
* [ ] Login page
* [ ] Logout functionality
* [ ] Protected routes

Definition of Done:

* User can create account and login.

---

# Epic 3: Grain Management

Priority: P0

## Database

* [ ] Create grains migration
* [ ] Create Grain model
* [ ] Create GrainSeeder

## Admin

* [ ] Grain listing
* [ ] Create grain
* [ ] Update grain
* [ ] Delete grain
* [ ] Enable/disable grain

## API

* [ ] List grains endpoint

Definition of Done:

* Admin can manage grains.

---

# Epic 4: Blend Builder Engine

Priority: P0

## Backend

* [ ] Blend calculation service
* [ ] Nutrition calculation service
* [ ] Pricing calculation service
* [ ] Validation service

## API

* [ ] Calculate blend endpoint

## Frontend

* [ ] Grain selector
* [ ] Percentage editor
* [ ] Validation messages
* [ ] Nutrition display
* [ ] Price display

Validation Rules:

* Total percentage = 100%
* No duplicate grains
* Minimum 1 grain selected

Definition of Done:

* Customer can create valid blend.

---

# Epic 5: Cart

Priority: P0

## Backend

* [ ] Cart APIs
* [ ] Add item
* [ ] Update item
* [ ] Remove item

## Frontend

* [ ] Cart page
* [ ] Quantity selector
* [ ] Cart summary

Definition of Done:

* Customer can manage cart.

---

# Epic 6: Address Management

Priority: P0

## Backend

* [ ] Address migration
* [ ] Address model
* [ ] Address APIs

## Frontend

* [ ] Address listing
* [ ] Add address
* [ ] Edit address
* [ ] Delete address

Definition of Done:

* Customer can manage addresses.

---

# Epic 7: Orders

Priority: P0

## Database

* [ ] Orders migration
* [ ] Order items migration

## Backend

* [ ] Create order
* [ ] Order details
* [ ] Order listing

## Frontend

* [ ] Order success page
* [ ] Order history page
* [ ] Order detail page

Definition of Done:

* Customer can place orders.

---

# Epic 8: Payments

Priority: P0

## Backend

* [ ] Razorpay integration
* [ ] Create payment order
* [ ] Verify payment
* [ ] Store transaction

## Frontend

* [ ] Payment page
* [ ] Payment success page
* [ ] Payment failure page

Definition of Done:

* Customer can pay successfully.

---

# Epic 9: Admin Order Management

Priority: P0

## Admin

* [ ] Orders listing
* [ ] Order details
* [ ] Update order status

Statuses:

* Pending
* Confirmed
* Processing
* Packed
* Shipped
* Delivered
* Cancelled

Definition of Done:

* Admin can process orders.

---

# Epic 10: Inventory

Priority: P1

## Backend

* [ ] Inventory transactions
* [ ] Stock adjustments
* [ ] Stock consumption

## Admin

* [ ] Inventory dashboard
* [ ] Low stock alerts

Definition of Done:

* Stock tracking operational.

---

# Epic 11: Homepage

Priority: P0

## Sections

* [ ] Hero section
* [ ] Benefits section
* [ ] Featured grains
* [ ] Featured blends
* [ ] How it works
* [ ] Testimonials
* [ ] CTA section

Definition of Done:

* Public landing page complete.

---

# Epic 12: Customer Account

Priority: P1

## Frontend

* [ ] Account dashboard
* [ ] Order history
* [ ] Profile settings

Definition of Done:

* Customer can manage account.

---

# Epic 13: Saved Blends

Priority: P2

* [ ] Save blend
* [ ] Rename blend
* [ ] Delete blend
* [ ] Reuse blend

Definition of Done:

* Customer can store favorite blends.

---

# MVP Release Checklist

## Functional

* [ ] Authentication
* [ ] Grain Management
* [ ] Blend Builder
* [ ] Cart
* [ ] Checkout
* [ ] Payments
* [ ] Orders

## Technical

* [ ] Error handling
* [ ] Validation
* [ ] Logging
* [ ] Security review

## Launch

* [ ] Production deployment
* [ ] Domain setup
* [ ] SSL configuration
* [ ] Backup strategy

Success Criteria:

* First successful customer order completed end-to-end.
