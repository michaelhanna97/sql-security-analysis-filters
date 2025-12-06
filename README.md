# 🛢️ SQL Filtering for Security Analysis – Login & Employee Data Investigation

## 📌 Overview
This project demonstrates how SQL filtering techniques can be utilized to investigate security incidents, analyze login activity, and identify employees who require workstation updates. Using logical operators, pattern matching, and conditional filtering, I extracted targeted insights from database tables such as **log_in_attempts** and **employees**.

This work shows hands-on experience with SQL in a security context, supporting incident investigation and system hardening tasks.

---

## 🗂️ Project File
- **SQL-Security-Filtering-Analysis.pdf**  
  Includes:
  - After-hours failed login investigation  
  - Suspicious date-based login filtering  
  - Querying logins outside Mexico  
  - Identifying employees in specific departments and buildings  
  - Filtering for employees not in IT  
  - Explanation of SQL operators (AND, OR, NOT, LIKE, wildcard %)

---

## 🔍 Scenario Summary

### ✔ After-hours failed logins  
Using the `log_in_attempts` table, I filtered for failed login attempts **after 18:00** using:
- `login_time > '18:00'`
- `success = FALSE`

This helped isolate login attempts related to a security incident occurring outside business hours.

### ✔ Logins on suspicious dates  
A suspicious event occurred on **2022-05-09**, so I retrieved all login attempts from **May 8th and May 9th** using:
- A `WHERE` clause with the `OR` operator  
- Exact date matching conditions  

### ✔ Logins outside of Mexico  
I filtered for login attempts originating **outside Mexico** using:
- `NOT`
- `LIKE 'MEX%'`
- `%` wildcard for pattern matching  

### ✔ Employees in Marketing (East building)
Using the `employees` table, I filtered for:
- `department = 'Marketing'`
- `office LIKE 'East%'`

This allowed the team to update machines only for employees meeting both criteria.

### ✔ Employees in Finance OR Sales
I retrieved employees from:
- Finance  
- Sales  
using:
- `OR` operator  

### ✔ Employees NOT in IT
To perform targeted updates, I filtered for employees **not** in the IT department using:
- `WHERE department NOT LIKE 'Information Technology'`

---

## 🛠️ Skills Demonstrated
- SQL filtering for security investigations  
- Using `WHERE`, `AND`, `OR`, `NOT`  
- Pattern matching with `LIKE` and wildcard `%`  
- Extracting authentication insights from login tables  
- Identifying anomalies and suspicious behavior  
- Filtering employee data for system update tasks  
- Supporting incident response workflow with SQL queries  

---

## 🧩 Key Technical Concepts
### 🔎 Logical Operators  
- **AND** restricts results to rows matching *all* conditions  
- **OR** returns rows matching *any* condition  
- **NOT** excludes records based on a specified rule  

### 🔎 Pattern Matching  
- `LIKE 'MEX%'` used to match country codes beginning with "MEX"  
- `%` wildcard matches any number of unknown characters  

### 🔎 Security Use Cases  
- Investigating unauthorized login behavior  
- Identifying login anomalies by time, country, or date  
- Segmenting employees for workstation security updates  

---

## 📌 What This Project Shows Employers
This project demonstrates my ability to:

- Use SQL to support **cybersecurity investigations**  
- Filter, analyze, and extract meaningful insights from authentication logs  
- Apply **logical operators and pattern matching** to refine datasets  
- Identify suspicious login activity  
- Support IT and security teams using precise data filtering  
- Document SQL queries and their purpose clearly  

---

## 📌 Roles This Project Aligns With
- **Cybersecurity Analyst (Entry Level)**  
- **SOC Analyst – Tier 1**  
- **IT Support / Desktop Support (with security focus)**  
- **GRC Analyst (technical data filtering)**  
- **Data Analyst (Security Operations)**  

---

## 📬 Contact
- **GitHub Portfolio:** *https://github.com/michaelhanna97*  
- **LinkedIn:** *your LinkedIn link here (optional)*  
