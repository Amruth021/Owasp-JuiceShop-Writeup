# Juice Shop Write-up: Five-Star Feedback Challenge

## Challenge Details

**Difficulty** : ✯✯.\
**Category** : Broken Access Control

**Description**

- Get rid of all 5-star customer feedback.
- This vulnerability allows unauthorized users to access admin functionalities, specifically the ability to manipulate customer feedback.
  
## Solution

- Delete all the 5-star feedback by Going to the `/administration` to solve the Challenge.


## Remediation

- **Restrict Access to Admin Functionality**: Ensure that only authorized admin users can access the admin section of the application. Implement proper authentication checks before allowing access to sensitive URLs, such as `/administration`.

- **Implement Role-Based Access Control (RBAC)**: Define user roles within the application, distinguishing between regular users and admin users. Enforce access controls based on these roles to prevent unauthorized access.

