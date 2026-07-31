# Juice Shop Write-up: Deluxe Fraud Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Improper Input Validation

**Description**

- Obtain a Deluxe Membership without paying for it.
- This challenge highlights vulnerabilities related to improper input validation in the application.
  
## Solution

- **Find Vulnerable Endpoint** : Access the Deluxe Membership page and proceed for the payment of membership request. Analyze the request and response in burp.

- **Modifying Payment Details** : Experiment with various modifications to `paymentMode` and `paymentId` to bypass the actual payment verification process.

- **Bypassing Payment** : Set `paymentMode` to "none" and `paymentId` to a random or non-existent value to test if the application logic improperly validates these inputs. And it does.
  
## Solution Explanation
The challenge was completed by identifying weakness in the payment for membership processes of the web application. By this it was possible to simulate a successful transaction without fulfilling the usual payment requirements.


## Remediation

- **Enhance Input Validation**: Ensure that all inputs, especially those related to payment operations, are rigorously validated both on the client-side and server-side.

- **Secure Payment Logic**: Implement robust checks on the server-side to verify that payment details are correct and complete before processing transactions.

- **Use Secure Payment Gateways**: Integrate with reputable payment gateways that provide additional security checks and validations.

