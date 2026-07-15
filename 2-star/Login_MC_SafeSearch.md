# Juice Shop Write-up: Login MC SafeSearch Challenge

## Challenge Details

**Difficulty** : ✯✯.\
**Category** : Sensitive Data Exposure

**Description**

- Log in with MC SafeSearch's original user credentials without applying SQL Injection or any other bypass.
- Find MC Safesearch password using OSINT.
  
## Solution

- Search about username of the user led to discovering a video by a rapper who discusses passwords in one of his song.

- The rapper mentioned a unique naming convention for his password involving his pet named Mr. Noodles, with modifications to replace certain letters with numbers.

- `Mr. N00dles` was used to login successfully 


## Remediation

- **Stronger Password Policies**: Implement and enforce policies that discourage the use of easily guessable passwords, even if they include number substitutions for letters.
  
- **Education and Awareness**: Train users on the importance of using non-predictable passwords that do not relate directly to publicly known information about them, such as pet names, favorite movies, etc.
  
- **Use of Multi-Factor Authentication (MFA)**: Adding an additional layer of security with MFA can significantly reduce the risk of unauthorized access, even if a password is compromised or guessed.
