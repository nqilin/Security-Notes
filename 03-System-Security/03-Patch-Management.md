# Patch Management Basics
## Core Concept
Patch management is the process of updating software, OS, and firmware with security patches to fix vulnerabilities. Patches are released by vendors to address known security flaws.

## Why It Matters
Most hackers exploit known vulnerabilities that have already been fixed by patches. Failing to apply patches leaves systems wide open to attacks (e.g., ransomware, data theft).

## How It Works (Theory)
1. Vendors discover vulnerabilities and develop patches to fix them.
2. Administrators (or automatic tools) detect missing patches on systems.
3. Patches are tested to ensure they do not break existing functionality.
4. Patches are deployed to all affected systems.
5. Verify that patches are applied successfully.

## Practical Example
A critical vulnerability is found in a popular OS. The vendor releases a security patch. If a user fails to install the patch, a hacker can use the vulnerability to gain access to their device and steal data.

## How to Defend / Secure
1. Enable automatic updates for OS and critical applications.
2. Regularly scan systems for missing patches.
3. Test patches in a non-production environment before deployment.
4. Set a schedule for patch deployment (e.g., weekly for non-critical, immediately for critical).

## Key Takeaways
1. Patches fix known vulnerabilities that hackers can exploit.
2. Unpatched systems are the easiest targets for attacks.
3. Automatic updates + regular scanning = effective patch management.
