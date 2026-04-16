# Nmap Basics
## Core Concept
Nmap (Network Mapper) is a free, open-source tool for network discovery and security auditing. It is used to scan networks, find live hosts, open ports, and detect services.

## Why It Matters
Nmap is the most widely used network scanning tool. It helps defenders find vulnerabilities, open ports, and exposed services before attackers do.

## How It Works (Theory)
1. Send packets to target hosts.
2. Analyze responses to determine if hosts are online.
3. Detect open/closed/filtered ports.
4. Identify running services and versions.
5. Detect OS types and hardware details.

## Practical Example
Basic scan:
`nmap 192.168.1.1`

Full scan with service detection:
`nmap -A 192.168.1.1`

## How to Defend / Secure
1. Use firewalls to block port scanning.
2. Close unused open ports.
3. Monitor for unexpected Nmap or scan traffic.
4. Hide service versions from public exposure.

## Key Takeaways
1. Nmap = network scanner for hosts, ports, and services.
2. Used by both defenders and attackers.
3. Essential for network security testing.
