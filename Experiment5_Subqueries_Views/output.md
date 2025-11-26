From the following tables write a SQL query to count the number of customers with grades above the average in New York City. Return grade and count.

SELECT grade, COUNT(*) 
FROM customer
WHERE grade > (
    SELECT AVG(grade)
    FROM customer
    WHERE city = 'New York'
)
GROUP BY grade;
Output
Screenshot 2025-05-12 190916

Question 2
Write a SQL query to retrieve all columns from the CUSTOMERS table for customers whose salary is LESS than $2500.

Sample table: CUSTOMERS

SELECT * 
FROM CUSTOMERS
WHERE SALARY < 2500;
Output
Screenshot 2025-05-12 191104

Question 3
From the following tables, write a SQL query to find those salespeople who earned the maximum commission. Return ord_no, purch_amt, ord_date, and salesman_id.

salesman table

SELECT ord_no, purch_amt, ord_date, salesman_id
FROM orders
WHERE salesman_id IN (
    SELECT salesman_id
    FROM salesman
    WHERE commission = (
        SELECT MAX(commission)
        FROM salesman
    )
);
Output
Screenshot 2025-05-12 191237

Question 4
Write a SQL query to Find employees who have an age less than the average age of employees with incomes over 1 million

Employee Table

SELECT *
FROM Employee
WHERE age < (
    SELECT AVG(age)
    FROM Employee
    WHERE income > 1000000
);
Output
Screenshot 2025-05-12 191358

Question 5
Write a SQL query to retrieve all columns from the CUSTOMERS table for customers whose AGE is LESS than $30

Sample table: CUSTOMERS

SELECT * 
FROM CUSTOMERS
WHERE AGE < 30;
Output
Screenshot 2025-05-12 191600

Question 6
Write a SQL query that retrieves the names of students and their corresponding grades, where the grade is equal to the minimum grade achieved in each subject.

Sample table: GRADES (attributes: student_id, student_name, subject, grade)

SELECT student_name, grade
FROM GRADES
WHERE (subject, grade) IN (
    SELECT subject, MIN(grade)
    FROM GRADES
    GROUP BY subject
);
Output
Screenshot 2025-05-12 191744

Question 7
Write a SQL query to retrieve all columns from the CUSTOMERS table for customers whose salary is greater than $1500.

Sample table: CUSTOMERS

SELECT * 
FROM CUSTOMERS
WHERE SALARY > 1500;
Output
image

Question 8
Write a SQL query to Retrieve the medications with dosages equal to the highest dosage

Table Name: Medications (attributes: medication_id, medication_name, dosage)

select *
from Medications
where dosage=(select max(dosage) from medications);
Output
Screenshot 2025-05-12 192711

Question 9
Write a SQL query to retrieve all columns from the CUSTOMERS table for customers whose salary is greater than $4500.

Sample table: CUSTOMERS

select * 
from customers
where salary >4500;
Output
image

Question 10
Write a SQL query that retrieve all the columns from the table "Grades", where the grade is equal to the maximum grade achieved in each subject.

Sample table: GRADES (attributes: student_id, student_name, subject, grade)

select *
from GRADES t1
where grade=(select max(grade) from GRADES t2
where t2.subject=t1.subject);
Output
image

RESULT
Thus, the SQL queries to implement subqueries and views have been executed successfully.

