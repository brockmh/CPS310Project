# Phase 1 Feedback and Fixes
- Use 0 to identify the system in DFD.  Some entities in the entity relationship diagram are actually actions, not the required people, places, or things.  Use case scenarios are incomplete.  Every bubble/use case in the diagram requires a scenario.
  
## DFD Fix
 ![DFD drawio](https://github.com/user-attachments/assets/95113424-b6cc-43a0-8747-f1d54f527f53)

## Entity Relationship Diagram Fix
![Entity drawio](https://github.com/user-attachments/assets/0f54143d-eb8f-4d0b-949b-41aa7823a0f4)

## Use Case Scenario Fix
Student Course Enrollment <br> 
Actors: Student, System  <br>

Steps:  
1. Student logs into the system.
2. The system displays available courses.
3. The student selects a course and enrolls.
4. The system updates the student’s academic schedule.
5. The student receives a confirmation notification.

Final Grade Submission (Faculty)<br>
Actors: Faculty, System <br>

Steps:
1. Faculty logs into the system.
2. The system displays the courses they are teaching.
3. Faculty selects a course.
4. Faculty enters final grades for each student.
5. The system stores the grades and submits them for approval.
6. Faculty receives confirmation.

Major Change Request <br>
Actors: Student, Registrar, System <br>

Steps:
1. Student logs into the system.
2. Student navigates to the “Major Change” request section.
3. Student selects a new major and submits the request.
4. The system forwards the request to the registrar.
5. The registrar reviews the request.
6. If approved, the system updates the student’s record.
7. If denied, the student is notified with a reason.

Graduation Processing <br>
Actors: Student, Registrar, Admin, System <br>

Steps:
1. Student applies for graduation through the system.
2. The system checks eligibility requirements.
3. The registrar reviews the application.
4. If requirements are met, the system forwards the application to the admin.
5. Admin grants final approval.
6. The system updates the student’s status and sends a confirmation.

Transcript Viewing & Generation <br>
Actors: Student, Registrar, System <br>

Steps:
1. Student logs into the system.
2. Student navigates to the transcript section.
3. The system retrieves the student’s academic record.
4. The system generates the transcript.
5. Student views/downloads the transcript.

Withdrawing from a Class <br> 
Actors: Student, Registrar, System <br>

Steps:
1. Student logs into the system.
2. Student selects a course to withdraw from.
3. Student provides a reason.
4. The system processes the withdrawal request.
5. The system updates the student’s schedule.
6. The student receives confirmation.








# Phase 2
 1. Brock Hensley
 2. Khagendra Mishra
 3. Tidiane Dia
 4. Gregory Pooler


## Diagram 0

![Diagram0 drawio](https://github.com/user-attachments/assets/96ac605b-2621-40d5-a886-fbdf59963c83)

This Level 0 Data Flow Diagram (DFD) shows how student records are managed in the university. It illustrates how students apply for courses, request transcripts, change majors, withdraw from classes, and apply for graduation. The registrar processes applications, verifies enrollments, and updates records, while faculty submit grades that update transcripts. Administration handles graduation approvals. Different processes connect to data stores that keep track of student records, course enrollments, and graduation requests. 

## Child Diagram

![Child drawio](https://github.com/user-attachments/assets/6ebc904d-d403-460f-b904-f957934e60b9)

The child diagram breaks down the course registration process in the university, detailing how student enrollment is handled step by step. First, the system verifies a student’s eligibility by checking prerequisites in the prerequisites database. If eligible, course availability is checked before proceeding with registration. The enrollment database stores current enrollment data and processes registration details. Once registration is completed, the system generates an enrollment confirmation, updating student records and notifying the student. This breakdown ensures that students can only enroll in courses they qualify for while maintaining accurate academic records.

## Data Dictionary

Data Flow Descriptions

<img width="622" alt="Screenshot 2025-03-18 at 6 09 47 PM" src="https://github.com/user-attachments/assets/e893269d-1fcf-4a42-b559-788c076c1507" />

Data Store Descriptions

<img width="604" alt="Screenshot 2025-03-18 at 6 10 13 PM" src="https://github.com/user-attachments/assets/df404d20-1023-4423-bea4-90dc05227da9" />

Data Element Descriptions

<img width="549" alt="Screenshot 2025-03-18 at 6 15 51 PM" src="https://github.com/user-attachments/assets/e5e94d71-4ad6-47b7-bc83-432f72b2add1" />

## Process Specifications

Process
1. Application Submission 
- Trigger: Student submits an application
- Validation: Check if all required fields are complete 
- Processing: If complete, process the application; otherwise, return for correction
- Output: Student Application Data stored in Student Records (DS1)

2. Course Enrollment
- Trigger: Student enrolls in a course
- Validation: Ensure the course is available and the student meets prerequisites
- Processing: If valid, update Enrollment Database (DS3)
- Output: Course Enrollment Data stored in Enrollment DB

3. Grade Submission 
- Trigger: Faculty submits final grades
- Validation: Verify grades meet academic standards and are approved by the registrar
- Processing: If verified, update Grade Data
- Output: Grade data stored in Student Records (DS1)

4. Transcript Request
- Trigger: Student requests a transcript 
- Validation: Verify student identity and eligibility 
- Processing: If verified, generate and provide the transcript
- Output: Transcript Data retrieved from Student Records (DS1)

5. Graduation Request
- Trigger: Student applies for graduation
- Validation: Ensure all required credits are completed
- Processing: If approved, update Graduation Request Data
- Output: Graduation Status updated in Graduation Requests (DS4)

Structured Decision

1. Application Submission Decision
- IF application is complete → Process application.
- ELSE → Return for correction.

2. Course Enrollment Decision
- IF course has availability AND student meets prerequisites → Enroll student.
- ELSE → Reject enrollment.

3. Grade Submission Decision
- IF grades are verified by the registrar → Update student record.
- ELSE → Request faculty review.

4. Transcript Request Decision
- IF student identity is verified → Generate transcript.
- ELSE → Reject request.

5. Graduation Request Decision
- IF all requirements are met AND administrator approves → Update graduation status.
- ELSE → Notify student of deficiencies.

  
