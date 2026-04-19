# Input Validation & Sanitization
## Core Concept
Input validation ensures user data follows expected rules. Sanitization cleans dangerous content to prevent injection and XSS.

## Why It Matters
Nearly all web vulnerabilities come from untrusted user input. Validation is the first line of defense.

## How It Works (Theory)
1. Validate type, length, format, and range.
2. Reject invalid inputs early.
3. Sanitize special characters before rendering or storing.
4. Use allowlists, not blocklists.

## Practical Example
- Validate email format
- Restrict username to letters/numbers only
- Limit input length
- Escape HTML/JS before rendering
- Use parameterized queries for databases

## How to Defend / Secure
- Validate all inputs
- Use strict allowlists
- Sanitize before output
- Escape special characters
- Never use raw user input in SQL/HTML/JS

## Key Takeaways
1. All user input is untrusted.
2. Validation > sanitization.
3. Whitelisting is safer than blacklisting.
