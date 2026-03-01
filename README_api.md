# 🔌 ReqRes REST API — Manual Testing Project

A complete API testing project built using **Postman** to manually test the [ReqRes REST API](https://reqres.in). This project covers two modules — Users and Authentication — testing all major HTTP methods with both positive and negative test cases.

---

## 📁 Project Structure

```
reqres-api-testing/
│
├── ReqRes_API_Testing.postman_collection.json   ← Import this into Postman to run all tests
├── ReqRes_API_Test_Cases.xlsx                   ← All test cases + bug report + summary
├── API_Test_Summary_Report.docx                 ← Formal test summary report
└── README.md                                    ← Project documentation
```

---

## 🛠 Tools Used

| Tool | Purpose |
|---|---|
| Postman v11 | Sending API requests and validating responses |
| ReqRes API | Free REST API used as the system under test |
| Microsoft Excel | Test case documentation |
| Microsoft Word | Test summary report |

---

## 🌐 API Details

| Item | Details |
|---|---|
| Base URL | `https://reqres.in/api` |
| API Type | REST API |
| Auth | API Key (`x-api-key` header) |
| Data Format | JSON |

---

## 🧪 What Was Tested

### Module 1: Users
| TC ID | Method | Endpoint | Type | Expected Status |
|---|---|---|---|---|
| TC_001 | GET | /users?page=1 | Positive | 200 |
| TC_002 | GET | /users/2 | Positive | 200 |
| TC_003 | GET | /users/99 | Negative | 404 |
| TC_004 | POST | /users | Positive | 201 |
| TC_005 | PUT | /users/2 | Positive | 200 |
| TC_006 | DELETE | /users/2 | Positive | 204 |

### Module 2: Authentication
| TC ID | Method | Endpoint | Type | Expected Status |
|---|---|---|---|---|
| TC_007 | POST | /register (valid) | Positive | 200 |
| TC_008 | POST | /register (missing password) | Negative | 400 |
| TC_009 | POST | /login (valid) | Positive | 200 |
| TC_010 | POST | /login (missing password) | Negative | 400 |
| TC_011 | POST | /login (wrong credentials) | Negative | 400 |

---

## 📊 Test Results Summary

| Metric | Result |
|---|---|
| Total Test Cases | 11 |
| Passed | 11 |
| Failed | 0 |
| Pass Rate | 100% |
| Bugs Found | 0 |

---

## 📚 HTTP Methods Tested

| Method | What it does |
|---|---|
| GET | Retrieve data |
| POST | Create new data |
| PUT | Update existing data |
| DELETE | Remove data |

## 📚 Status Codes Validated

| Code | Meaning | Where used |
|---|---|---|
| 200 | OK — Success | GET, Login, Register |
| 201 | Created | POST /users |
| 204 | No Content | DELETE /users |
| 400 | Bad Request | Missing fields, wrong credentials |
| 404 | Not Found | User ID that doesn't exist |

---

## 🚀 How to Run the Tests Yourself

1. Download and install [Postman](https://www.postman.com/downloads/)
2. Get a free API key from [https://reqres.in](https://reqres.in)
3. In Postman click **Import** and select `ReqRes_API_Testing.postman_collection.json`
4. Go to the collection settings → **Variables** tab
5. Add your API key as the value for `api_key`
6. Run each request and verify the status codes match the expected results

---

## 🔑 Key Learnings

- How to test REST APIs using Postman
- Understanding HTTP methods (GET, POST, PUT, DELETE)
- Validating HTTP status codes (200, 201, 204, 400, 404)
- API key authentication via request headers
- Writing positive and negative API test cases
- Documenting API test results professionally
