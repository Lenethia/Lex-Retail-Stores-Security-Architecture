# Cybersecurity Architecture for Lex Retail Stores

This repository contains the final team project for the Wilses Global Cybersecurity Remote Internship. Our team was tasked with designing a realistic, budget-conscious cybersecurity architecture for an SME with no prior security program. The project follows the NIST Cybersecurity Framework (CSF) and aligns all recommendations with ISO/IEC 27001:2022 controls.

## SME Profile: Lex Retail Stores

- Company Type: Online retail startup
- Size: 20 employees
- Cybersecurity Maturity: None (no policies, no controls, no IT staff)
- Budget: Extremely limited (free/open-source tools or entry-level paid tiers)
- Business Model: 
  - Customers purchase products online using Stripe or PayFast
  - Independent vendors register, upload products, and manage orders via WordPress/WooCommerce

## IT Infrastructure Summary

Website Platform:
- WordPress + WooCommerce on shared hosting
- No firewall, malware scanner, or security plugins
- Accepts online payments
- Basic SSL enabled

Cloud & Data Services:
- Google Workspace (Gmail, Drive, Meet, Docs)
- Order/vendor logs stored in shared Google Sheets
- No encryption or backup system

Employee Devices:
- 10 shared laptops (Windows) used in shifts
- No endpoint protection, patching, or device management (MDM)

Vendor Access:
- No MFA, vetting, or credential policies for vendors
- Weak password practices

Customer & Payment Data:
- WooCommerce stores PII: name, email, billing address
- Partial card data stored depending on plugin configuration
- No tokenisation, data retention policy, or compliance with POPIA/GDPR

Network & Access:
- All tools accessed via personal or home networks
- No VPN, segmentation, or access logging
- Shared passwords for Google Workspace and WordPress backend

## Key Risks Identified

- PII exposure from customer and vendor data
- No access controls or logging
- Unprotected endpoints and unmanaged devices
- Vulnerable WordPress stack (no updates, no 2FA)
- Zero training or security awareness across staff and vendors

## Project Objective

To develop a practical, risk-based cybersecurity architecture tailored to a zero-maturity SME environment. The strategy leverages the five NIST CSF functions (Identify, Protect, Detect, Respond, Recover) and aligns with ISO/IEC 27001:2022 Annex A controls. All activities simulate realistic threats while accommodating the startup’s technical and financial constraints.

## Project Structure

lex-retail-cybersecurity/
│
├── README.md ← This file (Project overview)
├── Presentation/ ← PowerPoint slides
│
├── Lenethia/ ← Risk matrix, ISO mapping, testing, final edits
├── Robert/ ← Asset inventory, control gap review
├── Prosper/ ← Vulnerability scans, detection tools
├── Precious/ ← Awareness program, IR and recovery strategy

markdown
Copy code

## Team Roles and Responsibilities

Lenethia Van Vuuren (Team Lead)  
- Step 1: SME Profile and Threat Landscape  
- Step 2: Risk Matrix Creation  
- Step 7: NIST-CSF to ISO/IEC 27001 Control Mapping  
- Step 10: Risk-Based Testing Plan  
- Step 11: Final Report and Presentation  
- Includes: Risk matrix visual, ISO mapping graphic, control implementation plan

Robert  
- Step 3: Asset Discovery (Packet Tracer, Nmap, Netdiscover)  
- Step 6: Review of Existing Controls (RBAC, Antivirus, MFA, Encryption)  
- Includes: Simulated network scans, WordPress vulnerabilities, asset tables

Prosper  
- Step 4: Threat and Vulnerability Scanning (Nessus, web app testing)  
- Step 8: Detection and Monitoring (logging, alerting, Snort, Wazuh)  
- Includes: Scan reports, detection tool evidence, internal traffic patterns

Precious  
- Step 5: Cybersecurity Awareness Plan (Monthly Training and Simulations)  
- Step 9: Incident Communication and Recovery Strategy  
- Includes: Training schedule, mock phishing examples, recovery RTO/RPO plans

## Deliverables

- NIST-CSF-based cybersecurity architecture  
- Risk matrix with scoring (likelihood vs impact)  
- ISO/IEC 27001:2022-aligned controls mapped by NIST function  
- Visual summaries: asset inventory, control coverage, matrix graphics  
- Realistic simulations: phishing, vulnerability scans, detection  
- Cybersecurity awareness and IR policy draft  
- Team presentation (PPT)
  
**Final PowerPoint Presentation:**  
[Lex-Retail-Stores-Security-Architecture/docs/Final_Team-Project.pptx](docs/Final_Team-Project.pptx)


## Project Completion

- Final Report Submission:  
- Presentation Slides: `/Presentation/Team_Presentation.pptx`  
- Screenshots and visuals: Embedded in each team member's folder

## Standards and References

- NIST Cybersecurity Framework v1.1  
- ISO/IEC 27001:2022 (Annex A Controls)  
- MITRE ATT&CK Framework (simulated threat techniques)  
- Open-source security tools (Nmap, Nessus, GoPhish, Wordfence, Snort)

This project simulates a complete cybersecurity architecture engagement for an SME and demonstrates real-world team collaboration using GitHub, Markdown, open-source tooling, and best practices from global cybersecurity standards.
