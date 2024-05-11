# Technical Report: Ethical Hacking Assessment

**Date:** May 11, 2024  
**Client:** SoleAce E-Commerce Website  
**Prepared by:** Mark Vincent M. Cleofe and Lyme G. Lavarias

## Executive Summary:

In accordance with the scope of work outlined, Cleofe and Lavarias conducted an ethical hacking assessment on the network infrastructure and web applications of SoleAce. The assessment aimed to identify potential vulnerabilities and provide recommendations for remediation to enhance the security posture of the organization. The assessment revealed several critical and high-severity vulnerabilities across various systems and applications. This report presents a summary of the findings and provides actionable recommendations for remediation.

## Findings:

1. **SQL Injection (Critical):**

   - Identified in the login form of the internal employee portal.
   - Attackers can exploit this vulnerability to gain unauthorized access to sensitive information stored in the database.

2. **Cross-Site Scripting (XSS) (High):**
   - Discovered in the customer-facing web application's feedback form.
   - Allows attackers to inject malicious scripts into web pages viewed by other users.
3. **Outdated Software (High):**

   - Found on several servers running outdated versions of operating systems and software packages.
   - Increases the risk of exploitation due to unpatched vulnerabilities.

4. **Weak Password Policy (High):**

   - Observed weak password policies across user accounts in the Active Directory.
   - Increases the risk of unauthorized access through brute-force attacks.

5. **Missing Security Headers (Medium):**

   - Absence of security headers such as Content-Security-Policy (CSP) and X-Content-Type-Options in HTTP responses.
   - Increases the risk of various web-based attacks, including XSS and clickjacking.

6. **Unrestricted File Upload (Medium):**

   - Discovered in the file upload functionality of the internal document management system.
   - Allows attackers to upload and execute malicious files on the server.

7. **Sensitive Data Exposure (Medium):**

   - Found sensitive data, including plaintext passwords, stored in configuration files on the web server.
   - Increases the risk of data breaches and unauthorized access.

8. **Insecure Direct Object References (IDOR) (Medium):**
   - Identified in the URL parameters of the online shopping cart application.
   - Allows attackers to manipulate object references to access unauthorized resources.
9. **Insecure Deserialization (High):**
   - Discovered in the payment processing module of the e-commerce website.
   - Allows attackers to manipulate serialized objects to execute arbitrary code or perform unauthorized actions.
10. **Cross-Site Request Forgery (CSRF) (Medium):**
    - Identified in the administrative interface of the content management system (CMS).
    - Allows attackers to trick authenticated users into performing unintended actions on behalf of the victim.

## Recommendations:

1. **SQL Injection:** Implement parameterized queries or prepared statements to sanitize user inputs and prevent SQL injection attacks. Regularly update and patch database management systems.
2. **Cross-Site Scripting (XSS):** Implement input validation and output encoding to sanitize user inputs and prevent XSS attacks. Utilize Content Security Policy (CSP) headers to mitigate the impact of XSS vulnerabilities.
3. **Outdated Software:** Establish a patch management process to regularly update and apply security patches to all systems. Utilize vulnerability scanning tools to identify and prioritize patching of critical vulnerabilities.
4. **Weak Password Policy:** Enforce strong password policies, including minimum length, complexity requirements, and regular password expiration. Implement multi-factor authentication (MFA) to add an additional layer of security.
5. **Missing Security Headers:** Configure web servers to include appropriate security headers in HTTP responses to mitigate common web-based vulnerabilities. Regularly review and update security header configurations based on best practices.
6. **Unrestricted File Upload:** Implement file type validation and content verification to restrict the types of files that can be uploaded. Store uploaded files in a secure location outside the web root directory to prevent direct execution.
7. **Sensitive Data Exposure:** Encrypt sensitive data at rest using strong encryption algorithms. Avoid storing sensitive information such as passwords in plaintext and utilize secure storage mechanisms such as hashed passwords with salt.
8. **Insecure Direct Object References (IDOR):** Implement access controls and proper authorization mechanisms to restrict access to resources based on user privileges. Validate user input to prevent tampering with object references.
9. **Insecure Deserialization:** Implement input validation and integrity checks on serialized objects to prevent malicious manipulation. Utilize secure deserialization libraries and frameworks to mitigate the risk of insecure deserialization vulnerabilities.
10. **Cross-Site Request Forgery (CSRF):** Implement anti-CSRF tokens and mechanisms to validate the origin and integrity of incoming requests. Utilize SameSite cookies to mitigate the risk of CSRF attacks targeting authenticated sessions. Additionally, educate users about the importance of verifying actions before executing them to prevent CSRF exploitation.

## Conclusion:

The ethical hacking assessment conducted by Cleofe and Lavarias has identified critical vulnerabilities within the network infrastructure and web applications of SoleAce. Addressing these vulnerabilities through the implementation of recommended remediation measures is essential to enhance the organization's security posture and mitigate the risk of potential cyber-attacks. Regular security assessments and proactive security measures are recommended to maintain a robust defense against evolving threats.

## Disclaimer:

This report is intended solely for the use of SoleAce and should not be disclosed to any third party without prior consent from Cleofe and Lavarias. The findings and recommendations provided are based on the assessment conducted at the time of evaluation and may not reflect the current state of security vulnerabilities. Cleofe and Lavarias disclaims any liability for damages arising from the use or implementation of the recommendations outlined in this report.

## Signature:

**_Mark Vincent Cleofe's Signature:_** ![Cleofe's Signature](/img/cleofe-esig.jpeg)

**_Lyme Lavarias' Signature:_** ![Lavarias' Signature](/img/lyme-esig.jpeg)
