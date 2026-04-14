# CSRF Attack Prevention
## Core Concept
Cross-Site Request Forgery (CSRF) is an attack that tricks a logged-in user's browser into sending unwanted requests to a trusted web application.

## Why It Matters
Attackers can perform actions like changing passwords, transferring funds, or modifying data on behalf of the user without their knowledge.

## How It Works (Theory)
1. The user logs into a trusted application and receives a session cookie.
2. The user visits a malicious website or email link.
3. The malicious site sends a request to the trusted application.
4. The browser automatically includes the user's session cookie.
5. The server accepts the request as legitimate.

## Practical Example
A malicious page contains:
`<img src="https://bank.com/transfer?amount=1000&to=attacker">`
When the user visits the page, their browser sends the transfer request using their active bank session.

## How to Defend / Secure
1. **CSRF Tokens**: Generate and validate unique tokens for all state-changing requests.
2. **SameSite Cookies**: Set `SameSite=Strict` or `SameSite=Lax` on session cookies.
3. **Re-authentication**: Require password re-entry for sensitive actions.
4. **Origin/Referer Validation**: Check the Origin or Referer header for requests.

## Key Takeaways
1. CSRF = performing actions on behalf of a logged-in user without consent.
2. CSRF tokens are the most effective and widely used defense.
3. SameSite cookies provide a strong additional layer of protection.
