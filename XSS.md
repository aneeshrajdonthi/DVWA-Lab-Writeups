# Cross-Site Scripting (XSS) in DVWA

In this section, I demonstrate how I exploited **Cross-Site Scripting (XSS)** in **DVWA**. XSS occurs when an attacker injects malicious scripts into web pages that are then executed by the victim's browser.

## Objective
The goal was to trigger a pop-up alert using a simple XSS payload.

## Steps to Exploit

1. **Identify Vulnerability**:  
   I navigated to the **XSS** section in DVWA after setting the security level to **low**. The form was designed to accept user input without proper validation.

2. **Inject Payload**:  
   I injected the following XSS payload in the input field to trigger a pop-up alert:
   ```html
   <script>alert('XSS triggered');</script>
