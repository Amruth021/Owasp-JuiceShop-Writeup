# Juice Shop Write-up: Password Strength Challenge

## Challenge Details

**Difficulty** : ✯✯.\
**Category** : Broken Authentication

**Description**

- Log in with the administrator's user credentials without previously changing them or applying SQL Injection.
- To use Bruteforce and find Admin password.
  
## Solution

- **Intercept Login Request**: Attempted to log in with the administrator email and a random password and Intercept the Request in Burp. (Admin mail can be found on one of the product reviews)
    
- **Setup for Brute Force**: Configure Burp Suite's Intruder mode to use a list of common passwords.

  <img src=".." alt="code image" width="500px">

- Got The Pass!.

## Remediation

- **Implement Strong Password Policies**:	Enforce minimum password lengths (at least 13-16 characters) and complexity requirements.
  
- **Use Multi-Factor Authentication (MFA)**:	Add an extra layer of security beyond just passwords to protect accounts.

- **Regularly Update Password Policies**:	Review and update password policies to adapt to evolving security threats and best practices.
  
