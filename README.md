# Introduction
Dive into the data job market! This project focuses on analyzing data analyst roles to uncover the most lucrative opportunities, the most in-demand skills, and the optimal intersection between salary and market demand. 

The queries and analysis are specifically tailored to help aspiring Data Analysts navigate the current job landscape efficiently.

# Background
This project was developed as part of the "SQL for Data Analytics" course by Luke Barousse. The primary goal was to take a real-world dataset of job postings and apply advanced SQL techniques to extract actionable insights. 

The questions I wanted to answer through my SQL queries were:
1. What are the top-paying Data Analyst jobs?
2. What skills are required for these top-paying roles?
3. What are the most in-demand skills for Data Analysts?
4. Which skills are associated with the highest average salaries?
5. What are the most optimal skills to learn (high demand AND high paying)?

# Tools I Used
To perform this deep dive into the data job market, I harnessed the power of several key tools:
* **SQL (PostgreSQL):** The core engine of this project. I used it to query the database, filter data, and perform complex joins and aggregations.
* **Visual Studio Code:** My preferred Integrated Development Environment (IDE) for database management and executing SQL scripts.
* **Git & GitHub:** For version control, tracking changes, and sharing my SQL scripts and analysis with the world.

# The Analysis
The core of this project consists of 5 SQL queries that tackle the questions established in the background. Here is a breakdown of the analysis:

### 1. Top Paying Data Analyst Jobs
To identify the highest-paying roles, I filtered the `job_postings_fact` table for remote Data Analyst positions with an available salary. 
* *[See the query here](project_sql/1_top_paying_jobs.sql)*

### 2. Skills for Top Paying Jobs
Building upon the first query, I joined the results with the `skills_dim` and `skills_job_dim` tables to reveal the specific technical requirements for the top 10 highest-paying roles.
* *[See the query here](project_sql/2_top_paying_job_skills.sql)*

### 3. Top Demanded Skills
To find out what employers are looking for the most, I counted the occurrences of each skill in remote Data Analyst job postings.
* *[See the query here](project_sql/3_top_demanded_skills.sql)*

### 4. Top Paying Skills
I calculated the average salary associated with each skill to understand which competencies yield the highest financial return.
* *[See the query here](project_sql/4_top_payings_skills.sql)*

### 5. Optimal Skills
By combining the demand count and the average salary using Common Table Expressions (CTEs), I identified the "sweet spot": skills that are highly sought after by employers and offer great compensation.
* *[See the query here](project_sql/5_optimal_skills.sql)*

# What I Learned
Throughout this project, I significantly leveled up my SQL proficiency. Some of the key technical takeaways include:
* **Advanced Joins:** Mastering the use of `INNER JOIN` and `LEFT JOIN` to seamlessly connect multiple tables (facts and dimensions).
* **Data Aggregation:** Extensive use of functions like `COUNT()`, `AVG()`, and `ROUND()` combined with `GROUP BY` to summarize large datasets.
* **Common Table Expressions (CTEs):** Utilizing the `WITH` clause to break down complex queries into readable, modular, and efficient blocks (specially for the optimal skills analysis).

# Conclusions
This analysis highlights that while core skills are universally demanded, specialized skills often command a premium. By focusing on the "optimal skills" identified in this project, data professionals can strategically guide their learning paths to maximize both their employability and their earning potential in the data field.
