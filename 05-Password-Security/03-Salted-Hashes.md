# Salted Hashes
## Core Concept
A salted hash is a cryptographic technique where a unique, random string (salt) is added to a password before hashing, preventing rainbow table attacks and hash collisions.

## Why It Matters
Unsalted hashes are vulnerable to rainbow table attacks, where attackers precompute hashes of common passwords. Salting makes these attacks infeasible.

## How It Works (Theory)
1. Generate a unique, cryptographically secure random salt for each user.
2. Combine the user's password with the salt.
3. Hash the combined value (password + salt) using a slow hashing algorithm (bcrypt, Argon2).
4. Store both the salt and the hash in the database.
5. When verifying, retrieve the salt, hash the input password + salt, and compare.

## Practical Example
- **Unsalted hash**: `SHA-256("password123") = 9f86d081884c7d659a2feaa0c55ad015a3bf4f1b2b0b822cd15d6c15b0f00a08`
- **Salted hash**: `bcrypt("password123" + "random_salt_123")`
Each user gets a unique salt, so even if two users have the same password, their hashes are different.

## How to Defend / Secure
1. **Always use unique, random salts for each password**.
2. Use slow, adaptive hashing algorithms (bcrypt, Argon2) that automatically handle salting.
3. Never reuse salts across multiple users.
4. Use cryptographically secure random number generators for salts.

## Key Takeaways
1. Salting adds a unique random string to passwords before hashing.
2. Salts prevent rainbow table attacks and identical hash collisions.
3. Modern hashing algorithms (bcrypt, Argon2) handle salting automatically.
