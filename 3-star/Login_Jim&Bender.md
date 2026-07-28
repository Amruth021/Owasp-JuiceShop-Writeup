# Juice Shop Write-up: Login Jim/Bender Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Injection

**Description**

- Log in with Jim's and Bender user account..
- Find Jim's email perform SQLi and login as jim/Bender.
  
## Solution

- For both account email id's you can find it from administration section or can be seen email format in the reviews of the products.

- `jim@juice-sh.op' --` .

- Above input in email field will bypass the password verification by commenting the rest of the query after `--` and logs in as jim

## Remediation

- **Input Validation**: Ensure all user inputs are validated and sanitized.
  
- **Parameterized Queries**: Use parameterized queries to separate data from commands.

- **Regular Security Testing**: Conduct thorough testing to identify and fix vulnerabilities.
  
