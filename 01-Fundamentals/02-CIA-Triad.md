# CIA Triad
## Core Concept
The CIA Triad is the foundation of cybersecurity—three key principles to protect data: Confidentiality, Integrity, and Availability.

## Why It Matters
It provides a clear framework to evaluate and build security systems. Every cybersecurity measure should align with one or more of these three principles.

## How It Works (Theory)
1. Confidentiality: Ensures data is only accessible to authorized users (e.g., encryption).
2. Integrity: Ensures data is not altered accidentally or maliciously (e.g., hashing).
3. Availability: Ensures data and systems are accessible when needed (e.g., backups, redundant servers).

## Practical Example
- Confidentiality: Using a VPN to encrypt your internet traffic so no one can spy on your browsing.
- Integrity: Using a hash function (like SHA-256) to verify that a file hasn’t been tampered with.
- Availability: A company using cloud backups so its website stays online even if its main server fails.

## How to Defend / Secure
1. Confidentiality: Use encryption (AES) for sensitive data, restrict user access with permissions.
2. Integrity: Use hashing for data verification, implement version control for files.
3. Availability: Regular backups, use load balancers, and protect against DDoS attacks.

## Key Takeaways
1. CIA Triad = Confidentiality (secret), Integrity (accurate), Availability (accessible).
2. All three principles are equally important—weakness in one breaks the whole system.
3. Every security tool/practice should support at least one of these principles.
