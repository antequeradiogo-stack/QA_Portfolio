# QA_Portfolio
# QA Tester Portfolio – Diogo Antequera

This repository showcases my practical skills as a **Quality Assurance Tester**, covering the complete QA lifecycle — from test planning and design to execution, bug reporting, and API validation.

## Project Structure
- **Test_Plan.docx:** Detailed test plan including scope, strategy, environment, and tools  
- **Web_Test_Cases.xlsx:** Functional and regression test cases for web application testing  
- **Bug_Reports.pdf:** Examples of documented bugs with detailed reproduction steps and evidence  
- **API_Tests.postman_collection.json:** API tests created and automated using Postman  
- **SQL_Test_Queries.txt:** Sample SQL queries for data validation  
- **README.md:** Project overview and documentation

## Tools & Technologies
| Category | Tools |
|-----------|--------|
| Test Management | Zephyr, TestRail |
| Project Tracking | Jira, Azure DevOps |
| API Testing | Postman |
| Version Control | Git, GitHub |
| Documentation | Confluence |
| Database | SQL |
| Business Platform | Salesforce |

## Project Context
The project simulates QA testing within a **Salesforce Sandbox environment**, involving functional, regression, and API validation processes.  
Test documentation, reporting, and execution were carried out using the listed QA tools to reflect real-world practices.

## Key Skills Demonstrated
- Test planning, design, and execution (aligned with ISTQB standards)  
- Bug reporting and prioritization using Jira  
- Functional and API testing (manual and automated)  
- Data validation using SQL  
- Documentation and collaboration through Confluence  
- Version control and workflow management via Git & Azure DevOps

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

