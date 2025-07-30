## Step 2: Risk Identification and Assessment

Lex Retail Stores is an online retail startup with 20 employees and no existing cybersecurity infrastructure. This assessment identifies the company’s top cybersecurity risks, based on its current systems, technologies, and business model. Risks were assessed using a basic qualitative matrix measuring likelihood and potential impact.

### Methodology

- Used NIST CSF Identify Function to guide risk assessment.
- Analysed SME's infrastructure, business processes, and user behaviours.
- Assigned qualitative risk ratings (Low, Medium, High) based on threat exposure and asset value.

### Summary Risk Matrix

| Risk ID | Risk Description | Impact | Likelihood | Risk Level |
|--------|------------------|--------|------------|------------|
| R1 | Customer PII exposure due to lack of data encryption and access control | High | High | **Critical** |
| R2 | Payment data compromise via insecure plugins or poor Stripe configuration | High | Medium | **High** |
| R3 | Vendor account misuse due to weak authentication and no vetting | Medium | High | **High** |
| R4 | Malware infections from shared, unmanaged employee laptops | Medium | Medium | **Medium** |
| R5 | Loss of business data (orders, inventory) due to no backups | High | Low | **Medium** |
| R6 | Insider threats due to shared logins and no monitoring | Medium | Medium | **Medium** |
| R7 | Non-compliance with POPIA/GDPR due to outdated privacy policy | Medium | High | **High** |

### Key Risk Themes

- **Sensitive data is unprotected**: Customer PII and transaction data are at risk.
- **No access control**: Shared devices and logins increase exposure.
- **No vendor screening**: Anyone can upload potentially malicious content.
- **Lack of monitoring**: No visibility into unauthorised access or changes.
- **Regulatory non-compliance**: No adherence to POPIA or GDPR.

### Next Steps

These risks will guide the mapping of NIST CSF controls (Step 7) and inform which controls from ISO/IEC 27001 are critical to implement first. Key risks will also be prioritised in the testing and mitigation plan (Step 10).
