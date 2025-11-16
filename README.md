Anonymous Grading Platform

This project is for Web Technologies assignment, for the EasyDevs Team(Busca Edoardo, Andrei Stefan). The goal is to build a simple web app where students can upload their project, and other randomly selected students can grade it anonymously. The professor can see the final results but not the identity of the graders.

Project Description

The application will include:

a Node.js backend with a REST API

a React frontend (SPA)

a PostgreSQL database accessed through an ORM

two roles: student and professor

Students can add projects and deliverables. Some students will be randomly selected as jury members and can give a grade from 1 to 10. Grades are anonymous, and the final grade removes the lowest and highest values.

Basic Features

register and login

add projects and deliverables

random jury assignment

anonymous grading

professor can see final results

Database (simple model)

Users: id, name, email, password, role
Projects: id, title, description, ownerId
Deliverables: id, projectId, name, videoLink
JuryAssignments: id, projectId, userId
Grades: id, juryAssignmentId, grade

API (short version)

Auth:
POST /auth/register
POST /auth/login

Projects:
POST /projects
GET /projects/:id

Deliverables:
POST /projects/:id/deliverables

Grades:
POST /grades/:assignmentId
PUT /grades/:assignmentId

Professor:
GET /admin/projects
