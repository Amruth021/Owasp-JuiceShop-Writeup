# Owasp Juice Shop Write-up: Score Board Challenge

## Challenge Overview

**Title:** Score Board\
**Category:** Miscellaneous\
**Difficulty:** ⭐ (1/6)

## Challenge Description

This challenge requires to find a **Score Board** page within the site. The solution for this challenge involves analyzing the JavaScript code of the application to find the route to the hidden Score Board page.

## Tools Used

- Developer Tools for viewing JavaScript source code

## Step-by-Step Solution

Here are the step-by-step details:

1. **Access Developer Tools**: Open the developer tools in the web browser while interacting with the application.
2. **Review JavaScript Files**: Navigate to the the `main.js` by Right Click > View Page Source.
3. **Analyze main.js**: Focus on the `main.js` file, as it often contains main route definitions and application logic.
4. **Search for Hidden Routes**: Searched within the `main.js` file for mentions of various application route including the "Score Board".
5. **JS Beatify**: Use a JavaScript Beautifier for a clearer code analysis.

<img src="../images" alt="scoreboard" width="500px">
6. **Access the Score Board**: Use the found route in the `main.js` by to entering the path in the browser's address bar.

## Remediation

None :).
