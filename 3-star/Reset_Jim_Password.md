# Juice Shop Write-up: Reset Jim's Password Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Broken Authentication

**Description**

- Reset Jim's password via the Forgot Password mechanism with the original answer to his security question.
  
## Solution

- **Identifying Jim's Identity**: Given that the challenge hint refers to Jim as a celebrity whose answer to his security question can be found publicly and In a comment Jim quote's a line from Star Trek.

- Googling Jim Star Trek reveals the character and you can find the security question answer in wikipedia.


## Remediation

- **Choose Robust Security Questions**: Avoid questions where answers are easily guessed or found. Use questions that have safe, unpredictable answers. If possible, remove security question and replaces them by an email sended to users when they want to reset their password.

- **Educate Users**: Guide users in selecting security questions and answers that are secure, emphasizing the risk of using easily accessible information.

- **Implement Multiple Authentication Factors**: Enhance security by requiring multiple methods of authentication beyond security questions.
  
