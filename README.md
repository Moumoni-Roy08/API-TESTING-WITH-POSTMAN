# API-TESTING-WITH-POSTMAN

*COMPANY* : CODTECH IT SOLUTIONS

*NAME* : MOUMONI ROY

*INTERN ID* : CT08MZR

*DOMAIN* : AUTOMATION TESTING

*DURATION* : 4 WEEKS

*MENTOR* :  NEELA SANTOSH


# API Testing Report

## 📌 Task Overview
The task involved creating and executing test cases for a **REST API** using **Postman** or **Newman CLI**. The objective was to validate API responses by asserting **status codes, response structure, and specific data fields**. The tests covered:
✅ Response time validation  
✅ Response format validation  
✅ Required fields existence  
✅ Content-type validation  
✅ Invalid input handling  
✅ User creation verification  

## 📌 Solution
Using **Postman**, a series of test scripts were written to ensure the API's functionality. The following test cases were implemented:

### ✅ Response Time Validation
- Ensured the API response time was **below 200ms**.

### ✅ Required Fields Validation
- Checked for **id, name, and email fields** in the response.

### ✅ Status Code Validation
- Confirmed the API returned a **200 status code** for successful requests.

### ✅ Response Format Validation
- Verified that the response was in **JSON format**.

### ✅ Field Existence Validation
- Ensured the **name** field was present in the response.

### ✅ Specific Value Check
- Validated that the **first user’s name** matched the expected value (`Leanne Graham`).

### ✅ Content-Type Validation
- Ensured the API returned the correct `Content-Type: application/json`.

### ❌ Invalid Input Handling
- Expected a **400 status code** for invalid inputs, but received **200 OK** instead.

### ✅ User Creation Verification
- Checked if a new user was successfully created and its **ID stored**.

### ✅ Fetch and Verify Created User
- Retrieved the created user and compared it with the **stored ID**.

## 📌 Tools Used
🛠 **Postman** – Used to create, execute, and validate API requests.  
🛠 **Newman (Optional)** – CLI tool for running Postman collections in automated environments.  
🛠 **JavaScript** – Used for writing **test scripts** in Postman.

## 📌 Test Results

| **Test Case** | **Status** |
|--------------|------------|
| Response time should be less than 200ms | ✅ Passed |
| Response body contains required fields (id, name, email) | ✅ Passed |
| Status code is 200 | ✅ Passed |
| Response should be in JSON format | ✅ Passed |
| First user has name field | ✅ Passed |
| First user has name 'Leanne Graham' | ✅ Passed |
| Content-Type is application/json | ✅ Passed |
| Status code is 400 for invalid input | ❌ Failed (Expected 400 but got 200) |
| User is created successfully | ✅ Passed |
| Fetch created user | ✅ Passed |
| User is created and ID is stored | ✅ Passed |
| Fetch created user and verify ID | ✅ Passed |

## 📌 Issues and Debugging
The test for **handling invalid input failed** because the API returned a **200 OK** response instead of the expected **400 Bad Request**. Possible causes include:

- The API does **not handle invalid input correctly**.
- The **test request** might not be sending an actual invalid input.
- The API may have **default handling that redirects or modifies bad requests**.

## 📌 Next Steps
🔹 Review the API's **error handling mechanism**.  
🔹 Confirm if the **invalid input test request is correctly structured**.  
🔹 Check **API documentation** for expected behavior regarding invalid inputs.  

---

📄 This report documents the API testing process, covering **implemented test cases, tools used, test results, and areas for improvement**.

🚀 Happy Testing! 🚀
