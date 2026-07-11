# Juice Shop Write-up: Login Admin Challenge

## Challenge Details

**Difficulty** : ✯✯.\
**Category** : Injection

**Description**

- Log in with the administrator's user account.
- This challenge involves exploiting an SQL Injection vulnerability in login panel to access administrator account.
  
## Solution

- **Exploit**: Use of classic SQL injection test payload `' or 1=1--`.

    <img src=".." alt="code image" width="500px">
  
- **Admin Login**: Just using the payload will land you on admin account.

## Explanation

-SQL query used in the login in this case could be looking like this.

`"SELECT * FROM Users WHERE email = ''' AND password = '698d51a19d8a121ce581499d7b701668' AND deletedAt IS NULL"`

here,

  `'` character close the email string.
  `OR` is a SQL query
  `1=1` is TRUE in boolean value
  `--` will comment out the SQL query after the TRUE


So, now the SQL will check for email = '' or true which is always a TRUE statement this will log us as the first user in the database which is `admin` in most cases.

## Remediation

- **Parameterized Queries**:	Separates SQL code from user input to prevent injection.
  
- **Input Validation**:	Ensures only valid data formats are accepted.

- **Least Privilege Access Control**:	Limits database permissions to reduce potential damage from attacks.
  
