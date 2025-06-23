# 📚 Skill-Swap E-learning Platform - SQL Schema Design (Task 1)

## 📌 Task Objective

This task is part of the SQL Developer Internship. The goal is to design a database schema for an **E-learning platform called Skill-Swap**, where users can **learn and teach skills**, **create or enroll in courses**, and manage **payments, lectures, and profiles**.

---

## 🛠 Tools Used

- ✅ MySQL Workbench – to create and run SQL queries
- ✅ MYSQL Workbench – to draw the ER diagram
- ✅ GitHub – to upload and submit the task

---

## 🧠 Key Concepts Used

- DDL (Data Definition Language)
- Primary Key and Foreign Key
- Entity Relationship Diagram (ERD)
- Normalization
- AUTO_INCREMENT
- Composite Key
- One-to-Many & Many-to-Many Relationships

---

## 🗂 Database Tables Overview

| Table Name      | Purpose |
|------------------|---------|
| `Users`          | All users (learners, educators, admins) |
| `Skills`         | List of skills (e.g., Python, Singing) |
| `UserSkills`     | Mapping of users to skills (want to learn/teach) |
| `Courses`        | Courses created by educators |
| `Lectures`       | Videos or materials inside each course |
| `Enrollments`    | Tracks which student enrolled in which course |
| `Payments`       | Stores course payment details |
| `Admins`         | Special user type with super access |

---
![Screenshot 2025-06-23 145354](https://github.com/user-attachments/assets/39c95c44-e0c0-48d7-8461-eed0e6500446)
![ER_Diagram_Task01](https://github.com/user-attachments/assets/c6123975-8aeb-49e1-80ea-3a741e2574d5)


## 📑 SQL Script

You can find the SQL script in the file:  
📄 `skill_swap_schema_Task01.sql`

It contains code to create all the tables with proper keys and constraints.

### ✅ Sample Code from the Script

```sql
CREATE TABLE Users (
    user_id INT AUTO_INCREMENT PRIMARY KEY,
    name VARCHAR(100),
    email VARCHAR(100) UNIQUE,
    password VARCHAR(255),
    role ENUM('learner', 'educator', 'admin') DEFAULT 'learner',
    registered_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP
);


📊 ER Diagram
This diagram shows how all tables are connected (relationships).
➡️ Primary keys, foreign keys, and table names are clearly marked.

📷 Screenshot of ER Diagram
![ER_Diagram_Task01](https://github.com/user-attachments/assets/2b62ec44-2ce5-41d4-9dd2-858b25c8b589)



📁 Folder Structure
skill-swap-db-schema_Task01/
├── Skill_Swap_Schema_Task01.sql      # SQL DDL code
├── ER_Diagram.png             # Screenshot of ER diagram
└── README.md                  # This file
💡 How to Run This Project
✅ Follow these steps to try this on your computer.

Step 1: Install MySQL Workbench (or use any SQL tool)
Link: https://dev.mysql.com/downloads/workbench/

Step 2: Run the SQL Code
Open MySQL Workbench

Copy code from Skill_Swap_Schema_Task01.sql

Run it to create the database and all tables

Step 3: View the Tables
Expand the database in your SQL tool to check all tables are created.

📤 GitHub Submission Steps
Create a new public repo on GitHub named Skill_Swap_Schema_Task01.sql

Upload:

Skill_Swap_Schema_Task01.sql

ER_Diagram_Task01.png

README.md

Copy the repository link.

🤝 Contribution
Designed and submitted by:
👤 Alok Kumar
📧 alokkumarkaranraj@gmail.com
