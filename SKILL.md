---
name: guardrailx-scan
description: Detect potential secrets, credentials, sensitive configuration, and PII exposure in code while preventing disclosure of sensitive values in the output.
---

## When to use

Use this skill when reviewing code, pull requests, diffs, or repositories for possible exposure of sensitive data or insecure configuration.

## What to check

Look for potential:

* Hardcoded API keys or tokens
* Passwords or authentication secrets
* Private credentials or signing keys
* Personal identifiable information (emails, phone numbers, IDs, addresses)
* Sensitive configuration values or internal endpoints

## How to report findings

1. Inspect the selected code or repository files.
2. If sensitive data is detected:

   * **Do NOT reproduce or expose the full value**
   * Show only a masked example if needed (e.g., `sk-****abcd`)
   * Refer to the location (file + line) instead of printing secrets
3. Briefly explain why the pattern is risky.
4. Recommend secure fixes, such as:

   * moving values to environment variables
   * using a secrets manager or vault
   * separating configuration from source code
   * masking or sanitizing sensitive logs/output
5. Provide a short remediation summary prioritizing the most important fixes.

## Output guidelines

* Never reveal full secrets, tokens, or credentials
* Mask sensitive values in any examples
* Prefer referencing file locations over copying sensitive content
* Be concise and actionable
* Avoid speculation if evidence is unclear
* Do not invent issues that are not present
