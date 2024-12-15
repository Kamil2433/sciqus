
Backend Deployed Link/testroutes- https://sciqus.onrender.com

Here’s a concise summary of the project and APIs in bullet points:
Project Overview: A student Course management system with APIs for managing users, students, and courses using SQLite as the database and Node.js as backend.
Key Features:
User Registration and Login: Users can register and log in with JWT authentication. On login, a JWT token is generated for session management.
JWT Authentication: Ensures secure communication between the client and server, allowing users to access protected routes only with a valid token.
Role-based Access: Admin users have elevated privileges to perform actions like adding, updating, or deleting students and courses.
Student Management: APIs to add, update, and view students, ensuring they are associated with valid courses.
Course Management: Admins can add and update courses, ensuring they are linked to students.
Data Validation: Ensures that only valid data is entered into the system, such as checking if a course exists before adding a student to it.
Error Handling: Proper error responses for invalid operations, such as non-existent users, courses, or unauthorized access.
Important Points:
JWT Authentication: Used for secure API access and session management.
Role-based Access Control (RBAC): Only admin users can perform sensitive operations like adding or updating students and courses.
Database: SQLite is used to store users, courses, and students.
Middleware: Ensures authentication and role validation before allowing access to protected routes.

Testing routes- 

1.  POST  https://sciqus.onrender.com/api/auth/reg - to register new user
2.  GET https://sciqus.onrender.com/api/auth/   -      to login new user, return an JWT token
3. POST https://sciqus.onrender.com/api/student/add-student  - Adds a new student with the specified course, but only if the user is an admin.
4. GET https://sciqus.onrender.com/api/student/students   -  Retrieves a list of all students
5. GET https://sciqus.onrender.com/api/student/students/course/:course_id - Updates the details of a student
6. DELETE https://sciqus.onrender.com/api/student/delete-student/:student_id - Deletes a student from the database.
7. POST https://sciqus.onrender.com/api/course/add-course  - Adds a new course to the system. Only accessible by admin users
– Screenshot of API- PTO
Screen shots of API testing user Thunderclient-
1. Api to add students to the db
   

<img width="689" alt="Screenshot 2024-12-15 213255" src="https://github.com/user-attachments/assets/e2736f34-1df7-4989-a294-8ca88e11a524" />




2. API for get list of students
<img width="675" alt="Screenshot 2024-12-15 213746" src="https://github.com/user-attachments/assets/00a0ecb8-a027-4d3d-ad29-450e8097ecb3" />




3. API to get all students form a course

<img width="697" alt="Screenshot 2024-12-15 213839" src="https://github.com/user-attachments/assets/1634141a-cd29-495e-9e3b-bb8de0927d78" />



4. API to delete the student from an course





<img width="711" alt="Screenshot 2024-12-15 214101" src="https://github.com/user-attachments/assets/01a6f6f6-c737-451f-bd52-b7bf5fe25f93" />





5. API to delete student- 

<img width="717" alt="Screenshot 2024-12-15 214207" src="https://github.com/user-attachments/assets/05068962-c20e-4766-b8c4-2480d3ba5146" />


6. JWT middleware(used to authenticate users- 

<img width="607" alt="Screenshot 2024-12-15 220932" src="https://github.com/user-attachments/assets/2a330d38-edab-4acb-816d-59d00f8f7d88" />

