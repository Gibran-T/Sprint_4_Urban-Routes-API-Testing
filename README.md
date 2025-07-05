# 🔌 Urban Routes – Sprint 4: API Testing

---

This repository documents the full suite of **manual API tests** executed during **Sprint 4** of the TripleTen QA Bootcamp. The goal was to validate all key backend functionalities of the **Urban Routes** delivery platform through well-structured requests and edge-case scenarios.

---

## 🧭 Project Overview

- 🎯 Test RESTful API endpoints across multiple services
- 🛠️ Validate request/response structure, authentication, data types, and limits
- ❌ Identify inconsistencies and unexpected status codes
- 📋 Log results and bugs for each test case

---

## 🗂️ Endpoints Tested

| Requirement | Description |
|-------------|-------------|
| `/api/v1/kits/:id/products` | Add products to a kit |
| `/api/v1/kits` | Create, edit, delete kits |
| `/api/v1/orders` | Create, read, cancel orders |
| `/order-and-go/v1/delivery` | Delivery price and availability |
| `/everything-you-need/v1/calculate` | Inventory check (JSON, XML, SOAP) |
| `/api/v1/couriers` | Shipping cost and area validation |
| `/api/v1/warehouses` | Inventory update and warehouse data |
| `/api/v1/users` | User creation and validation logic |

---

## 📄 Test Coverage

### ✅ Categories of Test Cases

- **Positive Cases:** Successful requests with valid input
- **Negative Cases:** Invalid payloads, unauthorized access, wrong formats
- **Boundary Cases:** Input limits (min/max characters, values, delivery times)
- **Special Formats:** XML & SOAP requests for inventory and product services

---

## 📊 Example Test Case

---

## 📌 Example Test Case

**Endpoint:** `POST /api/v1/kits/2/products`  
**Headers:**  
```http
Authorization: Bearer <token>  
Content-Type: application/json
{
  "productsList": [
    { "id": 1, "quantity": 2 },
    { "id": 2, "quantity": 3 }
  ]
}
Expected: 200 OK
Actual: 200 OK ✅
Status: Passed
---

| Bug ID | Summary                                    |
| ------ | ------------------------------------------ |
| TQS-3  | System allows adding non-existent product  |
| TQS-5  | Empty JSON body not handled                |
| TQS-7  | Missing auth still returns `200`           |
| TQS-14 | Order created without authentication       |
| TQS-22 | Email already used still allows creation   |
| TQS-23 | Weak passwords are accepted                |
| ...    | *See full bug list in the test plan below* |

---

📎 Documentation
✅ Test Plan Spreadsheet:
📄 Google Sheets – [Urban Lunch API Regression]
(https://docs.google.com/spreadsheets/d/1qw_6VOU1WC-owDRoMNuxDC4HkEF3K_xs/edit?usp=sharing)

🐞 Bug Reports in Jira:
🔗 Jira – gibranlog.atlassian.net
---

## 📌 Highlights of the Sprint

🧪 Over **40** detailed test cases across **6** major endpoints  
🔐 Covered **authorization**, **input types**, and **response structure**  
🛠️ Detected and reported **critical backend logic bugs**  
📉 Applied **boundary testing**, **invalid payloads**, and **format-specific requests**

---

👨‍💻 Author
Thiago Gibran Timoteo Nunes
📍 QA Engineer | REST API Testing | Exploratory & Functional QA
🌐 GitHub Portfolio

🧠 This project is part of a real-world QA portfolio showcasing structured test design, API analysis, and issue documentation. Developed during the TripleTen QA Bootcamp.

