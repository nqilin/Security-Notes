# Session Management Best Practices
## Core Concept
Session management controls how user login state is maintained. Poor session security leads to account hijacking and session fixation attacks.

## Why It Matters
Attackers often steal or hijack sessions to impersonate users without stealing passwords.

## How It Works (Theory)
1. A session ID identifies a logged-in user.
2. Cookies are the most common way to store session IDs.
3. Attackers can steal sessions via XSS, MitM, or insecure configuration.

## Practical Example
- Use HttpOnly, Secure, SameSite=Strict cookies
- Generate long, random session IDs
- Set short session timeouts
- Regenerate session ID after login
- Invalidate sessions on logout

## How to Defend / Secure
- HttpOnly, Secure, SameSite cookies
- Short session timeout
- Regenerate SID on login
- Strong random session IDs
- Server-side session storage
- Force logout on password change

## Key Takeaways
1. Sessions are high-value targets.
2. Cookie flags are critical for defense.
3. Always invalidate sessions properly.
