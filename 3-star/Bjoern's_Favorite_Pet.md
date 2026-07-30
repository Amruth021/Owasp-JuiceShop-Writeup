# Juice Shop Write-up: Bjoern's Favorite Pet Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Broken Authentication

**Description**

- Reset the password of Bjoern's OWASP account via the Forgot Password mechanism with the original answer to his security question.

  
## Solution

- Accessed the administrative panel of the application to obtain Bjoern’s email address.

- Use Bjoern’s email address to find his social media profiles and Locate his Twitter account.

- On his account you will find a post featuring a picture of his cat named `Zaya`.

-   <img src="../images/3-star/.png" alt="code image" width="500px">


## Remediation

- **Use of Non-Personal Security Questions**: Encourage or enforce the use of security questions that do not rely on information that could easily be obtained or guessed through public data. Note that it's better to not use security question but rather send email when user want to reset his password.

- **Privacy Settings**: Advise users to utilize privacy settings on social media platforms to control who can see their posts, especially when sharing personal or potentially sensitive information.

