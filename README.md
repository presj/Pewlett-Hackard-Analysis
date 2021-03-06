Employee Database Analysis

Overview of the analysis 

Pewlett-Hackard, a large company with several thousand employees, is beginning to experience the separation of a significant number of its workers due to retirement.  In anticipation of having a high number of job vacancies, we are tasked with accessing the current employee database to determine which employees might be leaving and how many positions will need to be filled.
By updating the existing employee database, using PostgreSQL, our focus is to apply our skills in data modeling, engineering, and analysis to be prepared for the wave of upcoming retirements and help plan for future succession.  We will be generating tailored lists of employees that show the number of employees eligible for retirement per current assignment and identifying those employees eligible to participate in a mentorship program.  

Results of the analysis

•	Our first step was to access Pewlett-Hackard’s existing employee records found in six separate CSV files (Fig. 1).  Given access to the data in these files, we were next able to use a diagraming tool called Quick Database Diagrams to create a flowchart or entity-relationship diagram (ERD) referencing the data (Fig. 2).  The ERD represents the conceptual, logical, and physical data model for our database design.
 ![image](https://user-images.githubusercontent.com/100803302/163721221-929f2c53-3d15-4151-a097-35d7bced1663.png)
 
  Fig. 1


![image](https://user-images.githubusercontent.com/100803302/163721317-0fece869-8e13-4715-a1b7-8b14a9003756.png)

  Fig. 2


•	A query was written and executed to create a Retirement Titles table for employees who are born between January 1, 1952, and December 31, 1955, and expected to be retiring soon.  Figure 3 is a table that identifies employees by their employee number, first name, last name, title, from-date, and to-date.  Note: Some employees appear more than once in the below list due to their change of job title over the course of their career.

![image](https://user-images.githubusercontent.com/100803302/163721334-2fe757e0-ac4f-4695-8a40-5463e999a945.png)

  Fig. 3
 

![image](https://user-images.githubusercontent.com/100803302/163721352-775d6b82-6eb3-4789-bd0a-ac684d5eb787.png)

 Fig. 4


•	Because some employees appeared more than once in the previous list, a new query was written and executed to create a Unique Titles table (Fig. 4) that contains the employee number, first and last name, and most recent job title.

![image](https://user-images.githubusercontent.com/100803302/163721364-eca970ad-cbdd-4733-b864-5dad4702d05f.png)

 Fig. 5
 
![image](https://user-images.githubusercontent.com/100803302/163721373-4a7a873d-23a5-4269-8d63-2cd6c7b4241d.png)

 Fig. 6


•	Another query was written and executed to create a Retiring Titles table that contains the number of job titles filled by employees who are planning to retire.  This table (Fig. 5) allows us to see how many employees, with specific job titles, will be retiring.

![image](https://user-images.githubusercontent.com/100803302/163721388-2d228056-1b0b-4534-b249-2c3e31a76c2f.png)

 Fig. 7
 
![image](https://user-images.githubusercontent.com/100803302/163721402-c260bae1-c54b-4589-827c-ad3c4ab1796e.png)

 Fig. 8



Summary 
72,458 positions will need to be filled as the number of employees eligible for retirement begin leaving.  Not only is there expected to be a high number of employees retiring, but most of the vacancies will also come from senior-level positions.  The data shows of the more than 72,000 employees eligible for retirement that approximately 70% of the vacancies will be in senior-level positions.  

The number of senior-level employees leaving will create the opportunity for others to promote into these positions.  Retaining some employees who are eligible to retire, through promotion, will help to reduce the overall number of retirements.  Fig. 6 (below) represents the total number of employees in each position, to give us an idea of how many potential promotions could be made into senior-level positions.  Comparing Figures 6 and 8 shows us that we have enough employees who could move into higher positions.  Pewlett-Hackard currently staffs more than 443,000 people throughout the company.

 ![image](https://user-images.githubusercontent.com/100803302/163721421-c8dfd636-4aad-41c5-a516-eca91e7c4c83.png)
 
 Fig. 9




One strategy to help maintain staffing numbers and productivity is to delay the departure of key, senior-level workers.  This might be done by requesting that some of the retirement eligible employees stay on an extended period to mentor younger employees.  A final query was written to create a Mentorship Eligibility table (Fig. 7) that holds the employees who are eligible to participate in a mentorship program.  The table represents the 1,549 employees eligible for the mentorship program.


![image](https://user-images.githubusercontent.com/100803302/163721432-83e6c2bd-0d20-4a67-adab-32ddd3eba7ab.png)

 Fig. 10

