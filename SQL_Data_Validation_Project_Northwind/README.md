SQL Data Validation Project – Northwind Database

By Diogo Antequera (ISTQB-Certified QA Tester)

 Project Overview

This project validates data integrity, referential consistency, and business rule enforcement in the Northwind demo database using SQL.
The objective is to ensure that relationships between tables are correct, required fields contain valid data, and no corrupted or orphaned records exist.

This work reflects real-world backend QA testing, where data validation is essential for preventing critical defects in production environments.

⸻

Objectives
	•	Validate customer, order, product, employee, and category consistency
	•	Ensure referential integrity between related tables
	•	Detect invalid, missing, or logically incorrect values
	•	Confirm compliance with business rules and constraints
	•	Apply ISTQB-aligned validation techniques

⸻

Scope of Testing
	•	Customer data validation
	•	Order & Order Details consistency
	•	Product–Category relationships
	•	Employee hierarchy validation
	•	Referential integrity (FK → PK relationships)
	•	Edge cases: nulls, invalid references, missing associations

⸻

 Business Rules Validated
	1.	Every order must belong to an existing customer
	2.	Every order must be handled by an existing employee
	3.	Discontinued products must not appear in new orders
	4.	Every product must belong to a valid category
	5.	Every order must contain at least one order detail line
	6.	Employees must report to valid managers (if ReportsTo is not null)
	7.	Unit price must always be greater than 0
	8.	Customer company names must never be null
	9.	ShipDate cannot be earlier than OrderDate
	10.	Freight must be ≥ 0
	11.	Category table must not contain empty categories
	12.	ProductName cannot be empty or null
	13.	Discount must be between 0 and 1
	14.	BirthDate must be earlier than HireDate
	15.	Calculated order subtotals must be > 0

⸻

Test Artifacts Included

This project includes:
	•	✔️ 15 detailed SQL Test Cases
	•	✔️ Expected vs Actual Results
	•	✔️ Status (Pass/Fail)
	•	✔️ Severity and Priority
	•	✔️ Structured documentation aligned with ISTQB standards

⸻

Tools Used
	•	W3Schools SQL Tryit Editor (query execution)
	•	Google Sheets (documentation)
	•	SQL Validation Techniques (manual backend QA)

⸻

Files in This Folder
	•	SQL_Data_Validation_Project_Northwind.xlsx – Full test case suite
	•	README.md – Project documentation
	•	Any exported PDFs (if added later)

⸻

What This Project Demonstrates
	•	Strong understanding of backend testing
	•	Ability to identify data anomalies, logic errors, and referential inconsistencies
	•	Practical SQL query-writing skills
	•	Capability to build complete QA documentation from scratch
	•	Professional project delivery suitable for portfolio and recruiters
