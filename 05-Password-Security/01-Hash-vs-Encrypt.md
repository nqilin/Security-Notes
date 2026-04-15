# Hash vs Encrypt
## Core Concept
Hashing and encryption are two different cryptographic methods for securing data, with distinct use cases in password security.

## Why It Matters
Confusing hashing and encryption leads to critical security mistakes, such as storing passwords in an encryptable (reversible) format instead of a one-way hash.

## How It Works (Theory)
### Hashing
- One-way function: Converts data into a fixed-length string (hash) that cannot be reversed back to the original data.
- Used for password storage: Store hashes, not plaintext passwords.
- Example algorithms: SHA-256, bcrypt, Argon2.

### Encryption
- Two-way function: Converts data into ciphertext that can be decrypted back to the original data with a key.
- Used for secure data transmission/storage (e.g., encrypting files, messages).
- Example algorithms: AES, RSA.

## Practical Example
- **Hashing**: When you create a password, the system stores `bcrypt(password)` instead of the plaintext. When you log in, it hashes your input and compares the hashes.
- **Encryption**: When you send a credit card number, it's encrypted with AES, and only the merchant can decrypt it with a key.

## How to Defend / Secure
1. **Always hash passwords, never encrypt them**: Hashing is irreversible, so even if the database is breached, attackers cannot get plaintext passwords.
2. Use slow, salted hashing algorithms (bcrypt, Argon2) instead of fast hashes (SHA-256).
3. Never store plaintext passwords or encryptable passwords.

## Key Takeaways
1. **Hash = one-way, irreversible; Encrypt = two-way, reversible**.
2. Passwords must be hashed, never encrypted.
3. Use slow, salted hashing algorithms for maximum security.
