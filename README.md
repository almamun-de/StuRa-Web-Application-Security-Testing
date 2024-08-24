# Security Testing of StuRa Web Application

## Overview
This project documents the security analysis conducted on the StuRa web application, which serves as a platform for student interactions at Brandenburg University of Technology. The analysis involved a comprehensive assessment to identify potential vulnerabilities that could compromise the confidentiality, integrity, and availability of sensitive student information and operational functionalities.

## Project Members
- Abdullah Almamun
- Giyosiddin Abdumalikov

## Objectives
The primary objectives of this security analysis were:
- To identify potential vulnerabilities in the StuRa web application.
- To assess the current security posture using static code analysis, dynamic testing, and threat modeling.
- To provide actionable recommendations to mitigate identified vulnerabilities and strengthen the overall security framework.

## Scope of Analysis
- **Web Application**: The assessment included the StuRa web application hosted at `http://localhost:8000`.
- **Email Services**: Evaluation of the email services hosted at `http://localhost:8025`.

## Methodologies
### 1. Threat Modeling
Threat modeling was conducted using the STRIDE framework, focusing on identifying and mitigating threats related to Spoofing, Tampering, Repudiation, Information Disclosure, Denial of Service, and Elevation of Privilege.

### 2. Static Code Analysis
- **Tool Used**: Snyk
- **Objective**: To analyze the source code for vulnerabilities such as SQL injection, Cross-Site Scripting (XSS), and other coding flaws.
- **Key Findings**: The static analysis identified potential vulnerabilities in third-party libraries and code quality issues.

### 3. Dynamic Testing
- **Tools Used**: OWASP ZAP, Burp Suite, Nessus
- **Objective**: To perform runtime vulnerability scanning, detect security misconfigurations, and simulate real-world attack scenarios.
- **Key Findings**:
  - OWASP ZAP detected medium and low-severity issues, including `.htaccess` information leaks, missing CSP headers, and clickjacking vulnerabilities.
  - Burp Suite corroborated these findings and identified additional informational alerts.
  - Nessus identified vulnerabilities related to PHP version disclosure and missing security headers.

### 4. Penetration Testing
- **Objective**: To simulate attacks on the StuRa application and identify potential security weaknesses.
- **Tools Used**: Kali Linux tools, Dirb, Nikto, Wapiti
- **Key Findings**: No critical vulnerabilities were found. Most issues identified were informational or low severity, indicating a robust security posture.

## Summary of Findings
- **Threat Modeling**: Identified potential threats in areas such as authentication, data integrity, and information disclosure.
- **Static Code Analysis**: Detected vulnerabilities in third-party libraries and coding practices.
- **Dynamic Testing**: Highlighted security misconfigurations, missing headers, and potential information leaks.
- **Penetration Testing**: Focused primarily on information gathering due to the absence of significant vulnerabilities.

## Conclusion
The security assessment revealed that the StuRa web application is well-secured, with no critical vulnerabilities that could compromise the system. Minor vulnerabilities related to information exposure were identified, but they do not pose a significant threat to the overall security of the application.

## Tools and Frameworks Employed
- **Static Analysis**: Snyk
- **Dynamic Testing**: OWASP ZAP, Burp Suite, Nessus
- **Penetration Testing**: Kali Linux tools, Dirb, Nikto, Wapiti

## Recommendations
- Implement strong authentication mechanisms, such as multi-factor authentication (MFA).
- Regularly audit and sanitize `.htaccess` files and configure strict file permissions.
- Enable security headers such as CSP, X-Frame-Options, and X-Content-Type-Options.
- Regularly update third-party libraries and dependencies to patch known vulnerabilities.

## Acknowledgments
This project was completed as part of a cybersecurity exercise at Brandenburg University of Technology, Germany, under the guidance of Prof. Dr. rer. nat. Leen Lambers and Dr. Lucas Sakizloglou.

