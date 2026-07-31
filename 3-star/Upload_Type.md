# Juice Shop Write-up: Upload Type Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Improper Input Validation

**Description**

- Upload a file that has no .pdf or .zip extension.
- Find a way to upload file that's neither .pdf nor .zip.
  
## Solution

- Upload a random file at `/complain` and intercept the HTTP request using Burp Suite.

- Change the upload file type by Replacing it with any file type.

## Remediation

- **File Type Restrictions**:	Accept only specific formats (.pdf, .zip).

- **Unsupported Format Rejection**:	Reject any file types not in the accepted list.

- **Input Validation**:	Validate file type on client and server sides.
  
