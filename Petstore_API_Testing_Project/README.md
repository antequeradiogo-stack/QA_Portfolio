## Petstore API Testing Project – Manual & Automated API Validation

Diogo Antequera (ISTQB-Certified QA Tester)

Tools: Postman, Postman Scripts (JS), JSON Schema Validation, Google Sheets
Test Type: Functional API Testing • Positive & Negative Testing • CRUD Validation

⸻

## Project Overview

This project validates the functionality, reliability, and data integrity of the Swagger Petstore REST API
➡️ https://petstore.swagger.io/

The objective is to ensure that all API endpoints behave according to specifications, return the correct status codes, handle errors properly, and maintain consistent data across CRUD operations.

This work simulates a real QA workflow used in professional environments, including structured test cases, automation logic (Postman Tests), negative testing, and schema validation.

⸻

## Scope of Testing

✔ CRUD operations for Pet entities
✔ Status code validation (2xx, 4xx, 5xx)
✔ Positive & Negative test scenarios
✔ Header validation
✔ Payload structure & JSON Schema validation
✔ Response time validation (<1200 ms)
✔ Data consistency checks
✔ Error handling for:
	•	Missing fields
	•	Invalid formats
	•	Wrong HTTP methods
	•	Non-existing resources

⸻

## Out of Scope

✖ Performance/load testing (JMeter)
✖ Security testing (Auth, tokens, OWASP)
✖ UI testing
✖ Database-level validation

⸻

## Business Rules Validated
	1.	A new Pet must be created successfully if all required fields are valid.
	2.	Retrieving a Pet by ID must return the correct object.
	3.	Updating a Pet must overwrite previous data.
	4.	Deleting a Pet must return a valid confirmation.
	5.	Searching for a non-existing Pet must return 404.
	6.	Invalid payloads must produce correct error messages.
	7.	Required fields must not accept null/empty values.
	8.	API should respond within acceptable performance thresholds (<1200ms).

⸻

## Deliverables Included

# API Test Cases (Google Sheets / PDF / Excel)
  
	•	15 fully detailed test cases
	•	Endpoint, method, request body, expected & actual results
	•	Status, severity, priority
	•	Notes for real-world documentation behavior

📁 Petstore_API_Test_Cases.xlsx

📁 Petstore_API_Test_Cases.pdf

⸻

# Postman Collection (Optional in future update)

✔ Automated scripts
✔ Assertions (Status, JSON validation, headers, schema)
✔ Data-driven tests
✔ Environment variables

⸻

## Example Test Case (TC_API_01)

Feature: Create Pet
Description: Verify that a pet is created successfully with valid data.
Method: POST /pet
Expected Result: 200 OK; correct Pet object returned.
Actual Result: Pass.
Severity: High
Priority: High
Notes: Confirms full CRUD creation path.

⸻

## Skills Demonstrated
	•	API Testing (Manual & Automated)
	•	Postman & JavaScript assertions
	•	JSON schema validation
	•	Positive & negative testing
	•	Real-world bug identification
	•	Test case design (ISTQB principles)
	•	Documentation & reporting
	•	GitHub project organization

⸻

 ## Why This Project Matters

This project simulates a real QA Analyst workflow, proving ability to:
	•	Design structured test cases
	•	Validate complex API behaviors
	•	Document issues professionally
	•	Maintain clear testing standards
	•	Work independently, following industry best practices
