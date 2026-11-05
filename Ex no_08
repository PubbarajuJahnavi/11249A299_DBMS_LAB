VIEWS,SEQUENCE AND INDEXES IN ORACLE

VIEWS

CREATE TABLE employee (
employee_id INT,
first_name VARCHAR(50),
last_name VARCHAR(50),
department VARCHAR(50),
salary INT
);

INSERT INTO employee (employee_id, first_name, last_name, department, salary) VALUES
(1, 'John', 'Smith', 'Sales', 50000),
(2, 'Alice', 'Johnson', 'Marketing', 55000),
(3, 'Michael', 'Williams', 'IT', 60000),
(4, 'Emily', 'Brown', 'Human Resources', 48000),
(5, 'David', 'Jones', 'Finance', 62000),
(6, 'Sarah', 'Martinez', 'Operations', 53000);

1. Creating a View in Oracle PL/SQL
CREATE VIEW employee_view AS
SELECT employee_id, first_name, last_name, department
FROM
employee;

2. Updating a View in Oracle PL/SQL
UPDATE employee_view
SET department = 'Customer Service'
WHERE employee_id = 1;

3. Dropping a View in Oracle PL/SQL
DROP VIEW employee_view;


SQL SEQUENCES

1: Creating a Sequence in Ascending Order

CREATE SEQUENCE sequence_1
start with 1
increment by 1
minvalue 0
maxvalue 100
cycle;

2: Creating a Sequence in Descending Order

CREATE SEQUENCE sequence_2
start with 100
increment by -1
min value 1
max value 100
cycle;


INDEX

Creating Index:
CREATE INDEX idx_Stud_ID ON Students(Stud_ID);

Display Created Index from Database: 
SHOW INDEX FROM Students;

Deleting the Created Index: 
DROP INDEX idx_Stud_ID ON Students;
