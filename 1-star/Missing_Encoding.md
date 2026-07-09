# Juice Shop Write-up: Missing Encoding Challenge

## Challenge Details

**Difficulty** : ✯.\
**Category** : Improper Input Validation

**Description**

- Retrieve the photo of Bjoern's cat in "melee combat-mode".
- Missing Encoding refers to a vulnerability where certain characters, like the hash symbol (#), are not properly encoded in URLs, which can lead to issues such as failure to retrieve resources.

## Solution

- **Identify the Issue**: Navigate to the Photo wall section of the site, There you will find a photo not displayed properly due to improper encoding of special characters.
  
  <img src=".." alt="code image" width="500px">
  
- **In Detail**: Improper encoding in the `src` atribute resulted in the image not processed correctly.
  
  <img src="../assets/difficulty1/missing_encoding_1.png" alt="code image" width="500px">
  
- **Fix**: Encode the `#` Character and replace it with in the src atribute using inspect element option

## Remediation

- Properly sanitize output data to prevent issues like these and ensure that all user input is correctly encoded before being displayed or transmitted.
- Utilize context-specific validation to handle data appropriately based on its intended use.
