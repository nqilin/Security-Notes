# HTTP Security Headers
## Core Concept
HTTP security headers are response headers that enhance browser security. They prevent XSS, clickjacking, MIME sniffing, and other common attacks.

## Why It Matters
Headers provide free, effective protection with minimal code changes. They are a basic but critical layer of web security.

## How It Works (Theory)
1. Headers instruct browsers to enforce security rules.
2. They are sent from the server with every response.
3. Modern browsers respect these headers to block dangerous behavior.

## Practical Example
- Content-Security-Policy (CSP)
- X-XSS-Protection
- X-Content-Type-Options: nosniff
- X-Frame-Options: DENY
- Strict-Transport-Security (HSTS)
- Permissions-Policy

## How to Defend / Secure
- Enable all modern security headers
- Use HSTS to force HTTPS
- Set strict CSP to block XSS
- Prevent clickjacking with X-Frame-Options
- Disable MIME sniffing

## Key Takeaways
1. Security headers are easy to implement.
2. They block many common web attacks.
3. Every production website should use them.
