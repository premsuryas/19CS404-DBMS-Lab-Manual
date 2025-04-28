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

# ER Diagram Submission - Student Name
```
S.PREM KUMAR
212223240125

```

## Scenario Chosen:
UNIVERSITY DATABASE

## ER Diagram:
![ER Diagram](![Screenshot 2025-04-28 135512](https://github.com/user-attachments/assets/6951b05f-ec7a-4cd7-a3ad-d4d78a693745)
)

## Entities and Attributes:
```
department-id,name
faculty-name,id,emai,phone no
course-credit,id,name,program id
entrollment-id,enrollmentdate,studentid,courseid
student-phone no,email,date of birth,programid,id,name
pre request-course id ,prereq course id
program-id,name,dept id

```
## Relationships and Constraints:
```
department-program(one-to-many)
program-course(one-to-many)
program-student(one-to-many)
course-enrollment(one-to-many)
student-enrollment(one-to-many)
instructor-course(one-to-many)
course-prerequisite(one-to-many)

```
## Extension (Prerequisite / Billing):
prerequisite- student have must to be id,date of birth.
## Design Choices:
Students are billed per semester, typically based on the number of credit hours.

A course can have multiple prerequisites, and a prerequisite can apply to multiple courses.

Payments can be made in installments, so billing and payment are separated for flexibility.

Each course belongs to one department, simplifying academic administration.

Prerequisite enforcement is logical (not procedural)—ensured via validation in software, not the database alone

## RESULT:
The university database was created sucessfully.
