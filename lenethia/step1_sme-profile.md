# Step 1: SME Profile – LexSecure Compliance Firm

## Company Overview
**Company Name:** LexSecure Compliance Firm  
**Sector:** Legal-Tech & Compliance Consultancy  
**Region of Operation:** Southern & West Africa  
**Number of Employees:** 50

LexSecure is a growing SME providing digital legal services and regulatory compliance solutions to clients in South Africa, Nigeria, and neighbouring countries. The company supports clients with cybersecurity audits, policy development, legal documentation storage, and risk advisory. Remote work is common for consultants and legal researchers.

## Primary Services
- Compliance advisory (NIST, ISO 27001, POPIA, GDPR)
- Legal-sector cybersecurity audits
- Third-party vendor risk management
- Secure digital document management
- Incident response planning and simulations

## IT Infrastructure Overview
- 2 virtual servers (Ubuntu and Windows Server 2019)
- 15 endpoint systems (mix of Windows 11 and macOS)
- 3 internally developed web applications (1 is client-facing)
- Microsoft Active Directory with limited MFA (mainly admins)
- Cloud storage for encrypted legal documents (via OneDrive Business)
- No dedicated Security Operations Centre (SOC)
- Firewalls on all servers and VPN for remote users
- No SIEM, no endpoint detection response (EDR) in place

## Current Cybersecurity Challenges
- No real-time security monitoring or log correlation
- Legal document storage vulnerable to exfiltration
- No DLP (Data Loss Prevention) tools implemented
- Weak identity and access management (IAM) for non-admin staff
- Staff are not trained in cyber hygiene or phishing awareness
- Cybersecurity controls are mostly manual or outdated

## Security Goals for the Project
- Identify current detection and response capability gaps
- Propose practical, scalable controls aligned with NIST CSF & ISO/IEC 27001
- Design controls that fit legal workflows without disrupting operations
- Develop cyber awareness training plans for legal staff
- Maintain low cost and high usability suitable for a small legal-tech firm

## Justification for SME Selection
LexSecure represents a realistic SME in a high-risk, high-trust sector (legal services). Its regional operations and digital-first model make it a strong candidate for implementing a modern cybersecurity architecture using the NIST Cybersecurity Framework and ISO/IEC 27001. The goal is to propose controls and recommendations that are both standards-based and SME-friendly.
