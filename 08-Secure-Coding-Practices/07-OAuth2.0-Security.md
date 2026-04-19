# OAuth2.0 Security Best Practices
## Core Concept
OAuth2.0 is an authorization framework that allows third-party apps to access user data without sharing passwords. Improper implementation leads to unauthorized access and data leaks.

## Why It Matters
OAuth2.0 is widely used for social login and API authorization. Weak OAuth2.0 setups are a common target for attackers to gain access to user accounts and sensitive data.

## How It Works (Theory)
1. OAuth2.0 uses authorization tokens to grant access.
2. Key roles: Resource Owner (user), Client (app), Authorization Server, Resource Server.
3. Common grant types: Authorization Code, Client Credentials, Password (not recommended).
4. Tokens can be stolen or misused if not secured.

## Practical Example
- Use Authorization Code Grant (most secure) instead of Password Grant.
- Validate redirect URIs to prevent open redirects.
- Use HTTPS for all OAuth2.0 communication.
- Shorten access token expiration (15–30 min).

## How to Defend / Secure
- Use Authorization Code Grant for user-facing apps.
- Validate redirect URIs (whitelist only trusted domains).
- Use HTTPS exclusively.
- Shorten access token lifetime.
- Securely store client secrets (never in frontend code).
- Implement PKCE for mobile/native apps.

## Key Takeaways
1. OAuth2.0 is for authorization, not authentication.
2. Authorization Code Grant is the most secure grant type.
3. Never expose client secrets in public code.
