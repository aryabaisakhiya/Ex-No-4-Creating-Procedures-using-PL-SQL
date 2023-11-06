# Ex. No: 4 Creating Procedures using PL/SQL
##DATE:


### AIM: To create a procedure using PL/SQL.

### Steps:
1. Create employee table with following attributes (empid NUMBER, empname VARCHAR(10), dept VARCHAR(10),salary NUMBER);
2. Create a procedure named as insert_employee data.
3. Inside the procdure block, write the query for inserting the values into the employee table.
4. End the procedure.
5. Call the insert_employee data procedure to insert the values into the employee table.
6. Display the employee table

### Program:
```
SQL> CREATE TABLE employee2(
     empid NUMBER,
     empname VARCHAR(10),
     dept VARCHAR(10),
     salary NUMBER
    );
CREATE OR REPLACE PROCEDURE employee_data AS
    BEGIN
    INSERT INTO employee2(empid,empname,dept,salary)
    values(1,'John','HR',50000);
    INSERT INTO employee2(empid,empname,dept,salary)
    values(2,'Joe','IT',600000);
    INSERT INTO employee2(empid,empname,dept,salary)
    values(3,'Bob','Finance',550000);
    COMMIT;
   FOR emp_rec IN (SELECT * FROM employee2)LOOP
   DBMS_OUTPUT.PUT_LINE('EMPLOYEE ID:'||emp_rec.empid||',EMPLOYEE NAME:'|| emp_rec.empname||
   ',DEPARTMENT:'||emp_rec.dept||',SALARY:'||emp_rec.salary);
   END LOOP;
   END;
  /
```

### Output:
![dbms procedure](https://github.com/aryabaisakhiya/Ex-No-4-Creating-Procedures-using-PL-SQL/assets/119393645/f823ba53-682c-4661-a835-d9b31353e8d5)


### Result:
THE PROGRAM HAS BEEN IMPLEMENTED SUCCESSFULLY
