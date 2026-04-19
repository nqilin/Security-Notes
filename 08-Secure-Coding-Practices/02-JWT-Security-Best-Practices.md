# JWT Security Best Practices
## Core Concept
JWT (JSON Web Token) is a compact, self-contained token used for authentication. Improper use leads to token theft, forgery, and unauthorized access.

## Why It Matters
JWT is widely used in web apps and APIs. Weak JWT implementations are one of the most common API vulnerabilities.

## How It Works (Theory)
1. JWT consists of Header.Payload.Signature.
2. The signature ensures the token is not tampered with.
3. Tokens can be stolen via XSS or MitM attacks.
4. Short expiration reduces risk if tokens leak.

## Practical Example
- Set short expiration (15–30 min)
- Use strong signing algorithm (HS256 with long secret or RS256)
- Store tokens in HttpOnly cookies, not localStorage
- Add refresh tokens for better security

## How to Defend / Secure
- Use strong signing algorithms
- Short expiration time
- Store in HttpOnly, Secure cookies
- Avoid sensitive data in payload
- Implement token revocation
- Always verify signature and expiration

## Key Takeaways
1. JWT is not encrypted, only signed.
2. localStorage is unsafe for JWT.
3. Short-lived tokens + strong signing = secure JWT.
