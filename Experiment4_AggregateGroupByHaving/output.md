## Question 1
Write a SQL Query to find how many medications are prescribed for each patient?
```
select patientID,count(medications) as AvgMedications
from MedicalRecords
group by patientID;
```
## OUTPUT
![image](https://github.com/user-attachments/assets/dc157063-2600-4f70-ab33-1578fbe033a0)

## Question 2
How many prescriptions were written for each medication?

Sample tablePrescriptions Table
```
select medication,count(*) as TotalPrescriptions
from Prescriptions 
group by medication;
```
## Output
![image](https://github.com/user-attachments/assets/e72df0bc-87ec-4200-9b4b-1ce34ffe4bf0)

## Question 3
How many male and female doctors are there in each medical specialty?

Sample table:Doctors Table
```
select specialty,gender,count(*) as TotalDoctors
from Doctors
group by specialty,gender;
```
# Output
![Screenshot 2025-05-12 181240](https://github.com/user-attachments/assets/7e52e245-92d1-4e4d-82f0-50b6d964a254)

## Question 4
Write a SQL query to find Who has the highest income among employee living in California?

Table: employee
```
select name,max(income)
from employee
where city='California'
and income=(select max(income) from employee where city ='California');
```
## Output
![image](https://github.com/user-attachments/assets/320944ff-1a9b-443b-800f-5ef35bfdf8db)

## Question 5
Write a SQL query to find how many employees have an income greater than 50K?

Table: employee
```
select count(*) as employees_count
from employee
where income>50000;
```
## Output
![Screenshot 2025-05-12 182111](https://github.com/user-attachments/assets/e8e9257b-fa21-4d22-9104-9eb4f1e9c70a)

## Question 6
Write a SQL query to  find the average salary of all employees?

Table: employee
```
select avg(income) as Average_Salary
from employee;
```
## Output
![Screenshot 2025-05-12 182744](https://github.com/user-attachments/assets/872a21e4-b3f3-41b2-89f9-e0a235c13013)

## Question 7
Write a SQL query to calculate the total number of working hours of all employees

Sample table: employee1
```
select sum(workhour) as "Total working hours"
from employee1;
```
## Output
![Screenshot 2025-05-12 183457](https://github.com/user-attachments/assets/2f676b2b-c4e3-47d5-83f7-ba152c473b26)

## Question 8
Write the SQL query that accomplishes the grouping of data by age, calculates the maximum income for each age group, and includes only those age groups where the maximum income is greater than 2,000,000.

Sample table: employee
```

select age, max(income) as "MAX(income)"
from employee
group by age
having max(income)>2000000;
```
## Output
![Screenshot 2025-05-12 184711](https://github.com/user-attachments/assets/1fc01628-5f0a-4788-9c72-ad080e62ba9f)

## Question 9
Write the SQL query that accomplishes the grouping of data by age, calculates the average income for each age group, and includes only those age groups where the average income falls between 300,000 and 500,000.

Sample table: employee
```
select age,AVG(income) as "AVG(income)"
from employee
group by age
having AVG(income) between 300000 and 500000;
```
## Output
![Screenshot 2025-05-12 185128](https://github.com/user-attachments/assets/c31cb447-fc2c-430c-8f2c-a21e5b0a8829)

## Question 10
What is the total number of appointments scheduled by each doctor?

Sample table:Appointments Table
```
select DoctorID,count(*) as TotalAppointments from Appointments
group by DoctorID;
```
## Output
![Screenshot 2025-05-12 185516](https://github.com/user-attachments/assets/b7308b9b-f85b-4f7f-b939-e38c789ea740)

## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
