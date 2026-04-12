# DDoS Basics and Protection
## Core Concept
DDoS (Distributed Denial of Service) is an attack where multiple compromised systems flood a target with traffic, overwhelming its resources and making it unavailable to legitimate users.

## Why It Matters
DDoS attacks can take down websites, apps, and entire networks quickly. They are one of the most common and disruptive attacks on the internet.

## How It Works (Theory)
1. An attacker controls a botnet (many infected devices).
2. All bots send massive traffic to the target simultaneously.
3. The target’s bandwidth, CPU, or memory is exhausted.
4. Legitimate users cannot access the service.

## Practical Example
A small website suddenly receives millions of fake requests per second. The server becomes unresponsive, and the website goes offline. This is a typical HTTP flood DDoS attack.

## How to Defend / Secure
1. Use cloud-based DDoS protection services to filter traffic.
2. Limit request rates per IP at the server or CDN level.
3. Use anycast networks to distribute traffic.
4. Enable SYN cookies and connection tracking to resist TCP floods.

## Key Takeaways
1. DDoS = Flooding a system to make it unavailable.
2. Local servers cannot defend against large-scale DDoS alone.
3. Cloud scrubbing and rate limiting are the most effective defenses.
