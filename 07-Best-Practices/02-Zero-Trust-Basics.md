# Zero Trust Basics
## Core Concept
Zero Trust is a security framework based on the principle: "Never trust, always verify." It assumes no user or device is trusted by default, even if inside the internal network.

## Why It Matters
Traditional network security (perimeter-based) fails to protect against internal threats and remote work risks. Zero Trust provides a more robust, modern approach to securing systems.

## How It Works (Theory)
1. **Verify every access request**: Authenticate and authorize users/devices for every resource.
2. **Least privilege access**: Grant only the minimum access needed to complete a task.
3. **Assume breach**: Treat all network traffic as untrusted, even internal traffic.
4. **Continuous monitoring**: Track user/device behavior to detect anomalies.
5. **Microsegmentation**: Split networks into small segments to limit breach impact.

## Practical Example
- A remote employee tries to access a company database:
  1. The employee must authenticate with MFA.
  2. The device is scanned for security updates and malware.
  3. The employee is granted only read access (not write) for the specific database.
  4. The session is monitored for unusual activity (e.g., downloading large amounts of data).

## How to Defend / Secure
1. Implement MFA for all users and devices.
2. Use microsegmentation to isolate critical resources.
3. Continuously monitor user behavior and network traffic.
4. Enforce device security policies (updates, antivirus, encryption).
5. Apply least privilege access to all systems and data.

## Key Takeaways
1. Zero Trust = "Never trust, always verify" for all access.
2. It protects against internal and external threats.
3. MFA, least privilege, and continuous monitoring are core to Zero Trust.
