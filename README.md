## 🏆 Premier League Data Pipeline: ETL Overview

This project demonstrates an **End-to-End Data Engineering pipeline (ETL)** that fetches football data for Premier League season 2024-2025 and prepares it for professional analytics.

![image alt](https://github.com/majedabdualla/Premier-league-Standings-2020-2025/blob/ee63fab2143bda4f373be736491adbf44f5a826c/assets/Project%20workflow.jpg)

This summary highlights practical experience in:

- API Integration  
- Data Cleaning & Transformation  
- Database Design & Management
- Data Visualization  


---

##  Technical Stack

**Language:**  
- Python  

**Libraries:**  
- Requests (API Integration)  
- Pandas (ETL & Data Transformation)  
- SQLAlchemy (Database Engine)  

**Database:**  
- PostgreSQL  

**API:**  
- Football-Data.org (RESTful API)  
**Visualization:**  
- Power BI 
---

## Implementation Steps

### 1️⃣ Data Extraction (Extract)

- Connected to a RESTful API using the `requests` library.
- Managed secure authentication using **API Tokens** passed through HTTP headers.
- Retrieved raw competition data in **JSON format**.

---

### 2️⃣ Data Transformation (Transform)

- **Normalization:**  
  Used `pandas.json_normalize()` to flatten nested JSON structures into a tabular DataFrame.

- **Cleaning & Renaming:**  
  Renamed columns to follow SQL-friendly naming conventions (e.g., removing dots and spaces).

- **Schema Organization:**  
  Rearranged column order to prioritize the **Primary Key (`team_id`)** and essential metrics for improved database readability.

---

### 3️⃣ Data Loading (Load)

- **Engine Creation:**  
  Built a database connection bridge using **SQLAlchemy** and the `psycopg` driver.

- **Automation:**  
  Utilized the `.to_sql()` method to automate table creation and data insertion.

- **Data Integrity:**  
  Implemented `if_exists='replace'` logic to ensure dashboards always reflect the most recent standings without duplicate rows.

  
![image alt](https://github.com/majedabdualla/Premier-league-Standings-2020-2025/blob/ee63fab2143bda4f373be736491adbf44f5a826c/assets/postgresql.jpg)
---

### 4️⃣ Data Visualization & Reporting

- Connected **Power BI** directly to PostgreSQL.
- Designed an interactive dashboard to summarize league performance in season 2024-2025.
- Created visual insights including:
  - Team rankings and standings  
  - Goals scored vs conceded analysis   
  - Performance trend comparisons  

- Enabled business-friendly analytics by transforming raw standings into easy-to-understand KPIs and visuals.

![image alt](https://github.com/majedabdualla/Premier-league-Standings-2020-2025/blob/ee63fab2143bda4f373be736491adbf44f5a826c/assets/screenshot.jpg)
---

## 📈 Key Engineering Concepts Applied

- **Stateless Communication**  
  Handling independent requests to a REST API.

- **Environment Variables**  
  Used `os.getenv()` to securely manage database credentials and avoid hardcoding sensitive information.

- **Vectorized Operations**  
  Leveraged Pandas for efficient bulk data cleaning instead of slower Python loops.

---

## 🎯 Project Outcome

- Built a scalable ETL pipeline from API to database.
- Demonstrated production-style data cleaning and transformation practices.
- Prepared analytics-ready data suitable for dashboards and reporting tools.
- Developed an interactive Power BI dashboard for performance monitoring and insights.

