# OS Permissions Basics
## Core Concept
Operating System (OS) permissions control which users can access, modify, or execute files, folders, and system resources. They are a fundamental layer of system security to prevent unauthorized access.

## Why It Matters
Most system breaches happen because of misconfigured permissions. For example, a regular user with admin-level permissions can accidentally or maliciously delete critical system files.

## How It Works (Theory)
1. Every OS (Windows, Linux, macOS) has a user and group system.
2. Permissions are assigned to users/groups for each resource (read, write, execute).
3. - Read: View the content of a file/folder.
   - Write: Modify or delete a file/folder.
   - Execute: Run a file (e.g., a script or program).
4. The OS checks permissions before allowing any action on a resource.

## Practical Example
- Linux: A file with permissions "rwxr--r--" means:
  - The owner can read, write, and execute the file.
  - Members of the owner’s group can only read the file.
  - All other users can only read the file.
- Windows: A file set to "Read-Only" prevents users from modifying or deleting it.

## How to Defend / Secure
1. Follow the principle of least privilege: Give users only the permissions they need to do their job.
2. Never use the admin/root account for daily tasks.
3. Regularly check and revoke unnecessary permissions.
4. Set strong permissions for critical system files (e.g., no write access for regular users).

## Key Takeaways
1. Permissions control who can do what with system resources.
2. Least privilege is the golden rule for permission configuration.
3. Misconfigured permissions are a common and avoidable security risk.
