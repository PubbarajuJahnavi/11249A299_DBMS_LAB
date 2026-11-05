Queries Using ANY, ALL, IN, EXISTS, NOT EXISTS, UNION, INTERSECT, Aggregate Functions, GROUP BY and HAVING

1. Create Tables

DEPARTMENT
CREATE TABLE department (
dept_id NUMBER(3) PRIMARY KEY,
dept_name VARCHAR2(30) NOT NULL
);

STUDENT
CREATE TABLE student (
roll_no NUMBER(5) PRIMARY KEY,
name VARCHAR2(30) NOT NULL,
age NUMBER(2),
marks NUMBER(5,2),
dept_id NUMBER(3),
FOREIGN KEY (dept_id) REFERENCES department(dept_id)
);

2. Insert Sample Data in

Department Data
INSERT INTO department VALUES (10, 'CSE');
INSERT INTO department VALUES (20, 'IT');
INSERT INTO department VALUES (30, 'ECE');
INSERT INTO department VALUES (40, 'MECH');
INSERT INTO department VALUES (50, 'CIVIL');

Student Data
INSERT INTO student VALUES (101, 'Arun', 20, 85, 10);
INSERT INTO student VALUES (102, 'Priya', 19, 92, 10);
INSERT INTO student VALUES (103, 'Kumar', 21, 76, 20);
INSERT INTO student VALUES (104, 'Divya', 20, 88, 20);
INSERT INTO student VALUES (105, 'Ravi', 22, 65, 30);
INSERT INTO student VALUES (106, 'Anu', 19, 95, 30);
INSERT INTO student VALUES (107, 'Suresh', 21, 72, 10);
INSERT INTO student VALUES (108, 'Meena', 20, 81, 40);

COMMIT;

Query 1: Find students from CSE and IT
SELECT *
FROM student
WHERE dept_id IN (10, 20);

Query 2: Find students whose marks are 65, 76 or 85
SELECT *
FROM student
WHERE marks IN (65, 76, 85);

Query 3: Find students belonging to CSE
Using a subquery:
SELECT *
FROM student
WHERE dept_id IN
(
SELECT dept_id
FROM department
WHERE dept_name = 'CSE'
);


Queries Using ANY
4. ANY Operator

Query 4: Find students whose marks are greater than any CSE student
SELECT name, marks
FROM student
WHERE marks > ANY
(
SELECT marks
FROM student
WHERE dept_id = 10
);


Queries Using ALL
5. ALL Operator

Query 6: Find students whose marks are greater than all CSE students
SELECT name, marks
FROM student
WHERE marks > ALL
(
SELECT marks
FROM student
WHERE dept_id = 10
);

Query 7: Find students whose marks are less than all CSE students
SELECT name, marks
FROM student
WHERE marks < ALL
(
SELECT marks
FROM student
WHERE dept_id = 10
);


EXISTS
6. EXISTS Operator

Query 8: Find departments that have students
SELECT dept_name
FROM department d
WHERE EXISTS
(
SELECT 1
FROM student s
WHERE s.dept_id = d.dept_id
);


NOT EXISTS
7. NOT EXISTS Operator

Query 9: Find departments that do not have any students
SELECT dept_name
FROM department d
WHERE NOT EXISTS
(
SELECT 1
FROM student s
WHERE s.dept_id = d.dept_id
);


UNION
8. UNION Operator

Query 10: Students who scored above 90 OR are below age 20
SELECT name
FROM student
WHERE marks > 90
UNION
SELECT name
FROM student
WHERE age < 20;


9. UNION ALL
SELECT name
FROM student
WHERE marks > 80
UNION ALL
SELECT name
FROM student
WHERE age < 21;


INTERSECT
10. INTERSECT Operator

Query 11: Students who scored above 80 AND are below age 21
SELECT name
FROM student
WHERE marks > 80
INTERSECT
SELECT name
FROM student
WHERE age < 21;


GROUP BY
11. GROUP BY Clause

Query 19: Count students in each department
SELECT dept_id, COUNT(*) AS total_students
FROM student
GROUP BY dept_id;

12. Average Marks Department-wise
Query 20
SELECT dept_id, AVG(marks) AS average_marks
FROM student
GROUP BY dept_id;

13. Total Marks Department-wise
Query 21
SELECT dept_id, SUM(marks) AS total_marks
FROM student
GROUP BY dept_id;

14. Highest and Lowest Marks Department-wise
Query 22
SELECT
dept_id,
MAX(marks) AS highest_mark,
MIN(marks) AS lowest_mark
FROM student
GROUP BY dept_id;

GROUP BY with Department Name
Query 23
SELECT
d.dept_name,
COUNT(s.roll_no) AS total_students,
AVG(s.marks) AS average_marks
FROM department d
JOIN student s
ON d.dept_id = s.dept_id
GROUP BY d.dept_name;

HAVING
21. HAVING Clause

Query 24: Find departments having more than 2 students
SELECT dept_id, COUNT(*) AS total_students
FROM student
GROUP BY dept_id
HAVING COUNT(*) > 2;

Query 25: Find departments whose average mark is greater than 80
SELECT dept_id, AVG(marks) AS average_marks
FROM student
GROUP BY dept_id
HAVING AVG(marks) > 80;

Query 26: Find departments whose highest mark is greater than 90
SELECT dept_id, MAX(marks) AS highest_mark
FROM student
GROUP BY dept_id
HAVING MAX(marks) > 90;

WHERE + GROUP BY + HAVING

Query 27
Find the average marks of students who scored at least 70, department-wise, and display only departments whose average is greater than 80.
SELECT
dept_id,
AVG(marks) AS average_marks
FROM student
WHERE marks >= 70
GROUP BY dept_id
HAVING AVG(marks) > 80;
