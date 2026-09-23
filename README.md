# lms-agile-project-portfolio
Portfolio overview of a Django-based Learning Management System, Agile team project (FIT2101)
# Learning Management System — Agile Team Project

A full-featured Learning Management System with role-based access (Admin/Instructor/Student), built with a Django backend across a 3-sprint Agile cycle.

## Overview

Contributed as Product Owner and backend developer to a 7-person team project simulating a real client engagement. The system supports course and lesson management with prerequisite chains, a credit-based progress system, classroom scheduling with capacity limits, and role-specific dashboards for admins, instructors, and students.

> **Note:** This project was completed as assessed team coursework at Monash University Malaysia. The original source code and assessment submission are kept private in accordance with university assessment requirements and respect for teammates' contributions. This repository provides a public overview of my individual role and contributions for internship and portfolio purposes.

---

## System Overview

*(diagram: role-based flow — Admin / Instructor / Student — into Courses, Lessons, Classrooms, Reports)*

The platform models courses (with a draft/publish workflow), lessons (with self-referential prerequisite chains and ordering), learning materials (PDF/video/link), a credit-transaction system tracking student progress per lesson, and classrooms with weekly scheduling and enrollment capacity limits.

---

## What I Did

### Product Ownership
- Owned end-to-end product backlog prioritization across a 3-sprint Agile delivery cycle
- Translated client and stakeholder needs into actionable user stories
- Facilitated sprint planning and sprint review sessions, formally accepting completed work each sprint

### Backend Development — Instructor Reporting & Student Profiles
Built the instructor-facing reporting module in Django, including:
- An instructor report dashboard aggregating student progress across all of an instructor's courses, computing per-student and course-wide progress percentages from the credit-transaction system
- A detailed per-student, per-course report view combining enrolled classroom schedules, completed-lesson history, and credit totals into a single page
- A student list view and individual student profile view scoped to an instructor's own courses
- Role-based access control throughout (an instructor can only view their own courses' data; a student can only view their own report)

---

## Technology Stack

`Django` · `Python` · `HTML/CSS/JS` · `Agile/Scrum` · `Git`

---

## Skills Demonstrated

- Django (models, views, URL routing, ORM query optimization with `select_related`/`prefetch_related`)
- Role-based access control
- Data aggregation across related models
- Agile/Scrum methodology, sprint planning, backlog management
- Stakeholder communication
- Git-based team collaboration

---

## Key Takeaways

Balancing the Product Owner role with hands-on backend work meant constantly switching between stakeholder-facing prioritization decisions and technical implementation details. Building the reporting views also reinforced how much of "backend work" in a data-heavy feature is really about query design — the reporting pages needed data pulled from four related models (courses, enrollments, lessons, credit transactions) without the queries ballooning into dozens of round trips to the database.
