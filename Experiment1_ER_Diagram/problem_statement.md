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

## Scenario Chosen:
University / Hospital (choose one)

## ER Diagram:
![image](https://github.com/user-attachments/assets/95a34c97-34eb-450b-9fc3-214415244855)


## Entities and Attributes:
- Entity	Attributes
-Hospital-> Hospital_ID (PK), Name, Contact, Address, Medical_List
-Doctor-> Doctor_ID (PK), Name, Specialization, Contact, Work_Schedule
-Patient-> Patient_ID (PK), Name, DOB, Gender, Phone, Address
-Medical_Records->Record_ID (PK), Diagnosis, Treatment, Test_Result, Medications
-Billing	->Billing_ID (PK), Date, Amount, Payment_Status, Method
...

## Relationships and Constraints:
- Hospital – Doctor	(A hospital employs many doctors)	1 (Hospital) : M (Doctors)
Hospital – Patient	(A hospital admits many patients)	1 : M
Doctor – Patient	(A doctor treats many patients, and a patient can be treated by many doctors)	M : N
Patient – Medical_Records	(A patient has multiple medical records)	1 : M
Patient – Billing	(A patient receives many bills) 1 : M
Hospital – Billing	(Hospital generates bills)	1 : M
...

## Extension (Prerequisite / Billing):
- Billing Attributes:

billing id (Primary Key)

date

method (e.g., Cash, Card, UPI)

payment status (e.g., Paid, Pending)

total amount

Hospital Attributes:

name

contact

special list

city

Patient (Indirectly related through hospital handling billing)

Relationship: handle
Between: hospital and billing

Meaning: Each hospital handles many billings, and each billing is handled by one hospital.

Cardinality:

One hospital → can handle many billing records (1:M)

Each billing → belongs to one hospital (M:1)

## Design Choices:
In designing the hospital ER diagram, we chose core entities like Patient, Doctor, Hospital, Medical Records, and Billing because they represent the main elements involved in hospital operations. Patients interact with doctors, receive treatment, and have medical records created, while hospitals manage these interactions and handle billing. Relationships such as "meets" between doctors and patients (many-to-many) allow tracking of consultations, and "admission" links patients to hospitals. The "has assigned" relationship connects hospitals and doctors, showing where each doctor works. We included Billing as a separate entity to track payment details, assuming each billing entry is handled by one hospital. These choices ensure the ER model clearly captures the flow of healthcare services and financial operations within a hospital, with attributes like diagnoses, treatments, and payment status fully detailed.

## RESULT
Hence,the concepts of ER diagram is understood and applied by creating an ER diagram for a real world application. 
