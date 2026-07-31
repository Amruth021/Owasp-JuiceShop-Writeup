# Juice Shop Write-up: Manipulate Basket Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Broken Access Control

**Description**

- Put an additional product into another user's shopping basket.
- Challenge involves adding an item to another user's shopping basket by exploiting potential IDOR vulnerability in the application.
  
## Solution

- **Request Manipulation** : Intercept the request after adding a product to basket and notice that the basket ID (BasketId) is included in the request body, indicating a potential vector for IDOR.

- Send a manipulated request that adds product to another basket and receive a successful response.

  
## Remediation

- **Ensure Proper Parameter Handling**: Servers should be designed to handle unexpected, duplicated, or out-of-order parameters securely.

- **Implement Robust Access Controls**: Ensure that all sensitive operations verify the user's permission to perform the action on the specified resource.

  
