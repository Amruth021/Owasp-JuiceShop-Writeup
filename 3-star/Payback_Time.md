# Juice Shop Write-up: Payback Time Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Improper Input Validation

**Description**

- Place an order that makes you rich.
- Find a way to make financial gain through manipulating product pricing in the site.
  
## Solution

- During checkout make the the quantity in negative value.

## Remediation

- **Proper Input Validation**: Ensure that all inputs, especially those related to financial transactions, are validated both client-side and server-side to prevent manipulation.

- **Use Prepared Statements for SQL**: Avoid SQL injection by using prepared statements with parameterized queries.
  
  
