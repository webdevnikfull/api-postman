# 🧪 QA Automation Portfolio: Book Store API Testing & Automation

> About this repository: This project demonstrates automated API testing using Postman and JavaScript test scripts (Chai assertions) for the DemoQA Book Store service. It covers end-to-end API scenarios including authentication token generation, negative testing with invalid credentials, and resource management (adding and deleting books). It also highlights a modern "Shift-Left" QA approach and Continuous Integration (CI/CD) readiness via Newman.

![Postman](https://img.shields.io/badge/Postman-FF6C37?style=for-the-badge&logo=postman&logoColor=white)
![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black)
![Newman](https://img.shields.io/badge/Newman-026E42?style=for-the-badge&logo=postman&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/GitHub_Actions-2088FF?style=for-the-badge&logo=github-actions&logoColor=white)

## 🎯 Project Overview

This collection provides automated API test scripts targeting the DemoQA Book Store API (`https://demoqa.com`). It validates core backend functionalities, security tokens, and data manipulation workflows.

As a QA Automation / API Testing Engineer, my focus in this repository is to implement robust automated assertions, handle dynamic pre-request scripts (such as generating random test users), manage collection variables, and ensure reliable API contract validation.

## 🛠️ QA Tech Stack & Tools

* **API Testing Tool:** Postman
* **CLI Runner / CI Execution:** Newman
* **Test Assertions & Scripting:** JavaScript (Chai Assertion Library built into Postman)
* **CI/CD Pipeline Support:** GitHub Actions
* **Target Environment:** DemoQA REST API

## 📊 Test Strategy & Coverage

### 1. Automated API Testing & Assertions
The Postman collection includes comprehensive test suites (`pm.test`) validating:
* **Authentication & Token Generation (`Login`):** Verifies HTTP 200 OK status, response body structure (`status: "Success"`), token existence, header presence (`Content-Type`), and minimum token length security constraints (>20 chars). Automatically captures and stores the `token` in collection variables for subsequent requests.
* **Negative Testing (`Login With Invalid Username`):** Utilizes pre-request scripts to generate dynamic random usernames (`$randomUserName`) and validates proper error handling (`status: "Failed"`, null token return).
* **Resource Management (`Add Book To Collection` & `Delete Book From Collection`):** Validates secure endpoint access using Bearer token authorization and ISBN payload processing.

### 2. Scripting Features
* **Pre-request Scripts:** Dynamic data generation (random username generation) and runtime header/environment configuration.
* **Test Scripts:** Automated assertions on status codes, response headers, JSON schemas, and dynamic variable persistence (`pm.collectionVariables.set`).

## 🚀 How to Run the Tests Locally

To run and evaluate this Postman collection locally using Node.js and Newman, follow these steps:

### 1. Prerequisites
Ensure you have Node.js installed, then install Newman globally (if not already installed):
```bash
npm install -g newman
