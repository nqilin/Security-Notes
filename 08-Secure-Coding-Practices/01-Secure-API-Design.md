# Secure API Design
## Core Concept
Secure API design means building APIs that prevent unauthorized access, data leaks, injection attacks, and abuse. It follows security-first principles while maintaining functionality.

## Why It Matters
APIs are the main entry point for modern applications. Insecure APIs lead to data breaches, account hijacking, and full system compromise.

## How It Works (Theory)
1. Authenticate all requests using strong tokens (JWT, OAuth2).
2. Enforce authorization to ensure users can only access their own data.
3. Validate and sanitize all input parameters.
4. Use HTTPS for all API communication.
5. Return minimal data and avoid leaking sensitive information.
6. Set proper rate limits to prevent abuse.

## Practical Example
Bad practice:
/api/user?id=123 (allows changing ID to access others’ data)

Good practice:
Get user ID from authenticated token, not from request parameter.

## How to Defend / Secure
- Use JWT/OAuth2 for authentication
- Enforce least privilege authorization
- Validate all inputs
- Use HTTPS only
- Add rate limiting
- Avoid exposing internal IDs or sensitive data

## Key Takeaways
1. Never trust user inputs in APIs.
2. Auth & Authz are the foundation of API security.
3. Return only necessary data to minimize leaks.
