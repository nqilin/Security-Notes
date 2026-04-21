# Security Logging & Auditing
## Core Concept
Security logging records critical events (login, data access, changes) to detect attacks, investigate breaches, and ensure compliance. Auditing reviews logs to identify anomalies.

## Why It Matters
Without logs, you cannot detect when an attack occurs or investigate what happened. Logs are essential for incident response and security compliance.

## How It Works (Theory)
1. Log all security-relevant events (login attempts, data modifications, access denied).
2. Include key details: timestamp, user ID, IP address, action, status.
3. Store logs securely (immutable, encrypted, off-server).
4. Regularly review logs to detect unusual activity.

## Practical Example
Flask logging implementation (simplified):
```python
import logging
from flask import Flask, request

app = Flask(__name__)

# Configure security logging
logging.basicConfig(
    filename="security.log",
    level=logging.INFO,
    format="%(asctime)s - IP: %(ip)s - User: %(user)s - Action: %(action)s - Status: %(status)s"
)

@app.route("/login", methods=["POST"])
def login():
    user = request.form.get("username")
    ip = request.remote_addr
    success = True  # Replace with actual authentication logic
    
    logging.info("", extra={
        "ip": ip,
        "user": user,
        "action": "login_attempt",
        "status": "success" if success else "failure"
    })
    return "Login attempt logged"
```

## How to Defend / Secure
- Log all authentication attempts (success/failure).
- Log data access and modifications (especially sensitive data).
- Store logs securely (off-server, encrypted).
- Avoid logging sensitive data (passwords, tokens).
- Regularly review logs for anomalies.

## Key Takeaways
1. Logs are critical for incident detection and investigation.
2. Never log sensitive data (passwords, JWT tokens).
3. Secure log storage prevents tampering.
