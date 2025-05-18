# Experiment 4: Aggregate Functions, Group By and Having Clause

## AIM
To study and implement aggregate functions, GROUP BY, and HAVING clause with suitable examples.

## THEORY

### Aggregate Functions
These perform calculations on a set of values and return a single value.

- **MIN()** – Smallest value  
- **MAX()** – Largest value  
- **COUNT()** – Number of rows  
- **SUM()** – Total of values  
- **AVG()** – Average of values

**Syntax:**
```sql
SELECT AGG_FUNC(column_name) FROM table_name WHERE condition;
```
### GROUP BY
Groups records with the same values in specified columns.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name;
```
### HAVING
Filters the grouped records based on aggregate conditions.
**Syntax:**
```sql
SELECT column_name, AGG_FUNC(column_name)
FROM table_name
GROUP BY column_name
HAVING condition;
```

**Question 1**

![image](https://github.com/user-attachments/assets/62055eb0-48cc-42a7-a900-f7ab05c795c1)

```sql
SELECT DoctorID,COUNT(RecordID)AS TotalRecords
FROM MedicalRecords 
GROUP BY DoctorID
```

**Output:**

![image](https://github.com/user-attachments/assets/a5f4c2ed-9300-407e-8184-8ccc11a08750)

**Question 2**

![image](https://github.com/user-attachments/assets/518db1a6-af55-40b7-8414-6c8f854c4aea)

```sql
SELECT CAST(SUBSTR(ValidityPeriod,1,4) AS INTEGER) AS ValidityYear, COUNT(DISTINCT PatientID) AS TotalPatients
FROM Insurance
GROUP BY CAST(SUBSTR(ValidityPeriod,1,4) AS INTEGER)
ORDER BY ValidityYear;
```

**Output:**

![image](https://github.com/user-attachments/assets/ba3871c5-8783-4664-a689-d198338920bf)

**Question 3**

![image](https://github.com/user-attachments/assets/64da832c-0891-4b85-a8d2-553811b3422e)

```sql
SELECT DoctorID,COUNT(AppointmentID) AS TotalAppointments
FROM Appointments
GROUP BY DoctorID
```

**Output:**

![image](https://github.com/user-attachments/assets/e52f49d6-94da-4d1b-9e86-61f38ce17447)

**Question 4**

![image](https://github.com/user-attachments/assets/6d44a5a6-7355-4208-8ba3-7276333e57bd)

```sql
SELECT name,MAX(LENGTH(name)) AS length
FROM customer
```

**Output:**

![image](https://github.com/user-attachments/assets/5b843877-cf73-4ec1-997a-f29839f304d0)

**Question 5**

![image](https://github.com/user-attachments/assets/8043ac55-4a51-4f24-a6b3-7e66199b7d82)

```sql
SELECT AVG(income) AS avg_income
FROM employee
WHERE name LIKE "A%";
```

**Output:**

![image](https://github.com/user-attachments/assets/f2d1cd23-5353-434c-8fe8-1cbef12c8396)

**Question 6**

![image](https://github.com/user-attachments/assets/72431fd8-5e4e-4636-9c37-c3c22ca42398)

```sql
SELECT COUNT(id) AS employees_in_california
FROM employee
WHERE city ="California";
```

**Output:**

![image](https://github.com/user-attachments/assets/78e5ba76-8cd6-4d20-b9ed-3d2f1095846c)

**Question 7**

![image](https://github.com/user-attachments/assets/3515ee75-17aa-4a57-b4e5-7d33f53bd9f2)

```sql
SELECT name AS fruit_name,MIN(inventory) AS lowest_quantity
FROM fruits
```

**Output:**

![image](https://github.com/user-attachments/assets/442586b0-ef51-428d-a8c2-85ae4ea0ee17)

**Question 8**

![image](https://github.com/user-attachments/assets/9b5f5b9d-9462-49b3-a345-0e3a2288a341)

```sql
SELECT jdate,AVG(workhour) AS "AVG(workhour)"
FROM employee1
GROUP BY jdate
HAVING AVG(workhour)<10;
```

**Output:**

![image](https://github.com/user-attachments/assets/7eef66d8-479e-48d6-acec-4e9dc9ef702d)

**Question 9**

![image](https://github.com/user-attachments/assets/7c3123c2-b8c1-437a-a8d5-63507b59aa5c)

```sql
SELECT address,AVG(salary) AS "AVG(salary)"
FROM customer1
GROUP BY address
HAVING AVG(salary)<15000;
```

**Output:**

![image](https://github.com/user-attachments/assets/630b5ae2-eb66-406c-88d5-8e58cd47f42c)

**Question 10**

![image](https://github.com/user-attachments/assets/a82df8ee-5b55-44a6-8c3d-0ce0e4c8453e)

```sql
SELECT age,MIN(income) AS "MIN(income)"
FROM employee
GROUP BY age
HAVING MIN(income)<400000;
```

**Output:**

![image](https://github.com/user-attachments/assets/18091313-5f8b-4baa-ae54-f8f9d515fae0)

## RESULT
Thus, the SQL queries to implement aggregate functions, GROUP BY, and HAVING clause have been executed successfully.
