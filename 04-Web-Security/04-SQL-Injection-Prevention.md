# SQL Injection Prevention
## Core Concept
SQL Injection (SQLi) is an attack where an attacker inserts malicious SQL code into user inputs, allowing unauthorized access, modification, or deletion of database data.

## Why It Matters
SQLi is one of the oldest and most dangerous web vulnerabilities. It can lead to full database compromise, data theft, or server takeover.

## How It Works (Theory)
1. The application concatenates user input directly into SQL queries without validation.
2. The attacker inputs SQL fragments to alter the query's logic.
3. The database executes the malicious query, granting the attacker access.

## Practical Example
Normal login query:
`SELECT * FROM users WHERE username = 'user' AND password = 'pass'`
Malicious input (username field):
`' OR 1=1 --`
Resulting query:
`SELECT * FROM users WHERE username = '' OR 1=1 --' AND password = '...'`
This bypasses authentication and logs the attacker in.

## How to Defend / Secure
1. **Prepared Statements (Parameterized Queries)**: Use parameterized queries to separate data from code.
2. **ORM Frameworks**: Use ORMs (e.g., SQLAlchemy, Hibernate) to avoid writing raw SQL.
3. **Input Validation**: Validate and sanitize all user inputs against expected formats.
4. **Least Privilege**: Use database users with minimal required permissions.

## Key Takeaways
1. Never trust user input in SQL queries.
2. Parameterized queries fully prevent SQL injection.
3. ORMs significantly reduce injection risks by abstracting raw SQL.
