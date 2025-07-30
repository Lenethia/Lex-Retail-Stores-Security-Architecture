## Step 1: SME Profile – Lex Retail Stores

### SME Name  
**Lex Retail Stores**

### Industry  
E-commerce / Online Retail Startup

### Business Model  
Lex Retail Stores is a small online marketplace startup where:
- Customers purchase items online using credit cards and mobile payments.
- Independent vendors register and upload their products to the platform.
- Sales, product listings, and order fulfilment are managed through a basic WordPress + WooCommerce setup.

### Size and Resources  
- **Employees:** 20  
- **Cybersecurity Maturity:** Very low  
- **Budget:** Limited; no dedicated security team or SOC

### Infrastructure Overview  
- **Platform:** WordPress + WooCommerce (shared hosting, basic SSL)  
- **Devices:** 10 shared laptops, no endpoint protection or encryption  
- **Cloud Services:** Google Workspace (Docs, Drive, Gmail), no access controls or backups  
- **Vendor Access:** Unscreened vendor registration, potential for malicious uploads  
- **Payment Processing:** Stripe and PayFast used, customer PII stored in WP database  
- **Network & Logging:** No VPN, no logging, remote work on unsecured Wi-Fi  

### Key Risks  
- Shared credentials and unmanaged endpoints  
- Customer and vendor data exposed to leakage or breach  
- No monitoring or alerts  
- No phishing protection, email security, or user training  
- Regulatory non-compliance (POPIA, PCI-DSS, GDPR)

### Why a Security Architecture is Needed  
Lex Retail Stores is highly vulnerable and lacks basic cyber hygiene.  
This project will apply the **NIST Cybersecurity Framework** and align it with **ISO/IEC 27001:2022** controls to:
- Reduce real-world risks  
- Build realistic safeguards that fit SME limitations  
- Lay the foundation for compliance and operational scale
