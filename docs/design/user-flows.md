# User Flows

## Overview

This document defines the primary user journeys for the Personalized Atta Platform MVP.

---

# Flow 1: Guest User Creates and Orders a Custom Blend

Goal:
Allow a first-time visitor to create a custom atta blend and place an order.

## Flow

Homepage

↓

Click "Build Your Atta"

↓

Select Grains

↓

Assign Percentages

↓

System Validates Total = 100%

↓

System Calculates:

* Protein
* Fiber
* Calories
* Price per KG

↓

Select Quantity

(2kg / 5kg / 10kg)

↓

Add To Cart

↓

Proceed To Checkout

↓

Login/Register (if required)

↓

Add Delivery Address

↓

Select Payment Method

↓

Place Order

↓

Payment Success

↓

Order Confirmation Page

---

## Validation Rules

* At least one grain must be selected.
* Total percentage must equal 100%.
* Quantity must be greater than 0.
* Delivery address is mandatory.

---

# Flow 2: Customer Uses Recommended Blend

Goal:
Help users who do not know how to build a blend.

## Flow

Homepage

↓

Click "Find My Blend"

↓

Select Goal

Options:

* Weight Loss
* Muscle Gain
* Family Health
* Diabetes Friendly
* High Fiber

↓

System Generates Recommended Blend

↓

Display:

* Ingredients
* Nutrition
* Price

↓

Customer Can:

A. Accept Recommendation

OR

B. Customize Further

↓

Add To Cart

↓

Checkout

↓

Order Confirmation

Note:
This flow is optional and may be introduced after MVP.

---

# Flow 3: Customer Reorders Previous Blend

Goal:
Enable quick repeat purchases.

## Flow

Login

↓

My Account

↓

Order History

↓

Select Previous Order

↓

View Blend Details

↓

Click Reorder

↓

Select Quantity

↓

Add To Cart

↓

Checkout

↓

Order Placed

---

# Flow 4: Customer Saves Favorite Blend

Goal:
Allow customers to reuse custom blends.

## Flow

Create Blend

↓

View Blend Summary

↓

Click Save Blend

↓

Enter Blend Name

Example:

* Gym Blend
* Family Blend
* Diabetes Mix

↓

Blend Saved

↓

Available Under:

My Account → Saved Blends

---

# Flow 5: Admin Creates Grain

Goal:
Manage grain catalog.

## Flow

Admin Login

↓

Dashboard

↓

Grains

↓

Create Grain

↓

Enter:

* Name
* Description
* Price Per KG
* Protein
* Fiber
* Calories
* Stock Quantity

↓

Save

↓

Grain Available In Builder

---

# Flow 6: Admin Processes Order

Goal:
Track order fulfillment.

## Flow

Admin Dashboard

↓

Orders

↓

View New Order

↓

Verify Payment

↓

Change Status

Pending

↓

Confirmed

↓

Processing

↓

Packed

↓

Shipped

↓

Delivered

Customer receives status updates at each stage.

---

# Flow 7: Inventory Consumption

Goal:
Maintain grain stock accuracy.

## Flow

Order Confirmed

↓

System Reads Blend Composition

Example:

5kg Order

Wheat 40%

Ragi 20%

Oats 15%

Chana 15%

Soybean 10%

↓

Calculate Grain Usage

↓

Reduce Inventory

↓

Record Inventory Transaction

↓

Update Available Stock

---

# Flow 8: Guest Registration

Goal:
Allow customer account creation.

## Flow

Register

↓

Enter:

* Name
* Email
* Phone
* Password

↓

Verify Account

↓

Account Created

↓

Redirect To Dashboard

---

# MVP User Flows

Required For Launch:

✓ Flow 1 - Create Blend & Order

✓ Flow 5 - Grain Management

✓ Flow 6 - Order Processing

✓ Flow 8 - Registration

---

# Post-MVP User Flows

Future Releases:

* Recommended Blends
* Saved Blends
* Reorder Functionality
* Subscription Orders
* AI Nutrition Recommendations
