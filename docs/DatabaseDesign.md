# Database Design

# PLANWISE
AI-Powered Study Planner

Version: 1.0

---

# 1. Overview

PLANWISE uses a relational database (MySQL) to store user information, study plans, subjects, exams, AI-generated schedules, and progress analytics.

The database is designed to be scalable, secure, and efficient.

---

# 2. Database Tables

## Users

Purpose:
Stores user account information.

Fields:

- user_id (Primary Key)
- full_name
- email
- password
- created_at

---

## Subjects

Purpose:
Stores subjects created by each user.

Fields:

- subject_id (Primary Key)
- user_id (Foreign Key)
- subject_name
- difficulty_level
- color

---

## Exams

Purpose:
Stores exam information.

Fields:

- exam_id (Primary Key)
- subject_id (Foreign Key)
- exam_name
- exam_date
- priority

---

## Study Plans

Purpose:
Stores AI-generated study plans.

Fields:

- plan_id (Primary Key)
- user_id (Foreign Key)
- date
- start_time
- end_time
- task
- completed

---

## Progress

Purpose:
Tracks completed study sessions.

Fields:

- progress_id (Primary Key)
- user_id (Foreign Key)
- subject_id (Foreign Key)
- study_hours
- completion_percentage
- streak

---

## AI Recommendations

Purpose:
Stores AI-generated recommendations.

Fields:

- recommendation_id (Primary Key)
- user_id (Foreign Key)
- recommendation_type
- recommendation_text
- created_at

---

# 3. Relationships

One User
→ can have many Subjects

One Subject
→ can have many Exams

One User
→ can have many Study Plans

One User
→ can have many Progress records

One User
→ can receive many AI Recommendations

---

# 4. Primary Keys

Users
- user_id

Subjects
- subject_id

Exams
- exam_id

Study Plans
- plan_id

Progress
- progress_id

AI Recommendations
- recommendation_id

---

# 5. Foreign Keys

Subjects.user_id
→ Users.user_id

Exams.subject_id
→ Subjects.subject_id

StudyPlans.user_id
→ Users.user_id

Progress.user_id
→ Users.user_id

Progress.subject_id
→ Subjects.subject_id

AIRecommendations.user_id
→ Users.user_id

---

# 6. Future Tables

Future versions may include:

- Flashcards
- Notes
- Friends
- Study Groups
- Notifications
- Achievements
- Leaderboards
- Chat History

---

# 7. Conclusion

The database structure is designed to minimize redundancy while maintaining efficient relationships between users, subjects, exams, study plans, and AI-generated recommendations.

This design provides a strong foundation for future scalability and feature expansion.
