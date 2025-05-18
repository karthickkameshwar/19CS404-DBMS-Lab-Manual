# Experiment 1: Entity-Relationship (ER) Diagram
- Courses have number, name, credits.
- Track course enrollments by students and enrollment date.
- Add support for prerequisites (some courses require others).

---

### 🔹 Scenario 2: Hospital Database
Design a database for patient management, appointments, medical records, and billing.

**User Requirements:**
- Patient details including contact and insurance.
- Doctors and their departments, contact info, specialization.
- Appointments with reason, time, patient-doctor link.
- Medical records with treatments, diagnosis, test results.
- Billing and payment details for each appointment.

---

## 📝 Tasks:
1. Identify entities, relationships, and attributes.
2. Draw the ER diagram using any tool (draw.io, dbdiagram.io, hand-drawn and scanned).
3. Include:
   - Cardinality & participation constraints
   - Prerequisites for University OR Billing for Hospital
4. Explain:
   - Why you chose the entities and relationships.
   - How you modeled prerequisites or billing.

# ER Diagram Submission - Oviya K P

## Scenario Chosen:
University
The ER diagram models a university’s information system, focusing on students, their login credentials, course enrollments, college details, and ERP (Enterprise Resource Planning) integration.

## ER Diagram:
![image](https://github.com/user-attachments/assets/efdd6f06-05df-48a8-95ab-ba6e94e8dc6e)


## Entities and Attributes:
1. Student
Attributes:
   - First Name, Last Name: Basic personal identification.
   - (Name): Composite attribute combining First and Last Name.
   - Age: Optional (dashed line), possibly derived from Date of Birth.
   - Date of Birth: For age calculation and identification.
   - Address: Student’s residential information
   - Email: For communication and login.
   - Phone: Contact number.

2. Login
Attributes:
   - Register Number: Unique identifier for login.
   - Email ID: Used for login and communication.
   - Password: For authentication.
       
3. Courses
Attributes:
   - Course Name: Name of the course.
   - Course Code: Unique code for each course.
   - Department: Department offering the course.
   - (Staff): Composite attribute for staff details:
   - Phone: Staff contact.
   - Faculty Name: Name of the instructor.
   - Teacher ID: Unique staff identifier.

4. College
Attributes:
   - College Name: Name of the college.
   - College Code: Unique college identifier.

5. ERP
No explicit attributes shown, represents the university’s ERP system.
...

## Relationships and Constraints:
1. Student - Login (Has)
   - Cardinality: One-to-one (each student has one login).
   - Participation: Total (every student must have a login).

2. Login - Courses (Enroll)
