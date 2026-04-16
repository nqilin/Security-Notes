# OpenSSL Basics
## Core Concept
OpenSSL is a powerful open-source toolkit for TLS/SSL encryption and cryptographic functions. It secures data transmission and manages certificates.

## Why It Matters
OpenSSL powers most HTTPS websites. It provides encryption, hashing, signing, and certificate management for all secure systems.

## How It Works (Theory)
1. Implements TLS/SSL for encrypted connections.
2. Supports symmetric and asymmetric encryption.
3. Creates and verifies digital certificates.
4. Generates hashes, keys, and signed data.

## Practical Example
Generate a hash:
`openssl sha256 file.txt`

Generate a private key:
`openssl genrsa -out private.key 2048`

## How to Defend / Secure
1. Always use latest OpenSSL version.
2. Use strong ciphers and key lengths.
3. Keep TLS certificates valid.
4. Disable old, insecure protocols (SSLv3, TLS 1.0/1.1).

## Key Takeaways
1. OpenSSL = encryption + TLS + certificates.
2. Used in nearly all secure web servers.
3. Must be kept updated to avoid vulnerabilities.
