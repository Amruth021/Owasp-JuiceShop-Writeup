# Juice Shop Write-up: Forged Review Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Broken Access Control

**Description**

- Post a product review as another user or edit any user's existing review.
- This challenge involves manipulating the review submission process in a web application to post reviews as another user.
  
## Solution

- **Identifying the Vulnerability** : Submit a generic review through the web application's interface and Intercept the Request.

- From analyzing request parameters  the request payload includes an "author" parameter, which appears to manually set the author of the review which makes it vulnerable to forged review.

- **Exploiting**: Modify the author parameter to another user's name or identifier and resend the request to solve the challenge.

## Remediation

- **Strict Server-Side Validation**: Ensure that the server validates that the user making the request is the owner of the account or content being modified. This can involve checking session tokens against user IDs.

- **Use Secure Session Handling**: Implement robust session management that securely associates users with their actions and prevents parameter manipulation.

- **Role-Based Access Control**: Enforce access controls that verify a user's role and permissions before allowing modifications to data.

