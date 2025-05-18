# Experiment 3: DML Commands

## AIM
To study and implement DML (Data Manipulation Language) commands.

## THEORY

### 1. INSERT INTO
Used to add records into a relation.
These are three type of INSERT INTO queries which are as
A)Inserting a single record
**Syntax (Single Row):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES (value_1, value_2, ...);
```
**Syntax (Multiple Rows):**
```sql
INSERT INTO table_name (field_1, field_2, ...) VALUES
(value_1, value_2, ...),
(value_3, value_4, ...);
```
**Syntax (Insert from another table):**
```sql
INSERT INTO table_name SELECT * FROM other_table WHERE condition;
```
### 2. UPDATE
Used to modify records in a relation.
Syntax:
```sql
UPDATE table_name SET column1 = value1, column2 = value2 WHERE condition;
```
### 3. DELETE
Used to delete records from a relation.
**Syntax (All rows):**
```sql
DELETE FROM table_name;
```
**Syntax (Specific condition):**
```sql
DELETE FROM table_name WHERE condition;
```
### 4. SELECT
Used to retrieve records from a table.
**Syntax:**
```sql
SELECT column1, column2 FROM table_name WHERE condition;
```
**Question 1**

![image](https://github.com/user-attachments/assets/20dd11b0-d1b1-4a54-bf17-8309abfb3d1b)

```sql
update employees
set first_name='John'
where department_id=80
and commission_pct<0.35;
```

**Output:**

![image](https://github.com/user-attachments/assets/1fe89747-49f5-4101-8a0c-59b95aca8b02)

**Question 2**

![image](https://github.com/user-attachments/assets/094ef05e-62c4-4f6f-8c3d-fc5056a5928f)

```sql
update sales
set sell_price=sell_price*0.05+50
where product_id=15 and sale_date='2023-01-31';
```

**Output:**

![image](https://github.com/user-attachments/assets/40a2cbec-63e0-4046-866c-f4d4b05a3289)

**Question 3**

![image](https://github.com/user-attachments/assets/81c33e3b-0d4e-4cc7-9a2b-b239ef32d097)

```sql
update products
set product_name='Grapefruit'
where product_id=4;
```

**Output:**

![image](https://github.com/user-attachments/assets/7c7a0803-32d1-4d0e-a5c3-6e579f0cd879)

**Question 4**

![image](https://github.com/user-attachments/assets/50f98634-3f16-4350-814e-e2ae1f11c50a)

```sql
UPDATE employees
SET salary=salary*2
WHERE department_id=20
AND job_id LIKE'%MAN';
```

**Output:**

![image](https://github.com/user-attachments/assets/ebb713d1-8c0c-42cc-89df-62b5d36a0a7b)

**Question 5**

![image](https://github.com/user-attachments/assets/7fa066f1-5bff-4268-b5a5-9f860e1704a6)

```sql
update Employees
set SALARY=8000
where EMPLOYEE_ID=105 AND SALARY<5000;
```

**Output:**

![image](https://github.com/user-attachments/assets/4e3232e6-ce3a-414f-8e0c-a032a17f9229)

**Question 6**

![image](https://github.com/user-attachments/assets/5c2f2ca3-163d-400c-bcb6-055c925503e9)

```sql
delete from Customer
where (GRADE>2 AND PAYMENT_AMT<(SELECT AVG(PAYMENT_AMT) FROM CUSTOMER))
OR OUTSTANDING_AMT>8000;
```

**Output:**

![image](https://github.com/user-attachments/assets/6339b72f-25c7-4a35-aab3-fea638712dd8)

**Question 7**

![image](https://github.com/user-attachments/assets/138485af-629d-41cb-bc07-e419d6509b45)

```sql
delete from Customer
where CUST_CITY NOT IN ('New York') and OUTSTANDING_AMT>5000;
```

**Output:**

![image](https://github.com/user-attachments/assets/e7fbfd7f-f0a2-4636-9c90-cdbf3d932087)

**Question 8**

![image](https://github.com/user-attachments/assets/85c57e45-3e29-49aa-9fb0-3445cc39324d)

```sql
delete from customer
where opening_amt BETWEEN 4000 AND 6000;
```

**Output:**

![image](https://github.com/user-attachments/assets/7b3463a0-ebc5-4e2e-a540-9438153e8fd2)

**Question 9**

![image](https://github.com/user-attachments/assets/edc712db-3f4a-4907-b92d-7b217583f2ff)

```sql
DELETE FROM Surgeries
WHERE surgery_id=3 OR surgeon_id=4;
```

**Output:**

![image](https://github.com/user-attachments/assets/ffc6e3f2-bed1-4763-8724-2002d123c9c4)

**Question 10**

![image](https://github.com/user-attachments/assets/00ae118d-2641-485c-aa5f-a8e385176a7a)


```sql
delete from Customer
where WORKING_AREA='New York';
```

**Output:**

![image](https://github.com/user-attachments/assets/ec6369d6-ec48-48cc-892f-819370ec2152)

## RESULT
Thus, the SQL queries to implement DML commands have been executed successfully.
