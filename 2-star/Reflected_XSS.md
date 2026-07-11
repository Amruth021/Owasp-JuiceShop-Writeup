# Juice Shop Write-up: Reflected XSS Challenge

## Challenge Details

**Difficulty** : ✯✯.\
**Category** : XSS

**Description**

- Perform a reflected XSS attack with <iframe src="javascript:alert(`xss`)">.
- Reflected XSS is a type of cross-site scripting vulnerability where the injected script is reflected off the web server without being stored.
  
## Solution

- **Initial Testing**: Start by testing a basic XSS payload in search bar paramater `q`, While this payload works fine it doesnt match challenge requirement since it wasnt reflected back on page.
    
- **Find a Reflective Surface**: Place an order and Go to the order history and Click "Track order", This will present an reflective surface with an `id` parameter.

- **Injecting Payload**: By navigating to the URL with the crafted payload, The payload will get reflected leading to execution of JS code.

  <img src=".." alt="code image" width="500px">

## Remediation

- **Input Validation**:	Check user inputs against predefined rules to block malicious data.
  
- **Context-Sensitive**: Output Encoding	Encode user inputs based on their context in the HTML document.
  
- **Content Security Policy (CSP)**:	Define trusted content sources to prevent unauthorized script execution.
  
