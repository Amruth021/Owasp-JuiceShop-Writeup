# Juice Shop Write-up: Privacy Policy Inspection Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Security through Obscurity

**Description**

- Prove that you actually read our privacy policy.
- Challenge requires to you be familiar with privacy policy by uncovering hidden elements or messages within the policy document.
  
## Solution

- **Identifying Hidden Triggers** : During the examination hovering over certain words in the policy triggers a glow effect on it which reveals it to be hidden messages.

- Piece together these words to form a chain of path might indicate a hidden URL or document which will lead to a error message which include another path specifically navigate to
- `/juice-shop/frontend/dist/frontend/assets/private/thank-you.jpg` as hint and accessing this solves the challenge.

  
