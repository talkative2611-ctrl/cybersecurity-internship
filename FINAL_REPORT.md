# Cybersecurity Internship — Final Report

**Name:** Talha  
**App:** OWASP NodeGoat  
**Platform:** Kali Linux + VMware  

## 1. Introduction
NodeGoat is an intentionally vulnerable Node.js application used to practice web security. The goal was to find vulnerabilities, fix them, and test the application over 3 weeks.

## 2. Vulnerabilities Found (Week 1)
- XSS on Profile and Contributions pages
- NoSQL Injection on Allocations page
- Information Disclosure in error messages
- Missing HTTP security headers (detected by OWASP ZAP, 21+ vulnerabilities)

## 3. Fixes Applied (Week 2)
- XSS: Sanitized user input using validator library
- Passwords: Confirmed bcrypt hashing
- Sessions: Added JWT for secure session management
- Headers: Added Helmet.js to set secure HTTP headers

## 4. Penetration Testing with Nmap (Week 3)
- Tool: Nmap 7.99
- Target: 127.0.0.1 (localhost)
- Date: 30 May 2026
- Open Port: 4000/tcp (NodeGoat HTTP app)
- Security headers confirmed present: X-Frame-Options, X-XSS-Protection, X-Content-Type-Options
- Result: Only port 4000 exposed, no unnecessary open ports found

## 5. Logging with Winston (Week 3)
Added Winston logging to record security events including application errors and server exceptions. Logs saved to logs/security.log in JSON format with timestamps.

## 6. Conclusion
Over 3 weeks, I identified 5+ vulnerabilities, applied security fixes, ran penetration tests using Nmap, and set up logging. Key learning: security is a continuous process, not a one-time task.
