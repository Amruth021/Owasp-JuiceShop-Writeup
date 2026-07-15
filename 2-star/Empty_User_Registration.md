# Juice Shop Write-up: Empty User Registration Challenge

## Challenge Details

**Difficulty** : ✯✯.\
**Category** : Improper Input Validation

**Description**

- Register a user with an empty email and password.
- This challenge tests the robustness of the application's user input validation mechanisms.
  
## Solution

- Register a dummy user and Intercept the request with burp.

- Change the user email and password to null or just space value.

  <img src=".." alt="code image" width="500px">

- This resulted in the server processing the request without these fields, leading to the creation of a Empty user with no email and password.

    <img src=".." alt="code image" width="500px">


## Remediation

- **Require Valid Inputs**: Ensure that the registration form mandates valid email and password entries. Users should not be able to submit the form with empty fields.

- **Implement Server-Side Validation**: Validate all input data on the server side to ensure that no empty or null values are accepted during the registration process. Reject any registration attempts that do not meet the criteria for valid email and password inputs.

