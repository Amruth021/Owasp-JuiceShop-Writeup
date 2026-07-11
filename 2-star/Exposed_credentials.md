# Juice Shop Write-up: Exposed credentials Challenge

## Challenge Details

**Difficulty** : ✯✯.\
**Category** : Sensitive Data Exposure

**Description**

- A developer was careless with hardcoding unused, but still valid credentials for a testing account on the client-side.
- Find the hardcoded credentials leaked by developer by mistake on client-side code.
  
## Solution

- **Search Source Files**: Search through source code files using developer options, Don't overlook the main file in any challenges.
    
- **Locate Hardcoded Creds**: Search through files using specific keywords that could fasten the search
  
```
credentials
password
login
@juice-sh.op
```

- **Use the Creds**: Login using the found Credentials to complete the challenge.

  <img src=".." alt="code image" width="500px">

## Remediation

- **Avoid Hardcoding Secrets**:	Never store sensitive information like API keys or passwords directly in the application code.

- **Use Secure Storage Mechanisms**:	Implement secure storage solutions for user secrets, such as secure storage APIs.
  
- **Rotate Credentials Regularly**:	Regularly change credentials to minimize the impact of any potential exposure.
  
