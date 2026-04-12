# IDS and IPS Fundamentals
## Core Concept
- IDS (Intrusion Detection System): Detects suspicious activity and generates alerts but does not block traffic.
- IPS (Intrusion Prevention System): Detects and automatically blocks malicious traffic in real time.

## Why It Matters
Firewalls filter traffic based on IP/port, but cannot understand attack content. IDS/IPS inspect packet payloads to detect SQL injection, XSS, exploits, and other application-layer attacks.

## How It Works (Theory)
1. Captures and analyzes all network traffic.
2. Matches traffic against a signature database of known attacks.
3. IDS: Logs and alerts administrators.
4. IPS: Drops malicious packets or blocks the source IP immediately.

## Practical Example
A hacker sends a malicious request attempting SQL injection. The firewall allows port 80 traffic, but the IPS detects the attack pattern and blocks the IP before the request reaches the server.

## How to Defend / Secure
1. Keep IDS/IPS signature database updated.
2. Deploy IPS in inline mode for critical services.
3. Tune rules to reduce false positives.
4. Review alerts daily to identify persistent threats.

## Key Takeaways
1. IDS = Detect & Alert; IPS = Detect & Block.
2. IDS/IPS protects against application-layer attacks.
3. Regular signature updates are critical for effectiveness.
