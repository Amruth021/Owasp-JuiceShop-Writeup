# Juice Shop Write-up: Upload Size Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Improper Input Validation

**Description**

- Upload a file larger than 100 kB.
- Find a way to upload file beyond the size limit enforced by the application's client-side validation.
  
## Solution

- **Testing File Upload** : Upload a random file at `/complain` and intercept the HTTP request using Burp Suite.

- Change the upload size by Replicating the content inside file as many times till its >100KB.

## Remediation

- **Implement Robust Server-Side Validation**: Ensure that all input validations, including file sizes, are re-checked on the server after being submitted.

- **Limit Input Modification**: Use multipart/form-data parsing libraries that strictly enforce total payload sizes, rather than relying on client-side enforcement.
  
