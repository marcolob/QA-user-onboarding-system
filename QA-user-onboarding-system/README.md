# QA User Onboarding System - DEMO 
Comprehensive QA testing project covering API validation using Postman, mock server simulation, and manual UI/UX test cases.

## 📌 Project Overview
This project simulates a **User Onboarding System** similar to what is used in banking, fintech, compliance, and KYC-driven platforms.  
It includes:

- 🚀 **Complete Postman API Collection** (40+ requests)
- 🧪 **Full test coverage for CRUD, Users, Documents, and KYC**
- 🧰 **Environment variables for dynamic testing**
- 🧷 **Mock API rules using Beeceptor**
- 📄 **40 detailed manual test cases (CSV)**
- 📚 **Portfolio-ready documentation**

This project showcases end-to-end QA skills across **API testing, mock server design, functional testing, error handling, and QA documentation**.

---

## 🗂 Project Structure

qa-user-onboarding-system/
│
├── postman/
│ ├── QA-User-Onboarding-System.postman_collection.json
│ └── qa-user-onboarding-env.postman_environment.json
│
├── test-cases/
│ └── onboarding_testcases.csv
│
└── README.md


---

## 🧪 API Features Covered

### 1️⃣ CRUD Basic (Users)
- Create user  
- Get user by ID  
- Update user  
- Delete user  

### 2️⃣ Users (Extended 10 cases)
- Validation errors  
- Duplicate emails  
- Missing fields  
- Listing users  
- Negative scenarios  

### 3️⃣ Documents (10 cases)
- Upload PDFs / images  
- Missing user_id  
- File update  
- Error handling  
- Document listing  

### 4️⃣ KYC (10 cases)
- Start KYC  
- Missing/invalid data  
- Status updates (pending → approved/rejected)  
- Filtering  
- KYC retrieval  

---

## 🧰 Mock Server Setup (Beeceptor)

Base URL:


https://marcolob.free.beeceptor.com/permisso


For each endpoint (`/users`, `/documents`, `/kyc`) custom mock rules were created to simulate:

- 201 Created (success)
- 400 Bad Request  
- 404 Not Found  
- 200 OK  
- Dynamic responses using variables (e.g., {{user_id}})

This allows reliable and consistent testing without depending on real backends.

---

## 🧪 Postman Testing

The collection includes:

- Pre-request scripts for dynamic IDs  
- Automated tests validating:
  - Status codes  
  - JSON schema  
  - Error responses  
  - Required fields  

### Example Test Assertions

```javascript
pm.test("Status code is 201", function () {
    pm.response.to.have.status(201);
});

pm.test("User has ID", function () {
    const json = pm.response.json();
    pm.expect(json.id).to.exist;
});

📄 Manual Test Cases (CSV)

File: /test-cases/onboarding_testcases.csv

Includes 40 detailed test cases, each with:

Test Case ID

Summary

Preconditions

Step-by-step procedure

Expected results

Priority

TestRail/Jira reference placeholders

Type (Functional / Non-functional / Negative)

Perfect for:

TestRail import

Interview review

Portfolio demonstration

🎯 Key QA Skills Demonstrated
✔ API Testing

CRUD + advanced validation, error handling, parameter checks, mock-based testing.

✔ Documentation

Clear, structured, reusable QA documentation.

✔ Manual Functional Testing

40 real-world test cases covering complex onboarding workflows.

✔ Negative & Edge Case Testing

Invalid IDs, missing fields, incomplete KYC, nonexistent documents.

✔ Mock Server Usage

Professional simulation of backend behavior.

✔ Test Design

Systematic approach aligned with industry best practices.

📚 How to Use
Import collection & environment in Postman:

Open Postman

Click Import

Select files from /postman

Set the environment

Run tests manually or via Collection Runner

👤 Author

Marco Lo Bianco
QA Engineer – API, Web & Functional Testing

GitHub: https://github.com/marcolob

Portfolio: https://marcolob.github.io/QA-Portfolio-Hub

LinkedIn: https://linkedin.com/in/marco-lo-bianco-869311b1

⭐ Feedback or Contributions

If you want to expand this project (e.g., adding Newman tests, CI integration, or automated collections), feel free to open an issue or contact me.
