# Juice Shop Write-up: Weird Crypto Challenge

## Challenge Details

**Difficulty** : ✯✯.\
**Category** : Cryptographic Issues

**Description**

- Inform the shop about an algorithm or library it should definitely not use the way it does.
- This challenge demonstrates insecure cryptographic practices.

    
## Solution

- Open Complaint / Feedback Section.

- Enter a message mentioning insecure MD5 hashing.

## Remediation

- **Update Hashing Algorithms**: Replace MD5: MD5 is outdated and insecure. Use stronger hashing algorithms such as bcrypt and Argon2

- **Implement Salting**: Salt Passwords: Ensure that all passwords are salted before hashing. This adds a unique value to each password, making it more resistant to attacks.

- **Key Management**: Avoid Hard-Coded Secrets: Do not use hard-coded secrets in your code. Instead, implement proper key management practices to secure sensitive information.

  
- **Educate Development Teams**:	Train developers on secure coding practices to prevent future vulnerabilities.
  
