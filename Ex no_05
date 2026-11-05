JOINS

1. INNER JOIN
SELECT s.student_id, s.student_name, d.dept_name
FROM Students s
INNER JOIN Departments d
ON s.dept_id = d.dept_id;

2.LEFT JOIN
SELECT s.student_id, s.student_name, d.dept_name
FROM Students s
LEFT JOIN Departments d
ON s.dept_id = d.dept_id;

3.RIGHT JOIN
SELECT s.student_id, s.student_name, d.dept_name
FROM Students s
RIGHT JOIN Departments d
ON s.dept_id = d.dept_id;

4.FULL OUTER JOIN
SELECT s.student_id, s.student_name, d.dept_name
FROM Students s
FULL OUTER JOIN Departments d
ON s.dept_id = d.dept_id;

5. CROSS JOIN
SELECT s.student_name, d.dept_name
FROM Students s
CROSS JOIN Departments d;

6. SELF JOIN
SELECT
e.emp_name AS Employee,
m.emp_name AS Manager
FROM Employees e
LEFT JOIN Employees m
ON e.manager_id = m.emp_id;

7.INNER JOIN with Condition
SELECT s.student_id, s.student_name, d.dept_name
FROM Students s
INNER JOIN Departments d
ON s.dept_id = d.dept_id
WHERE d.dept_name = 'CSE';

 8.JOIN + WHERE
SELECT s.student_name
FROM Students s
INNER JOIN Departments d
ON s.dept_id = d.dept_id
WHERE d.dept_name = 'IT';

9 JOIN + ORDER BY
SELECT s.student_name, d.dept_name
FROM Students s
INNER JOIN Departments d
ON s.dept_id = d.dept_id
ORDER BY d.dept_name ASC;

10 JOIN + COUNT
SELECT d.dept_name,
COUNT(s.student_id) AS total_students
FROM Departments d
LEFT JOIN Students s
ON d.dept_id = s.dept_id
GROUP BY d.dept_name;
