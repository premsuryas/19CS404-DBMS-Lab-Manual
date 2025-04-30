# Experiment 1: Entity-Relationship (ER) Diagram

## 🎯 Objective:
To understand and apply the concepts of ER modeling by creating an ER diagram for a real-world application.

## 📚 Purpose:
The purpose of this workshop is to gain hands-on experience in designing ER diagrams that visually represent the structure of a database including entities, relationships, attributes, and constraints.

---

## 🧪 Choose One Scenario:

### 🔹 Scenario 1: University Database
Design a database to manage students, instructors, programs, courses, and student enrollments. Include prerequisites for courses.

**User Requirements:**
- Academic programs grouped under departments.
- Students have admission number, name, DOB, contact info.
- Instructors with staff number, contact info, etc.
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

# ER Diagram Submission - Student 
## Name:S.PREM KUMAR
## Reg.no:21223240125

## Scenario Chosen:
University 

## ER Diagram:
![image](https://github.com/user-attachments/assets/8074880e-e8f8-4a4c-af85-967e800240f2)


## Entities and Attributes:
### Student:
Attributes: StudentID, FirstName, LastName, DateOfBirth, Email, PhoneNumber, EnrollmentDate, DepartmentID
### Faculty:
Attributes: FacultyID, FirstName, LastName, Email, PhoneNumber, HireDate, DepartmentID
### Department:
Attributes: DepartmentID, DepartmentName, Location
### Course:
Attributes: CourseID, CourseName, CourseCode, Credits, DepartmentID
### Enrollment:
Attributes: EnrollmentID, StudentID, CourseID, EnrollmentDate, Grade
### Class:
Attributes: ClassID, CourseID, FacultyID, Semester, Year, Schedule
### Advising:
Attributes: AdvisingID, StudentID, FacultyID, AdvisingDate
## Relationships and Constraints:
### Student–Advising–Faculty
Relationship: Advises
Cardinality: Many-to-Many (each student can have multiple advisors, each faculty can advise multiple students)
Participation: Total on Advising
### Student–Enrollment–Course:
Relationship: Enrolled in
Cardinality: Many-to-Many
Participation: Total on Enrollment
### Course–Class–Faculty:
Relationship: Teaches
Cardinality: Many-to-Many (each course can be taught in multiple classes, each faculty can teach multiple classes)
### Course–Department:
Relationship: Offered by
Cardinality: Many-to-One (Each course belongs to one department)
### Student–Department:
Relationship: Belongs to
Cardinality: Many-to-One
### Faculty–Department:
Relationship: Belongs to
Cardinality: Many-to-One
### Class–Course:
Relationship: Includes
Cardinality: Many-to-One
### Enrollment–Class:
Relationship: Taught by
Not standard; assumes indirect mapping via faculty
## Extension (Prerequisite / Billing):
### Prerequisite Modeling:
Could be modeled with a recursive relationship on Course:
Relationship: Requires
Cardinality: Many-to-Many (a course can have many prerequisites and be a prerequisite for many others)
## Design Choices:
Use of separate entities for Advising, Enrollment, and Class helps normalize many-to-many relationships and maintain relational integrity.
Department as a central entity provides a logical way to group students, faculty, and courses.

Class entity includes scheduling details, separating course content from the time/location of delivery.

The design is modular and supports easy extension for future requirements like prerequisites, billing, or attendance.

## RESULT
Thus, the Entity-Relationship (ER) Diagram have been created successfully.
