# Juice-Shop Write-up: Bonus Payload

## Challenge Overview

**Title:** Bonus Payload\
**Category:** Cross-Site Scripting (XSS)\
**Difficulty:** ⭐ (1/6)

## Challenge Description

Use the bonus payload <iframe width="100%" height="166" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/tracks/771984076&color=%23ff5500&auto_play=true&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe> in the DOM XSS challenge.

The provided SoundCloud iframe payload. If the music player appears on the page, it means the website is accepting and displaying HTML from user input.

### Step-by-Step Solution

1. **Encode the Payload**:
   - The complete URL with the injected payload looked like this: `http://[IP:PORT]/#/search?q=%3Ciframe%20width%3D%22100%25%22%20height%3D%22166%22%20scrolling%3D%22no%22%20frameborder%3D%22no%22%20allow%3D%22autoplay%22%20src%3D%22https:%2F%2Fw.soundcloud.com%2Fplayer%2F%3Furl%3Dhttps%253A%2F%2Fapi.soundcloud.com%2Ftracks%2F771984076%26color%3D%2523ff5500%26auto_play%3Dtrue%26hide_related%3Dfalse%26show_comments%3Dtrue%26show_user%3Dtrue%26show_reposts%3Dfalse%26show_teaser%3Dtrue%22%3E%3C%2Fiframe%3E`

2. **Execute the Attack**:
   - By navigating to the manipulated URL, the iframe successfully rendered within the web application, embedding the SoundCloud player with a song as intended.


## Remediation

- Validate and whitelist trusted sources if embedded content (e.g., iframes) is necessary.
- Implement a strong Content Security Policy (CSP) to reduce the impact of XSS.
- Prefer creating DOM elements programmatically (createElement, setAttribute) instead of injecting raw HTML.
