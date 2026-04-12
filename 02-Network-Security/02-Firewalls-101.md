# Firewalls 101
## Core Concept
A firewall is a network security system that monitors and filters incoming and outgoing traffic based on predefined rules. It acts as a barrier between trusted internal networks and untrusted external networks.

## Why It Matters
Firewalls are the first line of defense. They block unauthorized access, port scans, brute force attacks, and many common network threats before they reach your system.

## How It Works (Theory)
1. Inspects each packet’s source IP, destination IP, port, and protocol.
2. Compares packets against allowlist and blocklist rules.
3. Permits legitimate traffic and denies or drops malicious traffic.
4. Logs all activity for later auditing and analysis.

## Practical Example
A server runs a website on port 80/443. The firewall allows only those ports and blocks all other ports like 22, 3389 from public access. This stops automated scanners and brute force attacks.

## How to Defend / Secure
1. Follow the default deny principle: block everything unless explicitly allowed.
2. Allow only necessary ports and services.
3. Block known malicious IP ranges.
4. Regularly review and clean up outdated firewall rules.

## Key Takeaways
1. Firewall = Traffic gatekeeper between internal and external networks.
2. Default deny is the most secure configuration.
3. Proper firewall rules drastically reduce attack surface.
