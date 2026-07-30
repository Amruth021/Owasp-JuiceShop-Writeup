# Juice Shop Write-up: Client-side XSS Protection Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : XSS

**Description**

- Perform a persisted XSS attack with `<iframe src="javascript:alert(`xss`)">` bypassing a client-side security mechanism.

    
## Solution

- **Endpoint** : Using the prev challenges as reference, the `/register` page is vulnerable due to improper input validation

- Intercept the request and paste the payload in email parameter and change the Content-Type to `application/json`.

## Solution Explanation 
Due to improper input validation the attack string or payload is rendered as harmless text. (Client-side security mechanism) - The adminstration page renders xss payload in the administration page.

## Remediation

- **Input Validation**: Ensure that all user inputs are validated before being processed. This helps in identifying and rejecting potentially harmful data.
  
- **Output Encoding**: Encode data before rendering it in the browser. This prevents the browser from interpreting it as executable code.
  
- **Content Security Policy (CSP)**: Implement a CSP to restrict the sources from which scripts can be loaded. This adds an additional layer of security against XSS attacks.

  
