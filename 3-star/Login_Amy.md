# Juice Shop Write-up: Login Amy Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Sensitive Data Exposure

**Description**

- Log in with Amy's original user credentials. (This could take 93.83 billion trillion trillion centuries to brute force, but luckily she did not read the "One Important Final Note")
- OSINT.
  
## Solution

- **Futurama Reference**: Hint: Amy Wong, a character from Futurama, dates a character named Kif Kroker. Knowing this relationship provides a clue that "Kif" could be part of her password.

- By searching the time it takes to crack password you can find a hint of password format : `D0g.....................`, Using this and above hint the password can be found.


## Remediation

- **Educate Users on Password Security**: Inform users about creating strong, memorable passwords that do not simply rely on predictable patterns or easily guessed cultural references.

- **Implement Rate Limiting and Account Lockout Mechanisms**: Prevent brute force attacks by limiting the number of failed login attempts.

- **Use Multi-Factor Authentication (MFA)**: Enhance security by requiring additional verification beyond just a password.

  
