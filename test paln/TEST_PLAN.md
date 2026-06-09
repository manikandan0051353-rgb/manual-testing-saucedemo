# 📋 Test Plan — SauceDemo

**Document ID:** TP-SD-001  
**Version:** 1.0  
**Author:** Manikandan  
**Date:** 2026-06-09  
**Status:** Approved

---

## 1. Introduction

### 1.1 Purpose
This test plan defines the strategy, scope, resources, and schedule for manual testing of SauceDemo — a practice e-commerce web application used to simulate real-world QA scenarios.

### 1.2 Application Overview
SauceDemo is a single-page web application that simulates an online store selling products. It includes login, product browsing, cart management, and checkout.

---

## 2. Objectives

- Validate core user flows work end-to-end
- Identify functional defects in login, cart, and checkout
- Verify UI consistency and error messaging
- Test boundary conditions and negative paths

---

## 3. Scope

### In Scope
| Module | Description |
|---|---|
| Authentication | Login with valid/invalid credentials, locked user |
| Product Listing | Display, sorting (A-Z, Z-A, price low-high, price high-low) |
| Product Detail | Name, price, image, description, Add to Cart |
| Shopping Cart | Add/remove items, item count badge |
| Checkout | Form validation, order summary, order completion |
| Navigation | Hamburger menu, back buttons, logout |

### Out of Scope
- Performance / Load testing
- API / Backend testing
- Mobile native app testing
- Accessibility (WCAG) audit
- Security penetration testing

---

## 4. Test Strategy

**Approach:** Black-box manual testing  
**Techniques:** Equivalence partitioning, boundary value analysis, exploratory testing, error guessing

### Test Levels
| Level | Applied |
|---|---|
| Smoke Testing | ✅ Login + product listing |
| Functional Testing | ✅ All in-scope modules |
| Regression Testing | ✅ After defect fix |
| Negative Testing | ✅ Invalid inputs, locked users |

---

## 5. Entry & Exit Criteria

### Entry Criteria
- AUT is accessible at https://www.saucedemo.com
- Test credentials are valid and functional
- Test environment (browser/OS) is set up
- Test cases are reviewed and signed off

### Exit Criteria
- All 25 test cases executed
- 100% critical/high defects resolved or deferred
- Test summary report completed

---

## 6. Test Environment

| Parameter | Value |
|---|---|
| Browser | Google Chrome (latest stable) |
| OS | Windows 11 |
| Screen Resolution | 1920×1080 |
| Internet | Stable broadband |
| Tools | Chrome DevTools (for inspection) |

---

## 7. Test Data

| User | Password | Expected Behavior |
|---|---|---|
| `standard_user` | `secret_sauce` | Full access |
| `locked_out_user` | `secret_sauce` | Locked error message |
| `problem_user` | `secret_sauce` | Broken images/functions |
| `performance_glitch_user` | `secret_sauce` | Slow page loads |
| `invalid_user` | `wrong_pass` | Error message displayed |
| *(empty)* | *(empty)* | Required field errors |

---

## 8. Risk Assessment

| Risk | Likelihood | Impact | Mitigation |
|---|---|---|---|
| AUT unavailable | Low | High | Re-schedule; use screenshots for evidence |
| Test data reset between sessions | Medium | Medium | Re-run setup steps before execution |
| UI changes between test rounds | Low | Medium | Re-verify before regression |
| Browser caching issues | Medium | Low | Clear cache before each session |

---

## 9. Roles & Responsibilities

| Role | Name | Responsibility |
|---|---|---|
| QA Engineer | Manikandan | Test design, execution, bug reporting |
| Test Lead | Manikandan | Test plan approval, sign-off |

---

## 10. Schedule

| Activity | Duration |
|---|---|
| Test Planning | Day 1 |
| Test Case Design | Day 2 |
| Test Execution | Day 3–4 |
| Bug Reporting & Retesting | Day 5 |
| Test Summary Report | Day 6 |

---

## 11. Deliverables

- [x] Test Plan (this document)
- [x] Test Scenarios (`TEST_SCENARIOS.md`)
- [x] Test Cases (`TEST_CASES.md`)
- [x] Bug Reports (`BUG_REPORTS.md`)
- [ ] Test Execution Report *(post-execution)*
- [ ] Test Summary Report *(post-execution)*

---

## 12. Approvals

| Name | Role | Signature | Date |
|---|---|---|---|
| Manikandan | QA Engineer | ✅ | 2026-06-09 |
