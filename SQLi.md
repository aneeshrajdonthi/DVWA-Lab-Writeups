# SQL Injection (SQLi) in DVWA

In this section, I demonstrate how I exploited **SQL Injection (SQLi)** in **DVWA** to bypass authentication and gain unauthorized access.

## Objective
The goal was to bypass the login page by injecting a malicious SQL query.

## Steps to Exploit

1. **Identify Vulnerability**:  
   I accessed the **Login** section in DVWA, which was vulnerable to SQL injection due to improper sanitization of user input.

2. **Craft Payload**:  
   I injected the following SQL payload in the **Username** or **Password** fields:
   ```sql
   ' OR 1=1-- 
This payload is used to manipulate the SQL query sent to the database. The -- comments out the rest of the query, causing the authentication logic to always succeed.

Bypass Authentication:
Upon submitting the form, the application granted access without proper validation because the query always evaluated to true.

Analysis:
The SQL injection vulnerability allowed me to bypass authentication by exploiting an unsanitized input. This type of attack can be used to access sensitive user data or escalate privileges.

Conclusion
SQL Injection is one of the most critical vulnerabilities. It is important to use prepared statements and parameterized queries to prevent this attack. Always validate and sanitize user input to mitigate the risk.

sql
Copy
Edit
