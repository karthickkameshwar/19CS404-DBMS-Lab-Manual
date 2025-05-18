# Experiment 2: DDL Commands
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
