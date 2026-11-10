# Human Resource Database Project

Relational database design and SQL queries for a government agency HR system, built as a team capstone project at Red River College Polytechnic.

## Team Members

    Idongesit Orok, Neil Victolria & Fatoumatta Jallow 

## Introduction

This is a human resources system for a large government agency with multiple departments and complex hierarchical structures. The database manages employees, organizational charts, payroll grades and rubrics, and benefits, with a focus on hierarchical relationships and complex organizational data.

**Tools:** MariaDB, SQL

## Business Needs

- The agency has multiple departments (Finance, IT, Public Works, etc.).
- Each department may have one or more divisions. For example, Finance has "Accounts Payable" and "Payroll"; IT has "Networking", "Tech Support", and "Hardware Acquisition". Public Works has no divisions.
- Employees have basic info (name, hire date, contact details).
- Each employee is assigned to a position with a job title and description.
- Positions have salary grades that determine pay range.
- More than one employee can occupy a position (tech support needs many L1 technicians to handle all the tickets), each with their own place in the pay range.
- Positions may have supervisors (positions supervise other positions). For example, all on-duty L1 technicians in tech support report to the on-duty L2 technician.
- Employees can be promoted or transferred between positions and departments.
- Employment history within the agency must be tracked.
- Pay scales are adjusted annually, and historical pay data must be maintained.
- Some (but not all) positions are union-represented. There are multiple unions, each covering different positions. No position can be covered by more than one union.
- For employees in union-covered positions, their place in the pay range is determined by their years of continuous service within that union and that union's pay range rules.
- For employees not in union-covered positions, their place in the pay range is determined by their total years of service to the agency.

## Entity Relationship Diagram (ERD)

<img width="1156" height="512" alt="capstone_project_draft drawio" src="https://github.com/user-attachments/assets/6bfee890-68a2-47f1-8180-9bd6eee61231" />


## Query Challenges

1. List all employees currently working in IT, along with their division and job title.
2. Show the complete organizational structure of Finance – list each position and to whom it reports (if any).
3. Among all employees who have never changed position, find who has worked the longest.
4. Calculate the current pay of "Sarah Johnson", factoring in her years of service and the pay rules of her current position.
5. Find all vacant positions (positions with no one assigned to them).
6. List all employees who have been promoted at least twice (changed to a job that supervised their previous one).
7. List all employees who report (directly or indirectly) to "Inderjeet Singh", the current Director of IT.
8. List all of Inderjeet Singh's previous positions and the pay he was receiving on his last day in each.
9. Group employees by their union (or lack of one) and list the results in descending order of count.

## How to Run

1. Install MariaDB (or MySQL).
2. Run the schema file to create the database and tables.
3. Run the data file to insert the sample records.
4. Run the queries file to see the results of each query challenge.
