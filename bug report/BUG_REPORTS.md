# 🐛 Bug Reports — SauceDemo

**Document ID:** BR-SD-001  
**Version:** 1.0  
**Author:** Manikandan  
**Date:** 2026-06-09

---

## Bug Report Template Reference

| Field | Description |
|---|---|
| **Bug ID** | Unique identifier |
| **Title** | Short descriptive title |
| **Module** | Affected feature area |
| **Severity** | Critical / High / Medium / Low |
| **Priority** | P1 / P2 / P3 / P4 |
| **Status** | New / Open / Fixed / Closed / Deferred |
| **Environment** | OS, Browser, version |
| **Reported By** | Tester name |
| **Steps to Reproduce** | Numbered steps |
| **Expected Result** | What should happen |
| **Actual Result** | What actually happens |
| **Attachments** | Screenshots / logs |

---

## BUG-001 — Problem User: Product Images Are Broken

| Field | Value |
|---|---|
| **Bug ID** | BUG-SD-001 |
| **Title** | All product images fail to load for `problem_user` |
| **Module** | Product Listing |
| **Severity** | 🟠 High |
| **Priority** | P2 |
| **Status** | 🔵 Open |
| **Environment** | Windows 11 / Chrome 124 |
| **Reported By** | Manikandan |
| **Linked TC** | TC-010 |

**Steps to Reproduce:**
1. Navigate to https://www.saucedemo.com
2. Login with username: `problem_user`, password: `secret_sauce`
3. Observe the inventory/products page

**Expected Result:**  
All product images load correctly and display the appropriate product photo.

**Actual Result:**  
All product images are broken (display as a dog/wrong image). No product-specific images are rendered.

**Root Cause Hypothesis:**  
Image source URLs are hardcoded to a wrong path for `problem_user` session.

**Impact:**  
Users cannot visually identify products — severe UX degradation; potential loss of sales.

**Attachments:** `bug-001-broken-images.png` *(screenshot placeholder)*

---

## BUG-002 — Locked Out User Receives Generic Error Instead of Specific Message

| Field | Value |
|---|---|
| **Bug ID** | BUG-SD-002 |
| **Title** | Error message for locked_out_user is not user-friendly |
| **Module** | Authentication |
| **Severity** | 🟡 Medium |
| **Priority** | P3 |
| **Status** | 🔵 Open |
| **Environment** | Windows 11 / Chrome 124 |
| **Reported By** | Manikandan |
| **Linked TC** | TC-002 |

**Steps to Reproduce:**
1. Navigate to login page
2. Enter username: `locked_out_user`, password: `secret_sauce`
3. Click **Login**
4. Read the displayed error message

**Expected Result:**  
Error message should clearly state the account is locked and direct the user to contact support. E.g., *"Your account has been locked. Please contact your administrator."*

**Actual Result:**  
Message displayed: *"Epic sadface: Sorry, this user has been locked out."*  
The phrase "Epic sadface" is informal and unprofessional for a production application.

**Impact:**  
Poor user experience; non-professional language may damage brand credibility in a real-world deployment.

**Attachments:** `bug-002-locked-user-error.png` *(screenshot placeholder)*

---

## BUG-003 — Checkout: "Continue Shopping" from Cart Does Not Preserve Scroll Position

| Field | Value |
|---|---|
| **Bug ID** | BUG-SD-003 |
| **Title** | Continue Shopping button always scrolls to top of inventory page |
| **Module** | Shopping Cart / Navigation |
| **Severity** | 🟢 Low |
| **Priority** | P4 |
| **Status** | 🔵 Open |
| **Environment** | Windows 11 / Chrome 124 |
| **Reported By** | Manikandan |
| **Linked TC** | TC-018 |

**Steps to Reproduce:**
1. Login as `standard_user`
2. Scroll down to the bottom product on inventory page
3. Add the bottom product to the cart
4. Click the cart icon → navigate to cart page
5. Click **Continue Shopping**

**Expected Result:**  
User is returned to inventory page with scroll position preserved at the last viewed product.

**Actual Result:**  
User is returned to the top of the inventory page, losing their scroll position. They must scroll again to find where they were.

**Impact:**  
Minor UX issue for users browsing large product lists; increases friction when adding multiple items.

**Attachments:** `bug-003-scroll-position.png` *(screenshot placeholder)*

---

## BUG-004 — Checkout Step One: Cancel Button Does Not Restore Cart State

| Field | Value |
|---|---|
| **Bug ID** | BUG-SD-004 |
| **Title** | Pressing Cancel on checkout step two loses cart contents on some navigations |
| **Module** | Checkout |
| **Severity** | 🔴 Critical |
| **Priority** | P1 |
| **Status** | 🔵 Open |
| **Environment** | Windows 11 / Chrome 124 |
| **Reported By** | Manikandan |
| **Linked TC** | TC-019 |

**Steps to Reproduce:**
1. Login as `standard_user`
2. Add 3 items to the cart
3. Proceed to checkout → Fill step one → Reach step two
4. Click **Cancel** on step two
5. Navigate to cart via the cart icon

**Expected Result:**  
All 3 items should remain in the cart after cancelling checkout.

**Actual Result:**  
Intermittently, 1–2 items may be missing from the cart after cancellation. Cart badge count does not match the actual cart contents on the cart page.

**Root Cause Hypothesis:**  
Cart state management issue; possible race condition or premature state reset on Cancel action.

**Impact:**  
**Critical** — Users may lose cart items without completing purchase. Risk of revenue loss in production scenario.

**Attachments:** `bug-004-cart-state-cancel.png` *(screenshot placeholder)*

---

## BUG-005 — Sort Dropdown Defaults to "Name (A to Z)" After Page Refresh

| Field | Value |
|---|---|
| **Bug ID** | BUG-SD-005 |
| **Title** | Selected sort order resets to default after page navigation or refresh |
| **Module** | Product Listing |
| **Severity** | 🟡 Medium |
| **Priority** | P3 |
| **Status** | 🔵 Open |
| **Environment** | Windows 11 / Chrome 124 |
| **Reported By** | Manikandan |
| **Linked TC** | TC-008 |

**Steps to Reproduce:**
1. Login as `standard_user`
2. On inventory page, change sort to **"Price (high to low)"**
3. Click on any product to view the detail page
4. Click **← Back to products**
5. Observe the sort dropdown value

**Expected Result:**  
Sort preference **"Price (high to low)"** should persist when returning to the inventory page.

**Actual Result:**  
Sort dropdown resets to **"Name (A to Z)"** (the default). Products are re-sorted in alphabetical order, ignoring the user's previous selection.

**Impact:**  
Medium — Users who sort by price must re-apply their sort on every page navigation, degrading browsing experience.

**Attachments:** `bug-005-sort-reset.png` *(screenshot placeholder)*

---

## Bug Summary Dashboard

| Bug ID | Title | Module | Severity | Priority | Status |
|---|---|---|---|---|---|
| BUG-SD-001 | Broken product images for problem_user | Product Listing | 🟠 High | P2 | 🔵 Open |
| BUG-SD-002 | Unprofessional locked-out error message | Authentication | 🟡 Medium | P3 | 🔵 Open |
| BUG-SD-003 | Continue Shopping loses scroll position | Cart/Navigation | 🟢 Low | P4 | 🔵 Open |
| BUG-SD-004 | Cancel checkout may drop cart items | Checkout | 🔴 Critical | P1 | 🔵 Open |
| BUG-SD-005 | Sort order resets on navigation | Product Listing | 🟡 Medium | P3 | 🔵 Open |

### By Severity
| Severity | Count |
|---|---|
| 🔴 Critical | 1 |
| 🟠 High | 1 |
| 🟡 Medium | 2 |
| 🟢 Low | 1 |
