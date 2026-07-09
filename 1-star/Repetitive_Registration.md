# Juice Shop Write-up: Repetitive Registration Challenge

## Challenge Details

**Difficulty** : ✯.\
**Category** : Improper Input Validation

**Description**

- Follow the DRY principle while registering a user.
- The DRY principle, which stands for "Don't Repeat Yourself," emphasizes reducing repetition.
- It suggests that the registration process should avoid unnecessary duplication of data, such as requiring the same information multiple times, to enhance security and efficiency.

## Solution

- **Identify the Issue**: Navigate to the user regitration and register a user and capture the request in burp. 
    
- **Exploit**: When the contents of the password repeat field Modified to “Nothing” and submitted solves the challange.

  <img src=".." alt="code image" width="500px">

- **Why it works**: If the client-side forms validate that the passwords match, there isn’t really a reason to send both pieces of data to the server. It’s not useful for anything and just adds to your attack surface.

## Remediation

-  Implementing strict syntactic and semantic validation on all inputs.
-  Using allowlist-based validation for fields like email formats.
-  Performing server-side checks even when client-side validation exists.
