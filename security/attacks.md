# Web Attacks


## What is Cross-site request forgery (CSRF) attack?
A web security vulnerability that allows an attacker to induce users to perform actions that they do not intend to perform.

### How it works?
Attackers create a fake website or send email including malicious request to victims
```
<iframe height="0" width="0" src="https://vulnerable-website.com/email/change?email=pwned@evil-user.net">
```

### How to prevent?
For critical tasks
- Includ a CSRF token generated based on session tokens
- Demand re-authenticate


## What is cross-site scripting (XSS) attack?
A client-side code injection attack. 
that allows an attacker to compromise the interactions that users have with a vulnerable application.

### How it works?
Attacker attaches code onto a legitimate website that will execute when the victim loads the website.

1. Attacker sends an email including script-injected link to victim
2. The victim loads a webpage and the malicious code copies the user’s cookies
3. The code then sends an HTTP request to an attacker’s webserver with the stolen cookies.
4. The attacker can then use those cookies to impersonate the user on that website

### How to prevent?
- Validating inputs
