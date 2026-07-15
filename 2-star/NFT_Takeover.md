# Juice Shop Write-up: NFT Takeover Challenge

## Challenge Details

**Difficulty** : ✯✯.\
**Category** : Sensitive Data Exposure

**Description**

- Take over the wallet containing our official Soul Bound Token (NFT).
- This challenge involves exploiting a vulnerable wallet integration to gain control of an NFT.
  
## Solution

- The application's JavaScript files will lead in finding any references to "NFT," leading to the discovery of the /juicy-nft path

- Upon Visiting the site will be prompted for a private key to access the NFT wallet.

- Find a specific user feedback comment to find a seed phrase of password and Use a Mnemonic converter tool to change it to private key.

- Enter the derived private key on the NFT page, which will authenticate access to the wallet containing the Soul Bound Token.

## Remediation

- **Secure Private Key Storage**:	Ensure that private keys are stored securely, using encryption and secure access controls.
  
- **Implement Access Controls**:	Enforce strict access controls to limit who can access and manage wallet functionalities.
  
- **Regular Security Audits**:	Conduct regular audits of the wallet integration to identify and fix potential vulnerabilities.
