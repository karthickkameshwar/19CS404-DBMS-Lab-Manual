# Experiment 1: Entity-Relationship (ER) Diagram
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

# ER Diagram Submission - Student Name

## Scenario Chosen:
University / Hospital (choose one)

## ER Diagram:
![Screenshot (69)](https://github.com/user-attachments/assets/087ed14f-fc84-434f-823e-174b3ec856e8)

## Entities and Attributes:
University - Attributes: University code (Primary Key), Name

Student- Attributes: Student Name, Student ID (Primary Key)

Courses - Attributes: Course Name, Course code (Primary Key), Pre-requisite

Professor - Attributes: Professor ID (Primary Key), Professor Name, Experience

## Relationships and Constraints:
1. books (Between University and Student)
   
   Cardinality: One university can have many students (1:N)

   Participation: Total participation of Student (Every student belongs to a university)

3. assigned (Between Student and Courses)
   
   Cardinality: Many students can be assigned many courses (M:N)

   Participation: Partial

5. delivers (Between Professor and Courses)
   
   Cardinality: One professor can deliver many courses, but each course is delivered by one professor (1:N)

   Participation: Total participation of Courses

## Extension (Prerequisite / Billing):
Pre-requisite is modeled as an attribute in the Courses entity.

It stores information about a prerequisite course required to take that course.

Assumption: It is a self-referencing attribute (course code of the prerequisite).

## Design Choices:
Entities like University, Student, Courses, and Professor were chosen based on key real-world components in an academic system.
Relationships like books, assigned, and delivers were used to capture meaningful associations.
Pre-requisite is modeled as an attribute instead of a separate relationship for simplicity and clarity.
Assumption: A course can have at most one prerequisite; recursive relationships are simplified to attributes.

## RESULT
The ER model represents a simple academic system where:
1. A university books students.
2. Students are assigned to courses.
3. Professors deliver those courses.
4. Each course may have a pre-requisite.
