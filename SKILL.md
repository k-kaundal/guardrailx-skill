---
name: guardrailx-scan
description: Analyze code for potential secrets, credentials, and PII exposure and suggest secure practices.
---

When this skill is invoked:

1. Review the selected code or repository files.
2. Identify potential security risks such as:
   - hardcoded API keys
   - tokens or passwords
   - private credentials
   - personal identifiable information (emails, phone numbers, IDs)
   - sensitive configuration values
3. Highlight risky lines and explain why they are unsafe.
4. Suggest secure alternatives:
   - environment variables
   - secrets manager / vault usage
   - config separation
   - masking sensitive output
5. Provide a concise remediation summary.

Focus on practical developer-friendly fixes and avoid speculation.
