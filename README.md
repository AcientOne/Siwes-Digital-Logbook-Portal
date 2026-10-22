# SIWES Management & Digital Logbook Portal

**Course:** Csc 317 System Analysis & Design 
**Project Overview:**  
A digital portal designed to streamline the Student Industrial Work Experience Scheme (SIWES) process. It allows students to log daily activities electronically, enables industry supervisors to review and approve logs, and provides academic supervisors with remote progress tracking and evaluation tools.

---

## 👥 User Roles & Key Features

1. **Student**
   * Register SIWES placement (PPA) details and company acceptance.
   * Fill out daily activities and weekly summary logs.
   * Track logbook verification status.

2. **Industry Supervisor**
   * Review weekly student logbook submissions.
   * Add comments and approve/reject weekly entries.
   * Fill out student performance evaluation forms.

3. **Academic Supervisor**
   * Monitor student logbook progress remotely.
   * Grade final SIWES reports and defense results.

4. **Administrator**
   * Manage user accounts and assign academic supervisors to departments/students.

---

## 📋 System Requirements Specification

### Functional Requirements
* **FR-1:** Role-based access control and secure authentication for all user types.
* **FR-2:** Student placement record management (PPA location, supervisor contact info).
* **FR-3:** Weekly log submission with draft, submitted, and approved states.
* **FR-4:** Digital verification and feedback workflow for supervisors.

### Non-Functional Requirements
* **Security:** Enforced password hashing and encrypted authentication sessions.
* **Usability:** Mobile-responsive design allowing students to enter logs on smartphone browsers.
* **Reliability:** Data persistence ensuring submitted logs are safely stored for academic audit.

---

## 🗄️ Database Entity-Relationship (ERD) Overview

The database model consists of four core entities:
* **Users:** `user_id`, `full_name`, `email`, `password_hash`, `role`
* **StudentProfiles:** `student_id`, `matric_number`, `department`, `academic_supervisor_id`
* **Placements:** `placement_id`, `company_name`, `company_address`, `start_date`, `end_date`
* **LogbookEntries:** `entry_id`, `week_number`, `monday_activity`, `tuesday_activity`, `wednesday_activity`, `thursday_activity`, `friday_activity`, `status`, `supervisor_comment`
