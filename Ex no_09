PL/SQL Block in Oracle

1. Structure of a PL/SQL Block
DECLARE
-- Variable declarations
variable_name datatype;
BEGIN
-- Executable statements
SQL statements;
EXCEPTION
-- Error handling statements
WHEN exception_name THEN
statements;
END;
/

1.PL/SQL program to check whether a given number is Odd or Even
SET SERVEROUTPUT ON;
DECLARE
    n NUMBER := &n;
BEGIN
    IF MOD(n, 2) = 0 THEN
        DBMS_OUTPUT.PUT_LINE('Number is even');
    ELSE
        DBMS_OUTPUT.PUT_LINE('Number is odd');
    END IF;
END;
/



2.PL/SQL program to print the multiplication table of a given number (1 to 10).
SET SERVEROUTPUT ON;

DECLARE
    n NUMBER;
    i NUMBER;

BEGIN
    n := &n;

    FOR i IN 1..10
    LOOP
        DBMS_OUTPUT.PUT_LINE(n || ' x ' || i || ' = ' || n*i);
    END LOOP;

END;
/



3.PL/SQL program to find the Factorial of a given number.
SET SERVEROUTPUT ON;

DECLARE
    n NUMBER;
    fac NUMBER := 1;
    i NUMBER;

BEGIN
    n := &n;

    FOR i IN 1..n
    LOOP
        fac := fac * i;
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Factorial = ' || fac);

END;
/



4.PL/SQL program to print the Fibonacci Series.
SET SERVEROUTPUT ON;

DECLARE
    first NUMBER := 0;
    second NUMBER := 1;
    third NUMBER;
    n NUMBER := &n;
    i NUMBER;

BEGIN
    DBMS_OUTPUT.PUT_LINE('Fibonacci series is:');
    DBMS_OUTPUT.PUT_LINE(first);
    DBMS_OUTPUT.PUT_LINE(second);

    FOR i IN 2..n
    LOOP
        third := first + second;
        first := second;
        second := third;

        DBMS_OUTPUT.PUT_LINE(third);
    END LOOP;

END;
/



5.PL/SQL program to Reverse a Number.
SET SERVEROUTPUT ON;

DECLARE
    n NUMBER;
    i NUMBER;
    rev NUMBER := 0;
    r NUMBER;

BEGIN
    n := &n;

    WHILE n > 0
    LOOP
        r := MOD(n, 10);
        rev := (rev * 10) + r;
        n := TRUNC(n / 10);
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Reverse is ' || rev);

END;
/



6.PL/SQL program to Reverse a String.
SET SERVEROUTPUT ON;

DECLARE
    str1 VARCHAR2(50) := '&str';
    str2 VARCHAR2(50);
    len NUMBER;
    i NUMBER;

BEGIN
    len := LENGTH(str1);

    FOR i IN REVERSE 1..len
    LOOP
        str2 := str2 || SUBSTR(str1, i, 1);
    END LOOP;

    DBMS_OUTPUT.PUT_LINE('Reverse of String is: ' || str2);

END;
/



PL/SQL Programs for Predefined Exceptions in Oracle

1. ZERO_DIVIDE
DECLARE
A NUMBER := 10;
B NUMBER := 0;
C NUMBER;
BEGIN
C := A / B;
DBMS_OUTPUT.PUT_LINE('Result = ' || C);
EXCEPTION
WHEN ZERO_DIVIDE THEN
DBMS_OUTPUT.PUT_LINE('Error: Cannot divide by zero');
END;
/

2. NO_DATA_FOUND
DECLARE
A NUMBER := 10;
B NUMBER := 0;
C NUMBER;
BEGIN
C := A / B;
DBMS_OUTPUT.PUT_LINE('Result = ' || C);
EXCEPTION
WHEN ZERO_DIVIDE THEN
DBMS_OUTPUT.PUT_LINE('Error: Cannot divide by zero');
END;
/
