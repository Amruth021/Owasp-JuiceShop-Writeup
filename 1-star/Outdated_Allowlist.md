# Juice Shop Write-up: Outdated Allowlist Challenge

## Challenge Details

**Difficulty** : ✯.\
**Category** : Unvalidated Redirects

**Description**

- Let us redirect you to one of our crypto currency addresses which are not promoted any longer.
- The Outdated Allowlist vuln. involve exploiting a vulnerability where an outdated URL allowlist can be bypassed to redirect users to unauthorized destinations using the redirect?to= parameter.

## Solution

- **Identify the Issue**:  The web app provides QR code for crypto transaction in wallet section. The JavaScript code managing these QR codes, found within the main.js file, reveals that specific cryptocurrency addresses are hard-coded, and there is a redirect function that points to these addresses based on the user's selection.
  
  <img src=".." alt="code image" width="500px">
  
- **Exploit**: Navigate to the redirect URL to solve the challenge

- **Why it works**: Unvalidated redirects are vulnerabilities in web applications that occur when user-controlled input is used to redirect users to external URLs without proper validation. This can lead to phishing attacks and other security risks.

## Remediation

- Ensure that all redirect URLs are validated against a whitelist of allowed domains or paths before processing the redirect.
- Implement user confirmation steps, such as a disclaimer page, to inform users they are leaving the site.
