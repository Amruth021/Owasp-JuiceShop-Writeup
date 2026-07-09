# Juice Shop Write-up: Zero Stars Challenge

## Challenge Details

**Difficulty** : ✯.\
**Category** : Improper Input Validation

**Description**

- Give a devastating zero-star feedback to the store.
- This Challenge highlights improper input validation Which allows users to exploit the system's vulnerabilities, demonstrating how easily feedback can be manipulated.
  
## Solution

- **Interception**: Configure Burp Suite to intercept the HTTP requests using Proxy functionnality.
    
- **Submit Review & Modify:**: Attempt to submit a review normally through the website's interface, Modify the Request by Altering the ratings parameter in the intercepted request to 0, despite the website originally not allowing a zero-star rating to be submitted through its user interface.

  <img src=".." alt="code image" width="500px">

- Send the modified request to the server, successfully submitting a zero-star review.

## Remediation

- **Input Validation**: Ensure that all user inputs are properly validated to prevent malicious entries.

- **Security Measures**: Regularly review and update security protocols to protect against vulnerabilities that could lead to negative user experiences. 
