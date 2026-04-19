# Secure File Upload
## Core Concept
File upload is one of the riskiest features. Attackers often upload malicious scripts to gain server control. Secure file upload prevents execution of dangerous files.

## Why It Matters
Unrestricted file upload leads to remote code execution (RCE), server takeover, and data loss.

## How It Works (Theory)
1. Validate file type, extension, and content.
2. Rename files to avoid path traversal or execution.
3. Store files outside the web root.
4. Scan files for malware.
5. Limit file size and upload frequency.

## Practical Example
- Allow only image types (jpg, png, gif)
- Check MIME type and file signature
- Generate random filenames
- Save outside public directory
- Serve via a secure download endpoint

## How to Defend / Secure
- Whitelist allowed extensions
- Validate MIME types
- Rename uploaded files
- Store outside web root
- Scan files for malware
- Limit file size

## Key Takeaways
1. Never trust file uploads from users.
2. Extension checking is not enough.
3. Always store uploaded files securely.
