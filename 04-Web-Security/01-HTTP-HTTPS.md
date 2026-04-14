# HTTP vs HTTPS
## Core Concept
HTTP is an unencrypted protocol for transferring web data between browsers and servers.
HTTPS is HTTP secured by TLS/SSL encryption, ensuring data confidentiality, integrity, and authenticity during transmission.

## Why It Matters
HTTP sends all data in plaintext. Attackers on the same network can intercept passwords, session cookies, and personal information.
HTTPS is the foundation of modern web security, protecting users from eavesdropping and tampering.

## How It Works (Theory)
1. HTTP: Data is transmitted as readable plain text with no encryption.
2. HTTPS: Performs a TLS handshake to establish an encrypted connection.
3. The server presents a valid SSL/TLS certificate to verify its identity.
4. All subsequent data is encrypted end-to-end, unreadable to third parties.

## Practical Example
- Logging into an HTTP website: Your password is sent in plain text, visible to anyone intercepting the traffic.
- Logging into an HTTPS website: The password is encrypted, so even if intercepted, it cannot be read.

## How to Defend / Secure
1. Enforce HTTPS for all websites and APIs.
2. Enable HSTS (HTTP Strict Transport Security) to force HTTPS usage.
3. Install and maintain valid SSL/TLS certificates.
4. Redirect all HTTP traffic to HTTPS automatically.

## Key Takeaways
1. HTTP = insecure plaintext; HTTPS = encrypted, secure communication.
2. HTTPS protects against eavesdropping, tampering, and impersonation.
3. All modern web applications must use HTTPS as a baseline.
