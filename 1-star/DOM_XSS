# Juice-Shop Write-up: DOM XSS

## Challenge Overview

**Title:** DOM XSS\
**Category:** Cross-Site Scripting (XSS)\
**Difficulty:** ⭐ (1/6)

DOM XSS (Document Object Model Cross-Site Scripting) is a type of security vulnerability where an attacker injects malicious scripts into a web page, and these scripts are executed in the user's browser without involving the server.
**Which Means the request never reaches the server**

## Challenge Description

Perform a DOM XSS attack with <iframe src="javascript:alert(`xss`)">.

### Step-by-Step Solution

1. **Identify the Entry Point**:
   - The application's search functionality was identified as a possible vector for XSS attacks. The search parameter `q` in the URL can be used to manipulate the DOM.

2. **Payload**:
   - The XSS payload suggested in description was: `<iframe src="javascript:alert(`xss`)">`. This script is designed to execute JavaScript directly from the iframe source attribute, triggering an XSS alert.

3. **Encode and Inject the Payload**:
   - The payload will be URL-encoded using burp to bypass basic URL parsing and injected into the application via the search URL: `http://[IP:PORT]/#/search?q=%3Ciframe%20src=%22javascript:alert(%60xss%60)%22%3E`

4. **Execute the Attack**:
   - The resulted URL in the execution of the malicious script will display an alert box indicating a successful XSS attack.

   <img src="../images/" alt="alt text" width="500px">


This challenge was solved by injecting and executing a JavaScript code through an iframe's source attribute in a URL parameter that influences the DOM. This was a classic case of DOM-based XSS where user input directly affects the DOM without proper sanitization.

## Remediation
- Implement a strong Content Security Policy (CSP) to reduce XSS impact.
- Keep JavaScript libraries and frameworks up to date to address known XSS vulnerabilities.
- Perform regular security testing using static analysis, dynamic testing, and manual code reviews.
