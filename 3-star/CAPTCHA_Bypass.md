# Juice Shop Write-up: CAPTCHA Bypass Challenge

## Challenge Details

**Difficulty** : ✯✯✯.\
**Category** : Broken Anti Automation

**Description**

- Submit 10 or more customer feedbacks within 20 seconds.

  
## Solution

- Use Burp Suite to intercept the HTTP POST request made when submitting feedback.

- Since CAPTCHA validation in the request relies solely on the captchaId and the provided captcha answer. This allows the reuse of a single CAPTCHA solution multiple times.

- Send it to repeater and send multiple request to solve the Challenge

## Solution Explained

This Challenge highlights the failure in the application’s anti-automation logic, as it should ideally track and validate each CAPTCHA attempt individually to prevent abuse.

## Remediation

- **CAPTCHA Robustness**: Implement CAPTCHA systems that track attempts and ensure each CAPTCHA challenge is only valid for one submission.
  
- **Enhance CAPTCHA Logic**: Consider using more sophisticated CAPTCHA solutions like reCAPTCHA, which includes advanced risk analysis.
  
- **Rate Limiting**: Introduce rate limiting for form submissions to reduce the risk of automated attacks.

  
