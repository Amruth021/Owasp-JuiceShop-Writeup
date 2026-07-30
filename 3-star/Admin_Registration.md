# Juice Shop Write-up: Admin Registration Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Improper Input Validation

**Description**

- Register as a user with administrator privileges.
- This challenge highlights significant vulnerabilities that allows user to gain administrator privileges through a specific manipulation of the registration process.
  
## Solution

- **Register a new user** : Go to the registration page and register a new user.

- **Intercept** : Intercept the request thru burp proxy and examine the HTTP request sent to the server.

-   <img src="../images/3-star/.png" alt="code image" width="500px">

- The response for registration of has a user role defined, change the role to admin and add it to request to complete the challenge.

## Solution Explained

This challenge demonstrates an improper input validation flaw within the registration process. By modifying the user role in the registration request, it was possible to bypass the application's normal security measures and grant administrative privileges to a newly created account.


## Remediation

- Ensure that roles are assigned based on predefined criteria.

- Implement server-side checks to validate the role before granting access.

- Use strict data types and formats for each field to prevent manipulation.

- Implement robust server-side logic to handle role assignments and permissions.

