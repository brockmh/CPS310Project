# System Analysis Document

## 1. Introduction

### A. Purpose
The purpose of this project is to analyze and define the system requirements for an improved University of Dayton System. This system aims to show student and faculty interactions, including applying to the university, scheduling for classes, withdrawing from class, accessing your transcript, final class grade submission, changing your major, withdrawing from school, and graduation processing. By addressing all of the inefficiencies in the existing processes, this system will enhance usability, accuracy, and accessibility for all users. The purpose of this document is to provide a detailed analysis of the system being developed to improve university administrative processes. 


### B. Scope
**This document outlines the functional and non-functional requirements of the University Administrative System, including:**
  
1. Student application submission and tracking
2. Course scheduling and enrollment management
3. Final Grade submission
4. transcript viewing
5. Major change requests and processing
6. Graduation eligibility verification and approvals 
7. Withdrawing from class


This analysis examines the core components of the University Administrative System, focusing on their interactions with students, faculty, and administrative staff. It will exclude implementation details and the integration services outside the university of Dayton’s existing infrastructure. This document provides an overview of the system, detailed functionalities, user interaction flows, system constraints, and underlying assumptions.


### C. Definitions & Acronyms

- DFD - Data Flow Diagram - A visual representation of how data moves through a system
- ERD - Entity Relationship Diagram - A visual model that shows how entities relate to each other
- Use Case - A description of system behavior under specific conditions 
- UD - University of Dayton - The University of Dayton is a private, Catholic research university in Dayton, Ohio, United States. Founded in 1850 by the Society of Mary


### D. References
- CPS 310 Course Materials
- University of Dayton Administrative System Documentation
- Group members as Students

### E. Overview
- This system is designed to make the university system easier to use by handling student applications, class registration, academic records, major changes, transcripts, and graduation. It focuses on four main groups—Students, Registrars, Faculty, and Administration. Using a Data-Flow Diagram, Entity-Relationship Diagram, and a Use-Case Diagram . The goal is to improve efficiency, reduce mistakes, and create a user-friendly system for students, teachers, and administrators. 

---

## 2. Overall Description

### A. Product Perspective
- An overview of the environment that this system must operate within, including other software and hardware systems that will interface with this system.

### B. Product Functions
- An overview of the features to be provided by the software.

### C. User Characteristics
1. Student (StudentID, Name, DateOfBirth, Major)
2. Registrar (RegistrarID, Name, Role,)
3. Faculty (FacultyID, Name, Department)
4. Administration (AdminID, Name, Position)

### D. Constraints
- Any constraints that have been placed on the project (that are not, in themselves, requirements).

### E. Assumptions
- One assumption we are going by is that within this phase there are no errors when using the system and it runs perfectly. This will chnage as we dive deeper into each diagram during the other phases, where we will have to account for these errors and how they will be addressed. 

---

## 3. Systems Analysis

### A. Context Level Data Flow Diagram

![DFD drawio (1)](https://github.com/user-attachments/assets/38aabe71-4d8f-427b-b843-465b02097d8c)


### B. Context Level Entity Relationship Diagram

![Entity drawio](https://github.com/user-attachments/assets/bdaafce3-c6b0-4095-a4bd-5c8d231b4055)


### C. Use Cases
#### i. Scenarios
#### ii. Diagram(s)
