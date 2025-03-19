# Clickjacking-

Affected Domain(s): console.hivemq.cloud

POC File:https://drive.google.com/file/d/1WDZ0yxcvzwVDkJ2fRk9VwuznBxHAzyOz/view?usp=sharing


Summary: A clickjacking vulnerability has been identified on the website across all endpoints. Clickjacking allows an attacker to deceive a user into clicking on a disguised or hidden element, potentially leading to unintended actions or disclosure of sensitive information.

Description: The identified vulnerability on the website presents a serious clickjacking risk across all its endpoints. Clickjacking, also known as UI redressing, is a malicious technique where attackers overlay deceptive elements or pages on top of legitimate content, tricking users into clicking on unintended actions.

Steps to reproduce: 
1. Download the POC and open the FILE.
 2. Observe that the clickjacking is possible and being framed, confirming the vulnerability.







Suggested Fix: - X-Frame-Options Header: Set the X-Frame-Options header to DENY or SAMEORIGIN to prevent the website from being embedded in an iframe on other domains.
 - Content Security Policy (CSP): Implement a Content Security Policy with appropriate directives, including frame-ancestors, to control which domains can embed the website.
 - Frame-Busting Script: Use frame-busting JavaScript techniques to prevent the website from being loaded within an iframe


Impact: - Fraudulent Actions: Attackers can trick users into performing actions that are against their interests, such as making unauthorized transactions or revealing sensitive information.
 - Phishing and Social Engineering: Clickjacking can facilitate phishing attacks by creating deceptive interfaces that appear legitimate to users. 
- Reputation Damage: Successful exploitation of clickjacking can damage the reputation of the website and erode user trust.
