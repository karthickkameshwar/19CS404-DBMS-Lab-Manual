# Experiment 1: Entity-Relationship (ER) Diagram
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
   - Cardinality: Many-to-many (a login can enroll in multiple courses, and a course can have multiple logins).
   - Participation: Partial (not every login must enroll in a course, and vice versa).

3. Courses - College (Has)
   - Cardinality: Many-to-one (many courses belong to one college).
   - Participation: Total (every course must belong to a college).

4. College - ERP (Has)
   - Cardinality: One-to-one (each college has one ERP).
   - Participation: Total (every college is linked to an ERP).
...

## Extension (Prerequisite / Billing):
   - Each course may have implicit prerequisites defined in its metadata (not shown explicitly in this diagram).
   
   - Students enrolling in courses assume they meet any prerequisites set by the college or department.

## Design Choices:
- Entities:
The chosen entities (Student, Login, Courses, College, ERP) reflect core components of a university system, ensuring all essential information is captured.
- Attributes:
Attributes are selected to uniquely identify and describe each entity. Composite attributes like Name and Staff allow for grouping related details.
- Relationships:
Relationships are designed to mirror real-world associations: students have logins, logins enroll in courses, courses belong to colleges, and colleges use ERP systems.
- Assumptions:
   Each student has exactly one login.
   A login is required to enroll in courses.
   Courses are always associated with a college.
   ERP is unique per college.
   Staff is modeled as a composite attribute within Courses for simplicity.
  
## RESULT
  The ER diagram models a university system where each student has personal details and a unique login, can enroll in multiple courses (each managed by staff), and is associated with a college that uses an ERP system. Key relationships include students having logins, logins enrolling in courses, courses belonging to colleges, and colleges using ERP. The design captures essential academic and administrative data flow within a university.

