# Introduction
 My  project focuses on an in-depth analysis of data job postings and corresponding salary trends. This analysis aims to provide valuable insights into the demand for data professionals, the skills most sought after by employers, and the salary expectations across different regions and job roles.

 SQL Queries Check it ouy here: [project_sql_folder](/Project_SQL/)
# Background
This project involves analyzing a dataset comprising various data job postings and their associated salaries and skills. It's born from a desire to pinpont top-paid and in-demand skill.

Data hails from my [SQL course](https://lukebarousse.com/sql).It's packed with insights on job titel, salaries , location , and essential skills.

### The Question I want to answer through my SQL quries were.

1. What are the top-paying job?
2. What skills are required for these top-paying job?
3. What skill are most in demand for data analyst?
4. Which skill are associate with higher salaries?
5. What are the most optimal skill to learn? 
# Tools I Used
- SQL
- PostgreSQL
- Power BI
- Git & GitHub
# The Analyst
- To find the highest-paying roles, I looked at data analyst jobs by average yearly salary and location, focusing on remote positions that you can work from anywhere. This shows the best-paying opportunities in the field.
```sql
SELECT
    job_id,
    job_title,
    job_location,
    job_schedule_type,
    salary_year_avg,
    job_posted_date,
    name as company_name
FROM
    job_postings_fact
LEFT JOIN company_dim ON job_postings_fact.company_id = company_dim.company_id
WHERE
    job_title_short = 'Data Analyst' AND
    job_location = 'Anywhere' AND
    salary_year_avg IS NOT NULL
ORDER BY salary_year_avg desc
LIMIT 10
```
By using this SQL queries we found that.
- **Wide Salary Range**: Top 10 paying data analyst roles span from $184,000 to $650,000,    indicating significant salary potential in the field.
- **Diverse Employers**: Companies like SmartAsset, Meta, and AT&T are among those offering high salaries, showing a broad interest across different industries.
- **Job Title Variety**: There's a high diversity in job titles, from Data Analyst to Director of Analytics, reflecting varied roles and specializations within data analytics.

 [Top Paying Roles](asset\Top_paying_role.png)



# What I Learned
# Conclusion
