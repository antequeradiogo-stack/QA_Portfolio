# QA_Portfolio
# QA Tester Portfolio – Diogo Antequera

This repository showcases my practical skills as a **Quality Assurance Tester**, covering the complete QA lifecycle — from test planning and design to execution, bug reporting, and API validation.

## Project Structure
| File                                  | Description                                                           |
| ------------------------------------- | --------------------------------------------------------------------- |
| **Test_Plan.docx**                    | Detailed test plan including scope, strategy, environment, and risks. |
| **Web_Test_Cases.xlsx**               | Functional, regression, API and database validation test cases.       |
| **Bug_Reports.pdf**                   | Example of documented defects with reproduction steps and evidence.   |
| **API_Tests.postman_collection.json** | API tests created and executed in Postman.                            |
| **SQL_Test_Queries.txt**              | SQL queries for backend data validation.                              |
| **API_Results.txt**                   | Recorded API test results including response codes and times.         |
| **README.md**                         | Project documentation and overview.                                   |

## Tools & Technologies
| Category | Tools |
|-----------|--------|
| Test Management | Zephyr, TestRail |
| Project Tracking | Jira, Azure DevOps |
| API Testing | Postman |
| Version Control | Git, GitHub |
| Documentation | Confluence |
| Database | SQL (MySQL test environment) |
| Business Platform | Salesforce Sandbox |

## Project Context
The project simulates QA testing within a **Salesforce Sandbox environment**, involving functional, regression, and API validation processes.  
Test documentation, reporting, and execution were carried out using the listed QA tools to reflect real-world practices.

## Key Skills Demonstrated
- End-to-end QA process – test planning, design, and execution (aligned with ISTQB standards).
- Manual testing across functional web features and user workflows.
- API validation using Postman collections and assertions.
- Database validation through SQL queries to ensure data integrity.
- Bug reporting and traceability using Jira.
- Test case management simulated in Zephyr / TestRail.
- Documentation and collaboration through Confluence and Azure DevOps.
- Version control using Git & GitHub for project organization.

## Test Execution Summary

A total of 10 test cases were designed and executed covering functional, API, and database validation.
| Area                | Scope                                       | Status       | Tools Used            |
| ------------------- | ------------------------------------------- | ------------ | --------------------- |
| Functional (UI)     | Login, Registration, Search, Cart, Checkout | ✅ All Passed | Manual testing        |
| API Testing         | GET and POST endpoints validation           | ✅ All Passed | Postman               |
| Database Validation | SQL queries for data persistence            | ✅ Verified   | MySQL / SQL Workbench |
| Regression Suite    | Core flows post-deployment                  | ✅ Executed   | TestRail simulation   |

 ## API Testing (Postman)

This section demonstrates hands-on API testing using Postman and the public API ReqRes (https://reqres.in
).
The goal was to validate the functionality of the POST /api/users endpoint and confirm data persistence through automated scripts.

Test Objective:
Validate that new users can be created successfully via the API and verify the correctness of the response data.

Request:

POST https://reqres.in/api/users
Content-Type: application/json

{
  "name": "Diogo",
  "job": "QA Tester"
}


Expected Response:

{
  "name": "Diogo",
  "job": "QA Tester",
  "id": "random",
  "createdAt": "2025-11-07T..."
}


Validation Criteria:

✅ Status code 201 Created

✅ Response contains 'id' and 'createdAt' fields

✅ Response body echoes (name, job)

✅ Response time < 1000ms

Postman Test Script:

pm.test("Status code is 201", function () {
    pm.response.to.have.status(201);
});

pm.test("Response includes required fields", function () {
    const jsonData = pm.response.json();
    pm.expect(jsonData).to.have.property("id");
    pm.expect(jsonData).to.have.property("createdAt");
    pm.expect(jsonData.name).to.eql("Diogo");
    pm.expect(jsonData.job).to.eql("QA Tester");
});


Result:
All tests passed successfully ✅
Response time: 217ms
Environment: Postman Web + Cloud Agent

## Contact
📧 diogo.antequera@email.com  
🔗 [LinkedIn](https://linkedin.com/in/diogoantequera)

💻 GitHub

---

> This portfolio was created to demonstrate practical QA competencies across multiple tools and methodologies, combining manual testing, API testing, and documentation within a professional workflow.

