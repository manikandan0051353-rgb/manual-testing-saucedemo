# 🗂 Test Scenarios — SauceDemo

**Document ID:** TS-SD-001  
**Version:** 1.0  
**Author:** Manikandan  
**Date:** 2026-06-09

---

## Module 1: Authentication

| ID | Scenario | Priority |
|---|---|---|
| TS-001 | Verify that a registered user can log in with valid credentials | 🔴 Critical |
| TS-002 | Verify that login is blocked for a locked-out user with appropriate error message | 🔴 Critical |
| TS-003 | Verify that login fails gracefully with invalid/empty credentials | 🔴 Critical |

---

## Module 2: Product Listing

| ID | Scenario | Priority |
|---|---|---|
| TS-004 | Verify all products are displayed correctly on the inventory page after login | 🟠 High |
| TS-005 | Verify that products can be sorted by all four available sort options | 🟠 High |
| TS-006 | Verify that each product card displays name, price, image, and Add to Cart button | 🟡 Medium |

---

## Module 3: Product Detail Page

| ID | Scenario | Priority |
|---|---|---|
| TS-007 | Verify navigating to a product detail page shows correct product information | 🟡 Medium |
| TS-008 | Verify that a product can be added to cart from the detail page | 🟠 High |
| TS-009 | Verify the Back to Products button returns user to the inventory list | 🟡 Medium |

---

## Module 4: Shopping Cart

| ID | Scenario | Priority |
|---|---|---|
| TS-010 | Verify that adding a product updates the cart badge count correctly | 🔴 Critical |
| TS-011 | Verify that removing a product from the cart updates the cart badge and list | 🔴 Critical |
| TS-012 | Verify the cart persists added items when navigating between pages | 🟠 High |

---

## Module 5: Checkout Flow

| ID | Scenario | Priority |
|---|---|---|
| TS-013 | Verify checkout form validates required fields (First Name, Last Name, Zip Code) | 🔴 Critical |
| TS-014 | Verify the order summary page displays correct items, prices, and totals | 🔴 Critical |
| TS-015 | Verify a user can complete an order and sees the order confirmation screen | 🔴 Critical |

---

## Coverage Matrix

| Module | # Scenarios | Critical | High | Medium |
|---|---|---|---|---|
| Authentication | 3 | 3 | 0 | 0 |
| Product Listing | 3 | 0 | 2 | 1 |
| Product Detail | 3 | 0 | 1 | 2 |
| Shopping Cart | 3 | 2 | 1 | 0 |
| Checkout | 3 | 3 | 0 | 0 |
| **Total** | **15** | **8** | **4** | **3** |
