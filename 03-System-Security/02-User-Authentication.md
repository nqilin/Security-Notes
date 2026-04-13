# User Authentication Basics
## Core Concept
User authentication is the process of verifying that a user is who they claim to be. It ensures only authorized users can access a system, device, or application.

## Why It Matters
Without proper authentication, anyone can access sensitive data or control a system. Weak authentication (e.g., simple passwords) is one of the top causes of security breaches.

## How It Works (Theory)
1. The user provides credentials (e.g., username + password, biometrics).
2. The system verifies the credentials against a stored database.
3. If credentials match, the user is granted access; otherwise, access is denied.
4. Common authentication methods: Single-Factor (password), Two-Factor (2FA), Multi-Factor (MFA).

## Practical Example
- Single-Factor: Logging into a website with just a username and password.
- Two-Factor (2FA): Logging in with a password + a code sent to your phone (e.g., Google Authenticator).
- Biometric Authentication: Unlocking your phone with your fingerprint or face.

## How to Defend / Secure
1. Enforce strong password policies (long, complex, unique).
2. Enable Two-Factor Authentication (2FA) for all user accounts.
3. Never share credentials or store them in plain text.
4. Lock user accounts after multiple failed login attempts.

## Key Takeaways
1. Authentication = Proving you are who you say you are.
2. 2FA drastically reduces the risk of stolen credentials.
3. Strong credentials + 2FA is the minimum for secure authentication.
