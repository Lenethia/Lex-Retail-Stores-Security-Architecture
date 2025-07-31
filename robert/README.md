Robert's workspace for asset inventory and existing controls review (Step 3 and 6)
<h1>🔐 Lex Retail Stores – Cybersecurity Architecture Report</h1>

<h2>Section: Technical Infrastructure – Identify & Protect</h2>
<h2>Analyst: Robert</h2>
<h2>Step 3: Asset Inventory</h2>
<h2>Aligned Standard: ISO/IEC 27001:2022 – Control A.5.9 (Inventory of Information and Other Associated Assets)</h2>
<h3>1. Objective</h3>
To identify, classify, and document all assets associated with Lex Retail’s digital infrastructure, including servers, endpoints, and platforms. This step enables Lex Retail to understand its attack surface and implement protective measures in accordance with the NIST Cybersecurity Framework (Identify & Protect) and ISO 27001 A.5.9 requirements.

<br />
<h3>2. Tools Used</h3>

- <b>Packet tracer – To do a design simulation showing the organizations structure.</b>
- <b>Nmap – To detect active hosts, open ports, and services.</b>
- <b>Netdiscover – To identify live hosts and MAC addresses on the local network.</b>
- <b>Browser + WordPress Admin Panel – To inspect plugin settings, security gaps, and missing configurations like 2FA or firewalls.</b>
<h3>3. Findings</h3>
<h3>A. Mini Network in Packet Tracer Simulating Lex retail assets</h3>
<h3>Physical Topology</h3>

<p align="center">
Physical Topology: <br/>
<img src="https://imgur.com/gUucuza.png="cybersecurityarchitect"/>
<br />
<br />
The above image is a physical topology of lex retail stores.<br />
<h3>Netdiscover</h3>
<p align="center">
Netdiscover: <br/>
<img src="https://imgur.com/I2ETl7U.png="cybersecurityarchitect"/>
<br />
<br />
This simulates Netdiscover to find live devices through a successful ping on the inter connected host present in lex retail stores.<br />
<h3>Simulate Nmap Scan (Port/Service Discovery)</h3>
<p align="center">
Simulate Nmap Scan (Port/Service Discovery): <br/>
<img src="https://imgur.com/84kr0no.png="cybersecurityarchitect"/>
<br />
<br />
The above image shows a simulated nmap logic type scan showing that http port 80 is open and note that nmap scan can not be done in packet tracer so we decided to simulated further ideas to show case the presence of a possible nmap scan.<br />
<img src="https://imgur.com/8FfZn5i.png="cybersecurityarchitect"/>
<br />
<br />
The above shows the presence of an open port on port 21 ftp and this can also be show on an nmap scan output but am substituting the idea with this approach because nmap scans can’t be done in packet tracer.<br />
<h3>An Asset Table (Simulated Results)</h3>

| 🌐 IP Address  | 💻 Device        | 🖥️ OS (Assumed)   | ⚙️ Services Detected        | 📝 Notes                   |
|----------------|------------------|-------------------|-----------------------------|----------------------------|
| `192.168.1.10` | 🛒 POS Terminal   | 🪟 Windows 10      | 🟢 ICMP only                | Basic endpoint             |
| `192.168.1.11` | 👨‍💼 Admin PC     | 🪟 Windows 11      | 🟢 ICMP only                | 🔐 High-privileged user    |
| `192.168.1.12` | 📦 Inventory PC  | 🐧 Ubuntu Linux    | 🟢 ICMP only                | 📁 Stores inventory logs   |
| `192.168.1.20` | 🖥️ Server         | 🐧 Linux Server    | 🟠 FTP (21)<br>🌐 HTTP (80) | 🚫 No firewall detected    |

<h3>B. Asset Discovery (Nmap + Netdiscover) Done on kali for real world scenario</h3>
<h3>Note this is still a simulation event.</h3>

- <b>Public IP scanned: (45.33.32.156) nmap Ip address.</b>
- <b>Results Summary:</b>
This result shows information on the open port, filtered port meaning presence of possible firewalls or closed ports, web server running, WordPress platform detected if available and dns server records.

<br />
<p align="center">
Nmap Scan Result: <br/>
<img src="https://imgur.com/uytUaGJ.png="cybersecurityarchitect"/>
<br />
<br />

- <b>Internal IP scan (Netdiscover results):</b>
This result was done based on a simulation and certain information’s were withheld for privacy reasons and 3 hosts were discovered.

<br />
<p align="center">
Netdiscover Scan Result: <br/>
<img src="https://imgur.com/e3ra46v.png="cybersecurityarchitect"/>
<br />
<br />
<h3>C. Asset Classification Table</h3>

| 🏷️ Asset Name     | 💽 Type             | 🌐 IP Address     | 🧩 Role                       | 🔐 Data Sensitivity        |
|-------------------|---------------------|-------------------|-------------------------------|----------------------------|
| `lexretail.com`   | 🌍 Web Server        | `147.93.57.86`    | Hosts customer-facing<br>site | 🔴 High (PII, credentials) |
| Admin Workstation | 💻 Endpoint (PC)     | `192.168.0.12`    | Backend access                | 🟠 Medium                  |
| POS Terminal      | 🧾 IoT Device        | `192.168.0.18`    | Sales transaction             | 🟠 Medium                  |
| MySQL Server      | 🗄️ Database Backend  | `192.168.0.10`    | Stores user/vendor<br>data    | 🔴 High (PII, payment info) |

<h3>NB: This is a fictional scenario but a standard professional procedure explaining all the possible found asset in lex retail stores and further expanded assets would include the following below.</h3>
<h3>Expanded Asset Classification – Lex Retail Stores.</h3>
This section goes beyond IPs and scan data and helps show what Lex Retail really owns and needs to protect, grouped by categories:

<br />
<h3>1. Hardware Assets</h3>

| 🏷️ Asset                  | ⚙️ Function               | 📝 Notes                                       |
|---------------------------|---------------------------|------------------------------------------------|
| 🧑‍💼 Admin Workstations    | Used by staff to manage site | ⚠️ High risk of phishing/malware               |
| 🛒 POS Terminals          | Payment processing         | 💳 May store card data or sync to cloud        |
| 🌐 Routers/Switches       | Network backbone           | 🚪 Gateway to internet — critical for uptime   |
| 💾 Backup Drives / NAS    | Offline/online backups     | 🔒 Needs encryption & physical control         |
| 📱 Personal Devices (BYOD)| Staff phones, laptops      | 🚨 Likely unmanaged — serious attack vector     |

<h3>2. Software & Platform Assets</h3>

| 💻 Platform              | 🧩 Use                            | ⚠️ Risk                                            |
|--------------------------|-----------------------------------|---------------------------------------------------|
| 🌐 WordPress CMS         | Hosts main retail website         | 🌍 Exposed to internet — plugin abuse             |
| 🗄️ MySQL Database        | Stores user/vendor/payment data   | 🔐 PII and business-critical info                 |
| 🛒 WooCommerce Plugin    | Handles orders and carts          | 💳 Payment-related logic                          |
| 🧑‍💼 Vendor Dashboard     | Custom-coded management tool      | 🚫 May lack proper access control                 |
| 📧 Email Server/Accounts | Communications                    | 🎯 Phishing target + business data exposure       |

<h3>3. Data Assets</h3>

| 🧬 Data Type              | 📍 Location                          | 🔐 Sensitivity                         |
|--------------------------|--------------------------------------|----------------------------------------|
| 🧑‍🤝‍🧑 Customer PII         | 🗄️ WordPress DB, WooCommerce         | 🔴 High (GDPR, privacy laws)           |
| 💳 Payment Info (tokens)  | 🔌 WooCommerce or 3rd-party plugin   | 🔴 High (PCI compliance required)      |
| 🧑‍💼 Vendor Account Data   | 🗃️ MySQL or cloud DB                 | 🟠 Medium to High                      |
| 📊 Sales Reports          | 🖥️ Admin PC or ☁️ cloud spreadsheets | 🟠 Medium                              |
| ⚙️ Website Config Files   | 📁 Server root folders                | 🟠 Medium (can expose paths/API keys)  |

<h3>D. WordPress Security Findings</h3>
A security check was performed on the Lex Retail WordPress admin panel (simulated instance). The following weaknesses were identified:

<br />
<h3>Missing Security Controls:</h3>

- <b>No Firewall Plugin Installed: Wordfence or similar tools not active to block malicious traffic.</b>
- <b>No Two-Factor Authentication (2FA): Admin login panel is accessible via /wp-admin with only single-factor login.</b>
- <b>Outdated Plugins Detected: WooCommerce and other plugins were several versions behind, exposing potential known CVEs.</b>
- <b>No Backup or Hardening Plugin Active: No scheduled backup system or security hardening plugin like iThemes Security.</b>

<h3>Observed Risk Summary:</h3>

| 🕵️ Finding             | ⚠️ Risk   | 💥 Impact                                |
|------------------------|-----------|------------------------------------------|
| 🚫 No 2FA              | 🔴 High   | Easy brute-force or credential stuffing  |
| 🔥 No Firewall Plugin  | 🔴 High   | No defense against bot/scan attacks      |
| 🧩 Outdated Plugins     | 🟠 Medium | Vulnerable to known exploits             |
| 💾 No Backup Tool       | 🟠 Medium | No recovery if site is compromised       |

<p align="center">
Wordpress Scan Result: <br/>
<img src="https://imgur.com/GOCTbLY.png="cybersecurityarchitect"/>
<br />
<br />

<h3>4. ISO/IEC 27001:2022 Alignment – Control A.5.9</h3>
<h3>Control A.5.9 requires organizations to:</h3>
“Identify and document inventories of assets relevant to information processing and associated information systems.”

<br />
<h3>This inventory satisfies baseline compliance by:</h3>

- <b>Identifying and documenting all critical and supporting assets.</b>
- <b>Mapping asset roles and data classification.</b>
- <b>Supporting future control implementation (e.g., protection, monitoring, access restriction).</b>
- <b>Assign Asset Ownership.</b>
- <b>Track Asset Lifecycle.</b>

<h3>Purpose of This Control:</h3>

- <b>Ensure all critical assets (devices, software, data, etc.) are known, tracked, and assigned ownership.</b>
- <b>Enable proper risk management, incident response, and protection measures.</b>

<h3>5. Next Steps</h3>

- <b>Implement a formal asset inventory register in spreadsheet or CMDB tool.</b>
- <b>Schedule regular rescans (monthly/quarterly) to detect unauthorized devices.</b>
- <b>Apply WordPress hardening and install firewall + 2FA plugins.</b>
- <b>Tag high-risk assets for prioritized protection in the next project phase.</b>


<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
