# ✅ Test Cases — SauceDemo

**Document ID:** TC-SD-001  
**Version:** 1.0  
**Author:** Manikandan  
**Date:** 2026-06-09

---

## Module 1: Authentication

---

### TC-001 — Successful Login with Valid Credentials
**Scenario Ref:** TS-001 | **Priority:** 🔴 Critical | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | Browser open, navigate to https://www.saucedemo.com |
| **Test Data** | Username: `standard_user` / Password: `secret_sauce` |

**Steps:**
1. Enter `standard_user` in the Username field
2. Enter `secret_sauce` in the Password field
3. Click the **Login** button

**Expected Result:** User is redirected to `/inventory.html`; page title shows "Swag Labs"; products are visible.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-002 — Login with Locked Out User
**Scenario Ref:** TS-002 | **Priority:** 🔴 Critical | **Type:** Negative

| Field | Details |
|---|---|
| **Pre-condition** | Navigate to login page |
| **Test Data** | Username: `locked_out_user` / Password: `secret_sauce` |

**Steps:**
1. Enter `locked_out_user` in Username
2. Enter `secret_sauce` in Password
3. Click **Login**

**Expected Result:** Error message displayed: *"Epic sadface: Sorry, this user has been locked out."* No redirect occurs.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-003 — Login with Invalid Password
**Scenario Ref:** TS-003 | **Priority:** 🔴 Critical | **Type:** Negative

| Field | Details |
|---|---|
| **Pre-condition** | Navigate to login page |
| **Test Data** | Username: `standard_user` / Password: `wrongpass` |

**Steps:**
1. Enter `standard_user` in Username
2. Enter `wrongpass` in Password
3. Click **Login**

**Expected Result:** Error message: *"Epic sadface: Username and password do not match any user in this service."*  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-004 — Login with Empty Username and Password
**Scenario Ref:** TS-003 | **Priority:** 🔴 Critical | **Type:** Negative

| Field | Details |
|---|---|
| **Pre-condition** | Navigate to login page |
| **Test Data** | Username: *(empty)* / Password: *(empty)* |

**Steps:**
1. Leave both fields empty
2. Click **Login**

**Expected Result:** Error message: *"Epic sadface: Username is required."*  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-005 — Login with Empty Password Only
**Scenario Ref:** TS-003 | **Priority:** 🟠 High | **Type:** Negative

| Field | Details |
|---|---|
| **Pre-condition** | Navigate to login page |
| **Test Data** | Username: `standard_user` / Password: *(empty)* |

**Steps:**
1. Enter `standard_user` in Username
2. Leave Password empty
3. Click **Login**

**Expected Result:** Error message: *"Epic sadface: Password is required."*  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

## Module 2: Product Listing

---

### TC-006 — Verify Product Count on Inventory Page
**Scenario Ref:** TS-004 | **Priority:** 🟠 High | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | Logged in as `standard_user` |
| **Test Data** | N/A |

**Steps:**
1. After login, observe the inventory page
2. Count the number of product cards displayed

**Expected Result:** Exactly **6 products** are displayed on the page.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-007 — Sort Products by Name A–Z
**Scenario Ref:** TS-005 | **Priority:** 🟠 High | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | Logged in, on inventory page |
| **Test Data** | Sort option: "Name (A to Z)" |

**Steps:**
1. Click the sort dropdown (top-right)
2. Select **"Name (A to Z)"**
3. Observe product order

**Expected Result:** Products are sorted alphabetically A→Z by product name.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-008 — Sort Products by Price Low to High
**Scenario Ref:** TS-005 | **Priority:** 🟠 High | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | Logged in, on inventory page |
| **Test Data** | Sort option: "Price (low to high)" |

**Steps:**
1. Click sort dropdown
2. Select **"Price (low to high)"**
3. Observe prices from top to bottom

**Expected Result:** Products displayed in ascending price order. First product has lowest price.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-009 — Sort Products by Price High to Low
**Scenario Ref:** TS-005 | **Priority:** 🟡 Medium | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | Logged in, on inventory page |
| **Test Data** | Sort option: "Price (high to low)" |

**Steps:**
1. Click sort dropdown
2. Select **"Price (high to low)"**
3. Observe prices

**Expected Result:** Products displayed in descending price order. First product has highest price.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-010 — Verify Product Card Elements
**Scenario Ref:** TS-006 | **Priority:** 🟡 Medium | **Type:** UI Validation

| Field | Details |
|---|---|
| **Pre-condition** | Logged in, on inventory page |
| **Test Data** | Any product card |

**Steps:**
1. Inspect any product card on inventory page
2. Check for: product image, product name, product description, price, and Add to Cart button

**Expected Result:** All 5 elements are present and visible on every product card.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

## Module 3: Product Detail Page

---

### TC-011 — Navigate to Product Detail Page
**Scenario Ref:** TS-007 | **Priority:** 🟡 Medium | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | Logged in, on inventory page |
| **Test Data** | Click on "Sauce Labs Backpack" |

**Steps:**
1. Click on product name **"Sauce Labs Backpack"**
2. Observe detail page

**Expected Result:** Detail page loads with correct name, description, price ($29.99), image, and Add to Cart button.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-012 — Add Product to Cart from Detail Page
**Scenario Ref:** TS-008 | **Priority:** 🟠 High | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | On product detail page for any product |
| **Test Data** | "Sauce Labs Backpack" |

**Steps:**
1. Navigate to detail page of "Sauce Labs Backpack"
2. Click **Add to Cart**
3. Observe cart icon badge

**Expected Result:** Cart badge shows **1**; button changes to **"Remove"**.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-013 — Back to Products Navigation
**Scenario Ref:** TS-009 | **Priority:** 🟡 Medium | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | On any product detail page |
| **Test Data** | N/A |

**Steps:**
1. Click **← Back to products** link

**Expected Result:** User is returned to `/inventory.html`; all products visible; scroll position reasonable.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

## Module 4: Shopping Cart

---

### TC-014 — Add Single Item to Cart
**Scenario Ref:** TS-010 | **Priority:** 🔴 Critical | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | Logged in, on inventory page, cart empty |
| **Test Data** | "Sauce Labs Bike Light" |

**Steps:**
1. Click **Add to Cart** on "Sauce Labs Bike Light"
2. Observe cart icon in header

**Expected Result:** Cart badge appears with count **1**.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-015 — Add Multiple Items to Cart
**Scenario Ref:** TS-010 | **Priority:** 🔴 Critical | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | Logged in, on inventory page, cart empty |
| **Test Data** | Any 3 products |

**Steps:**
1. Click **Add to Cart** on 3 different products
2. Observe cart badge after each

**Expected Result:** Cart badge increments correctly: 1 → 2 → 3 after each addition.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-016 — Remove Item from Cart (Inventory Page)
**Scenario Ref:** TS-011 | **Priority:** 🔴 Critical | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | 1 item already in cart |
| **Test Data** | N/A |

**Steps:**
1. Click **Remove** on the item that was added
2. Observe cart badge

**Expected Result:** Cart badge disappears (count = 0); button reverts to **"Add to Cart"**.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-017 — Remove Item from Cart Page
**Scenario Ref:** TS-011 | **Priority:** 🔴 Critical | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | At least 2 items in cart; on cart page |
| **Test Data** | N/A |

**Steps:**
1. Navigate to cart (click cart icon)
2. Click **Remove** on one item
3. Observe cart list and badge

**Expected Result:** Removed item no longer appears in cart list; badge count decrements by 1.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-018 — Cart Persistence Across Navigation
**Scenario Ref:** TS-012 | **Priority:** 🟠 High | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | 2 items added to cart |
| **Test Data** | N/A |

**Steps:**
1. Add 2 items from inventory page
2. Navigate to a product detail page
3. Navigate back to inventory
4. Check cart badge

**Expected Result:** Cart badge still shows **2**; items preserved.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

## Module 5: Checkout Flow

---

### TC-019 — Proceed to Checkout
**Scenario Ref:** TS-013 | **Priority:** 🔴 Critical | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | At least 1 item in cart; on cart page |
| **Test Data** | N/A |

**Steps:**
1. Click **Checkout** button from cart page

**Expected Result:** User is redirected to `/checkout-step-one.html`; form with First Name, Last Name, Zip Code is shown.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-020 — Checkout with Missing First Name
**Scenario Ref:** TS-013 | **Priority:** 🔴 Critical | **Type:** Negative

| Field | Details |
|---|---|
| **Pre-condition** | On checkout step one page |
| **Test Data** | First Name: *(empty)*, Last Name: "Doe", Zip: "12345" |

**Steps:**
1. Leave First Name blank
2. Fill Last Name and Zip
3. Click **Continue**

**Expected Result:** Error: *"Error: First Name is required"*; user stays on step one.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-021 — Checkout with Missing Zip Code
**Scenario Ref:** TS-013 | **Priority:** 🟠 High | **Type:** Negative

| Field | Details |
|---|---|
| **Pre-condition** | On checkout step one |
| **Test Data** | First Name: "John", Last Name: "Doe", Zip: *(empty)* |

**Steps:**
1. Fill First and Last Name, leave Zip blank
2. Click **Continue**

**Expected Result:** Error: *"Error: Postal Code is required"*; user stays on step one.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-022 — Successful Checkout Form Submission
**Scenario Ref:** TS-013 | **Priority:** 🔴 Critical | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | 1+ items in cart, on checkout step one |
| **Test Data** | First Name: "John", Last Name: "Doe", Zip: "12345" |

**Steps:**
1. Fill all fields with valid data
2. Click **Continue**

**Expected Result:** User is redirected to checkout step two (`/checkout-step-two.html`).  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-023 — Verify Order Summary on Checkout Step Two
**Scenario Ref:** TS-014 | **Priority:** 🔴 Critical | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | On checkout step two; 1 product added prior |
| **Test Data** | "Sauce Labs Backpack" ($29.99) |

**Steps:**
1. Observe items listed in order summary
2. Check Item Total, Tax, and Total price

**Expected Result:** Item total matches product prices; tax is calculated correctly; Total = Item Total + Tax.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-024 — Complete Order Successfully
**Scenario Ref:** TS-015 | **Priority:** 🔴 Critical | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | On checkout step two |
| **Test Data** | N/A |

**Steps:**
1. Click **Finish** button

**Expected Result:** Confirmation page shown with message *"Thank you for your order!"*; cart badge disappears; URL is `/checkout-complete.html`.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

### TC-025 — Logout via Hamburger Menu
**Scenario Ref:** Navigation | **Priority:** 🟠 High | **Type:** Positive

| Field | Details |
|---|---|
| **Pre-condition** | Logged in as `standard_user` |
| **Test Data** | N/A |

**Steps:**
1. Click ☰ hamburger menu (top-left)
2. Click **Logout**

**Expected Result:** User is redirected back to login page (`/`); session is ended; pressing Back does not re-enter the app.  
**Actual Result:** *(fill on execution)*  
**Status:** ⬜ Not Run

---

## Execution Summary

| Module | Total TCs | ✅ Pass | ❌ Fail | ⬜ Not Run |
|---|---|---|---|---|
| Authentication | 5 | — | — | 5 |
| Product Listing | 5 | — | — | 5 |
| Product Detail | 3 | — | — | 3 |
| Shopping Cart | 5 | — | — | 5 |
| Checkout | 6 | — | — | 6 |
| Navigation | 1 | — | — | 1 |
| **Total** | **25** | **—** | **—** | **25** |
