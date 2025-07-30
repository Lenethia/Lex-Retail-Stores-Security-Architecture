# Cybersecurity Architecture for Lex Retail Stores

This repository contains a group cybersecurity project for the Wilses Global Cybersecurity Remote Internship. Our team was tasked with designing a realistic, risk-based security architecture for an SME, using the NIST Cybersecurity Framework (CSF) and aligning recommendations to ISO/IEC 27001:2022 controls.

---

## SME Profile: Lex Retail Stores

- Company Type: Online retail startup (marketplace model like Amazon)  
- Size: 20 employees  
- Cybersecurity Maturity: No existing cybersecurity program, policies, or dedicated personnel  
- Budget: Extremely limited (relying mostly on free tools or basic paid plans)  
- Business Model: Customers buy goods online; independent vendors register and sell through the platform

---

## IT Infrastructure Summary

- Website Platform: WordPress + WooCommerce on shared hosting  
  - Accepts online payments via Stripe and PayFast  
  - No security plugins, firewall, or malware scanner installed  
  - SSL certificate enabled (basic level)  

- Cloud & Data Services:  
  - Google Workspace (Gmail, Drive, Meet, Docs)  
  - Vendor and order tracking done in Google Sheets  
  - No encryption, classification, or backup system  

- Employee Devices:  
  - 10 shared laptops (Windows 10/11 and macOS)  
  - Unmanaged, no endpoint protection or patching  
  - Shared across shifts, increasing insider and malware risk  

- Vendor Access:  
  - Vendors manage listings through WordPress portal  
  - No vetting, validation, or MFA  
  - Poor password hygiene  

- Customer & Payment Data:  
  - WooCommerce stores customer PII (name, email, billing info)  
  - Some partial card data depending on plugin config  
  - No tokenisation, retention policy, or POPIA/GDPR compliance  

- Network & Access:  
  - Accessed via personal/home Wi-Fi  
  - No VPN, no segmentation  
  - Shared admin credentials, no logging or monitoring  

---

## Key Risks Identified

- Customer and vendor PII exposed due to lack of data protection  
- Poor access controls and shared credentials  
- No endpoint or network security  
- No logging, monitoring, or incident detection  
- No security awareness or training across staff or vendors  

---

## Project Objective

To develop a practical cybersecurity architecture tailored to Lex Retail Stores, using the NIST CSF's five functions (Identify, Protect, Detect, Respond, Recover) and mapping controls to ISO/IEC 27001. All controls are chosen with the startup’s low budget and lack of maturity in mind.

---

## Project Structure & Team Roles

```plaintext
lex-retail-cybersecurity/
│
├── README.md                  ← Project overview (this file)
├── Final-Report/              ← Combined PDF report for submission
├── Presentation/              ← PowerPoint slides for each team member
│
├── Lenethia/                  ← SME profile, risk matrix, ISO mapping, test strategy, final assembly
├── Robert/                    ← Asset inventory, current controls review
├── Prosper/                   ← Vulnerability scan, detection/response tools
├── Precious/                  ← Awareness plan, incident communication
Each team member works independently in their folder, contributing 4–5 slides and screenshots based on their assigned steps. Final integration will occur before submission.

Team Roles
Lenethia Van Vuuren (Team Lead):

SME profile & threat landscape (Step 1)

Risk matrix development (Step 2)

NIST-to-ISO/IEC 27001 mapping (Step 7)

Risk-based testing plan (Step 10)

Final report and presentation coordination (Step 11)

Includes screenshots of risk matrix, control mappings, and planning documents

Robert:

Asset discovery using Nmap & Netdiscover (Step 3)

Review of current controls (Snort, auditd) (Step 6)

Includes screenshots of scans and logs

Prosper:

Vulnerability & threat scanning (Nessus) (Step 4)

Detection & response tools (Wireshark, Snort, Wazuh) (Step 8)

Includes Nessus report, alerts, packet captures

Precious:

Awareness and training plan (Step 5)

Incident response communication strategy (Step 9)

Includes mock email samples, training checklist

Deliverables
NIST-based cybersecurity architecture

Risk matrix and threat modelling

ISO/IEC 27001 mapped control recommendations

Testing and validation plan

Awareness and incident communication protocols

Final PDF report and team presentation

vbnet
Copy
Edit
