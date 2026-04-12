# IP, TCP and UDP Basics
## Core Concept
IP, TCP, and UDP are the core protocols that power all network communication. IP handles addressing, TCP ensures reliable delivery, and UDP provides fast, connectionless transmission.

## Why It Matters
Nearly all network attacks — such as port scanning, DDoS, and data interception — rely on these protocols. Understanding them is essential to secure networks and analyze threats.

## How It Works (Theory)
1. IP (Internet Protocol): Assigns a unique address to each device and routes data between devices.
2. TCP (Transmission Control Protocol): Connection-oriented, guarantees data order and integrity, used for web, email, and file transfer.
3. UDP (User Datagram Protocol): Connectionless, lightweight, fast, used for streaming, gaming, and voice calls.

## Practical Example
- When visiting a website: Your browser uses IP to find the server, TCP to load pages reliably.
- When playing online games: The game uses UDP for low-latency transmission even if some packets are lost.

## How to Defend / Secure
1. Restrict access by allowing only trusted IP ranges.
2. Close unused TCP/UDP ports on firewalls.
3. Block abnormal UDP floods to prevent basic DDoS.
4. Use TCP flags and session management to detect spoofed connections.

## Key Takeaways
1. IP = Addressing, TCP = Reliable, UDP = Fast.
2. Most attacks target open ports and unprotected protocols.
3. Filtering traffic by IP, port, and protocol is the foundation of network security.
