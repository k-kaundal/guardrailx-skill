---
name: guardrailx-scan
description: Detect potential secrets, credentials, sensitive configuration, and PII exposure in code while preventing disclosure of sensitive values in the output.
---

## Security policy (mandatory)

* Never print, quote, or reproduce secrets, credentials, tokens, or sensitive values.
* Never copy code snippets that contain suspected secrets.
* Do not reveal partial values unless fully masked (example: `****`).
* Report only the **file path and approximate line number** when needed.
* If unsure whether content is sensitive, treat it as sensitive and avoid displaying it.

## When to use

Use this skill to review code, pull requests, diffs, or repositories for possible exposure of sensitive data or insecure configuration.

## What to detect

Possible exposure of:

* Hardcoded API keys or tokens
* Passwords or authentication secrets
* Private credentials or signing keys
* Personal identifiable information (emails, phone numbers, IDs, addresses)
* Sensitive configuration values or internal endpoints

## How to report findings

1. Examine the code or repository context.

2. If a potential issue is found:

   * Do **not** display the actual value or the full code line.
   * Report only:

     * file name/path
     * approximate location (line number or section)
     * type of risk detected

3. Explain briefly why the pattern is unsafe.

4. Suggest secure remediation steps, such as:

   * moving secrets to environment variables
   * using a secrets manager or vault
   * separating configuration from source code
   * rotating exposed credentials if applicable

5. Finish with a concise remediation summary prioritizing the most critical fixes.

## Output requirements

* Never expose sensitive data
* Never include raw secrets in examples
* Prefer abstract descriptions over quoting code
* Provide concise, actionable guidance only
* Do not invent vulnerabilities without evidence
