Practicing DCL&TCL Commands

DCL COMMANDS:

1. GRANT Command
CREATE TABLE students (
reg_no NUMBER PRIMARY KEY,
name VARCHAR2(50),
department VARCHAR2(20),
marks NUMBER
);
GRANT SELECT ON students TO student1;

2. Grant Multiple Privileges
GRANT SELECT, INSERT, UPDATE
ON students
TO student1;

3. GRANT All Privileges
GRANT ALL
ON students
TO student1;

4. REVOKE Command
Remove UPDATE permission:
REVOKE UPDATE
ON students
FROM student1;
Now student1 can no longer execute:
UPDATE students
SET marks = 90
WHERE reg_no = 101;

TCL COMMAMDS:
1. COMMIT
INSERT INTO students VALUES (101, 'Arun', 'CSE', 85);
COMMIT;

2. ROLLBACK
UPDATE students
SET marks = 90
WHERE reg_no = 101;
ROLLBACK;

3. SAVEPOINT
INSERT INTO students VALUES (101, 'Arun', 'CSE', 85);
SAVEPOINT sp1;
INSERT INTO students VALUES (102, 'Priya', 'ECE', 90);
ROLLBACK TO sp1;

4. ROLLBACK TO
ROLLBACK TO sp1;
