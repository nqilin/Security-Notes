# Wireshark Basics
## Core Concept
Wireshark is a network protocol analyzer that captures and inspects packets traveling across a network. It shows real-time data flow in readable format.

## Why It Matters
Wireshark helps troubleshoot networks and detect malicious traffic such as data leaks, malware communication, and attacks.

## How It Works (Theory)
1. Capture live packets from a network interface.
2. Filter traffic by IP, port, protocol, or content.
3. Inspect packet headers and payload.
4. Analyze TCP, UDP, HTTP, HTTPS, DNS, and more.
5. Detect abnormal or malicious behavior.

## Practical Example
- Capture HTTP traffic to see unencrypted data.
- Filter TCP packets: `tcp.port == 80`
- Find suspicious DNS queries.

## How to Defend / Secure
1. Use HTTPS to encrypt traffic so Wireshark cannot read payloads.
2. Use VPNs to protect sensitive communication.
3. Monitor for unusual packet patterns.
4. Encrypt all sensitive data in transit.

## Key Takeaways
1. Wireshark captures and analyzes network packets.
2. Unencrypted data can be fully read.
3. HTTPS/VPN prevent packet inspection.
