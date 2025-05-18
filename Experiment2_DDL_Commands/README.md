# Experiment 2: DDL Commands

## AIM
To study and implement DDL commands and different types of constraints.

## THEORY

### 1. CREATE
Used to create a new relation (table).

**Syntax:**
```sql
CREATE TABLE (
  field_1 data_type(size),
  field_2 data_type(size),
  ...
);
```
### 2. ALTER
Used to add, modify, drop, or rename fields in an existing relation.
(a) ADD
```sql
ALTER TABLE std ADD (Address CHAR(10));
```
(b) MODIFY
```sql
ALTER TABLE relation_name MODIFY (field_1 new_data_type(size));
```
(c) DROP
```sql
ALTER TABLE relation_name DROP COLUMN field_name;
```
(d) RENAME
```sql
ALTER TABLE relation_name RENAME COLUMN old_field_name TO new_field_name;
```
### 3. DROP TABLE
Used to permanently delete the structure and data of a table.
```sql
DROP TABLE relation_name;
```
### 4. RENAME
Used to rename an existing database object.
```sql
RENAME TABLE old_relation_name TO new_relation_name;
```
### CONSTRAINTS
Constraints are used to specify rules for the data in a table. If there is any violation between the constraint and the data action, the action is aborted by the constraint. It can be specified when the table is created (using CREATE TABLE) or after it is created (using ALTER TABLE).
### 1. NOT NULL
When a column is defined as NOT NULL, it becomes mandatory to enter a value in that column.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) NOT NULL
);
```
### 2. UNIQUE
Ensures that values in a column are unique.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) UNIQUE
);
```
### 3. CHECK
Specifies a condition that each row must satisfy.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) CHECK (logical_expression)
);
```
### 4. PRIMARY KEY
Used to uniquely identify each record in a table.
Properties:
Must contain unique values.
Cannot be null.
Should contain minimal fields.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size) PRIMARY KEY
);
```
### 5. FOREIGN KEY
Used to reference the primary key of another table.
Syntax:
```sql
CREATE TABLE Table_Name (
  column_name data_type(size),
  FOREIGN KEY (column_name) REFERENCES other_table(column)
);
```
### 6. DEFAULT
Used to insert a default value into a column if no value is specified.

Syntax:
```sql
CREATE TABLE Table_Name (
  col_name1 data_type,
  col_name2 data_type,
  col_name3 data_type DEFAULT 'default_value'
);
```

**Question 1**

![image](https://github.com/user-attachments/assets/e041cb77-8e29-42a3-99d8-52c64b55d952)

```sql
insert into Employee(EmployeeID,Name,Position,Department,Salary) values (2,'John Smith','Developer','IT',75000),(3,'Anna Bell','Designer','Marketing',68000);
```

**Output:**

![image](https://github.com/user-attachments/assets/8add77e5-974b-48f2-89e7-3551672be64e)

**Question 2**

![image](https://github.com/user-attachments/assets/b9356e2c-0897-41e6-8802-8ae4c8b80319)

```sql
create table Employees(
EmployeeID primary key,
FirstName NOT NULL,
LastName NOT NULL,
Email unique,
Salary not null CHECK(Salary>0),
DepartmentID int,
foreign key(DepartmentID) references Departments(DepartmentID)
);
```

**Output:**

![image](https://github.com/user-attachments/assets/2927987d-ed33-4020-88de-b5c8ee93a7c1)

**Question 3**

![image](https://github.com/user-attachments/assets/40461262-712b-42ce-8b7b-726017b26da8)

```sql
insert into Books(ISBN,Title,Author,Publisher,YearPublished)
SELECT ISBN, Title, Author, Publisher, YearPublished
FROM Out_of_print_books;
```

**Output:**

![image](https://github.com/user-attachments/assets/5a0f9285-3033-4779-943e-039531516c8a)

**Question 4**

![image](https://github.com/user-attachments/assets/effdd734-7925-42a4-84c9-4465e821aff9)

```sql
alter table Companies
RENAME COLUMN name TO VARCHAR(50);
alter table Companies
ADD column DOB Date;
```

**Output:**

![image](https://github.com/user-attachments/assets/92d5d045-c231-4403-a521-c59f5d5302b3)

**Question 5**

![image](https://github.com/user-attachments/assets/51283f69-4b35-49b5-a755-73b65fc2014f)

```sql
create table Products(
ProductID primary key,
ProductName NOT NULL,
Price real check(Price>0),
Stock int check(Stock>=0)
);
```

**Output:**

![image](https://github.com/user-attachments/assets/298e415b-33a5-45e0-a9bc-707694579e46)

**Question 6**

![image](https://github.com/user-attachments/assets/6f691f89-d8de-4a5b-98e9-291534cc8dc5)

```sql
ALTER TABLE Student_details
Add column Country TEXT;
```

**Output:**

![image](https://github.com/user-attachments/assets/16aa727e-6bc4-4a1c-86f2-58a0c0f30d98)

**Question 7**

![image](https://github.com/user-attachments/assets/bbdf2a4b-4bf8-416c-986f-eca166026450)

```sql
create table ProjectAssignments(
AssignmentID INTEGER primary key,
EmployeeID INTEGER,
ProjectID INTEGER,
AssignmentDate DATE NOT NULL,
foreign key(EmployeeID)references Employees(EmployeeID),
foreign key(ProjectID)references Projects(ProjectID)
);
```

**Output:**

![image](https://github.com/user-attachments/assets/d6f1fc5c-f061-4539-991b-9523a74fd219)

**Question 8**

![image](https://github.com/user-attachments/assets/405f7767-e115-4c61-9424-e3ba0acd99bc)

```sql
create table Tasks(
TaskID INTEGER,
TaskName TEXT,
DueDate DATE
);
```

**Output:**

![image](https://github.com/user-attachments/assets/0137f4f3-3e2a-4fb6-b011-735abe10642e)

**Question 9**

![image](https://github.com/user-attachments/assets/a72e8aa6-dc9f-4537-9577-79e16d0a8fae)

```sql
insert into Books(ISBN,Title,Author,Publisher,Year) values ('978-1234567890','Data Science Essentials','Jane Doe','TechBooks',2024);
```

**Output:**

![image](https://github.com/user-attachments/assets/f557b942-4863-43c4-9bd9-e8d39f2edfd8)

**Question 10**

![image](https://github.com/user-attachments/assets/6e68dffe-111b-4a6f-bd89-354955a95bde)

```sql
create table Attendance(
AttendanceID INTEGER primary key,
EmployeeID INTEGER,
AttendanceDate DATE NOT NULL,
Status TEXT CHECK(STATUS IN('Present','Absent','Leave')),
foreign key(EmployeeID)references Employees(EmployeeID)
);
```

**Output:**

![image](https://github.com/user-attachments/assets/1c807311-9fa3-4dae-8267-9d65c408c13e)

## RESULT
Thus, the SQL queries to implement different types of constraints and DDL commands have been executed successfully.
