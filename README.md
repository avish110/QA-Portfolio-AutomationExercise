# QA-Portfolio-AutomationExercise
Manual and API test suites, bug tracking log, and test execution reports for Automation Exercise

# 🧪 QA Portfolio: Automation Exercise Project

Welcome to my Quality Assurance portfolio repository! This project demonstrates end-to-end manual and API testing performed on [Automation Exercise](https://automationexercise.com/), a comprehensive e-commerce dummy application designed for QA testing.

---

## 📊 Project Scope & Metrics

| Test Suite  | Total Cases  | Pass Count | Fail Count | Coverage Focus |
| :--- | :--- | :--- | :--- | :--- |
| **Manual UI Test Suite** | 33 | 29 | 4 | End-to-end user flows (Cart, Checkout, Payment, Search) |
| **API Test Suite** | 80 | 54 | 26 | REST endpoints, negative testing, boundary values, security |
| **Combined Defect Log** | 21 Tracked Bugs | — | — | Severity mapping, reproduction steps, and root-cause analysis |

---

## 📂 Repository Contents

1. **`automationexercise_manual_test_cases.xlsx`**
   * Contains manual functional test cases covering User Signup, Login, Product Catalog, Search, Cart calculations, Checkout steps, and Order/Invoice verification.
2. **`automationexercise_test_cases_api.xlsx`**
   * Contains structured test cases for 14 backend API endpoints (Products, Brands, Search, Login, Account creation/deletion, and user lookups).
   * Incorporates **Equivalence Partitioning**, **Boundary Value Analysis (BVA)**, and negative testing (omitting required fields, invalid formats, SQL/XSS injections).
3. **`combined_bug_report.xlsx`**
   * A professional Defect Log tracking **21 identified bugs** across the UI and API layers.
   * Categorized by Bug ID, Module, Type, Severity (Critical/High/Medium/Low), Priority, Steps to Reproduce, Expected vs. Actual results, and developer notes.

---

## 🔑 Key Technical Findings & Architecture Notes

* **REST API Status Code Mismatch:** The server transports almost all responses as `HTTP 200 OK` in the transport header, while placing actual error or success indicators (`201`, `400`, `404`, `405`) inside the JSON body `responseCode` property.
* **Content-Type Mismatch:** All API endpoints incorrectly return `Content-Type: text/html; charset=utf-8` instead of `application/json`.
* **Server-Side Validation Gaps:** The `createAccount` endpoint accepts requests missing critical required fields (like email and password) with a `201 Created` status due to missing backend input validation.

---

## 🛠️ Tools & Technologies Used
* **Manual Testing:** Exploratory testing, UI/UX validation, test case design techniques.
* **API Testing:** Postman, REST API validation, payload inspection, negative & security test design.
* **Documentation:** Microsoft Excel.

---
*Created by Avish*  
*Aspiring Software QA Engineer | Gandhinagar, India*
