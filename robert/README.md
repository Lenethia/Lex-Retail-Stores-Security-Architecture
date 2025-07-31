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

| table | table2 |
|.......|........|



<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
