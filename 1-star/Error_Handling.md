# Juice Shop Write-up: Error Handling Challenge

## Challenge Overview

**Title:** Error Handling\
**Category:** Security Misconfiguration\
**Difficulty:** ⭐ (1/6)

## Challenge Description

Provoke an error that is neither very gracefully nor consistently handled.
Improper error handling occurs when an application fails to manage errors correctly, potentially revealing sensitive information

## Solution

1. **Experiment on URL Paths**: Access various non-existent or restricted URL paths web app's server to trigger error responses.
2. **Analyze**: Look for error messages that are verbose or detailed information leakage.
3. **Specific Errors**: Try accessing different files in `ftp` server which are not allowed to be downloaded.

## Solution Explanation

The error was provoked by attempting to access an invalid URL on the server, The server responded with a detailed error message indicating:

<img src=".." alt="error" width="500px">


## Remediation

- Use appropriate HTTP status codes (e.g., 400, 401, 403, 404, 500) without revealing internal application details.
- Monitor and review application logs to detect recurring errors or attempted attacks while protecting log integrity and sensitive data.
