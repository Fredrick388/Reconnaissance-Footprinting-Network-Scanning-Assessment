# Penetration Testing Report

## Reconnaissance, Footprinting & Network Scanning Assessment
 

> Week 2 Practical Module (W2-PM-FINAL)
>
> Cybersecurity & Ethical Hacking Internship - Networkwalks
 
---
 
## Author
 
**Fredrick Musonda**
Cybersecurity Professional
 
- Program/Batch: B082-Networkwalks
- Date: 20 August 2026
- LinkedIn: https://www.linkedin.com/in/fredrick-musonda-b47286192
 
---
 
## Project Overview
 
This penetration testing assessment focused on the initial stages of ethical hacking:
 
- Reconnaissance
- Footprinting
- Open Source Intelligence (OSINT) Gathering
- Network Discovery
- Network Scanning
 
The assessment involved reconnaissance against the **networkwalks.com** domain using Kali Linux security tools and network scanning of an authorized local network using Zenmap.
 
All testing activities were performed within an authorized environment and under approved scope.
 
---
 
## Scope
 
### Target Systems
 
1. Networkwalks.com (authorized assessment)
2. Personal Local Area Network (LAN)
 
### Authorization
 
✅ Written authorization obtained
 
### Phases Covered
 
| Phase | Status |
|---------|---------|
| Reconnaissance & Footprinting | Completed |
| Scanning & Network Discovery | Completed |
| Enumeration & Exploitation | In Progress |
 
---
 
# Liability Disclaimer
 
This assessment was conducted solely on systems, networks, and devices for which explicit authorization was granted.
 
The information contained in this repository is intended for educational, research, and authorized security assessment purposes only.
 
Unauthorized use of the techniques or tools described may violate applicable laws and regulations.
 
---
 
# Objectives
 
The objectives of this assessment were:
 
- Gather publicly available information about a target organization
- Perform OSINT-based reconnaissance
- Discover exposed technologies and infrastructure
- Enumerate DNS and email-related information
- Identify active hosts on an authorized network
- Understand how attackers conduct the early stages of penetration testing
 
---
 
# Tools Used
 
| Tool | Purpose |
|--------|---------|
| Kali Linux | Reconnaissance and Footprinting |
| Windows OS | Network Scanning Environment |
| WHOIS | Domain Registration Enumeration |
| WhatWeb | Website Technology Detection |
| Nslookup | DNS Resolution |
| Curl | HTTP Header Inspection |
| Wafw00f | WAF Detection |
| DNSRecon | DNS Enumeration |
| Google Search (GHDB) | Advanced Search Reconnaissance |
| Maltego | OSINT Relationship Mapping |
| theHarvester | Email/Subdomain Enumeration |
| Zenmap (Nmap GUI) | Network Discovery |
| Windows CMD | Network Configuration Discovery |
 
---
 
# Activities Performed
 
## 1. Reconnaissance Using Kali Linux Tools
 
Reconnaissance was conducted against:
 
```text
networkwalks.com
```
 
### Tools Utilized
 
- WHOIS
- WhatWeb
- Nslookup
- Curl
- Wafw00f
- DNSRecon
 
### Key Findings
 
#### WHOIS
 
Collected:
 
- Domain registration information
- Registrar details
- Name server records
 
#### WhatWeb
 
Identified:
 
- WordPress 7.0.4
- WP Download Manager 3.3.58
 
#### Nslookup
 
Resolved domain to:
 
```text
192.232.216.135
```
 
#### Curl
 
Identified:
 
- HTTP response headers
- WordPress REST API endpoint
 
```text
/wp-json/
```
 
#### Wafw00f
 
Detected:
 
```text
ModSecurity (SpiderLabs)
```
 
#### DNSRecon
 
Enumerated:
 
- Name Servers
- Mail Servers
- TXT Records
- SPF Records
- Service Records
 
---
 
## 2. GHDB Footprinting
 
Google Hacking Database (GHDB) was used to perform search engine reconnaissance.
 
### Objectives
 
- Discover exposed resources
- Identify indexed systems
- Locate internet-facing devices
 
### Findings
 
Search results revealed:
 
- Publicly discoverable camera interfaces
- Indexed surveillance devices
- Internet-exposed management systems
 
### Security Impact
 
Improperly secured devices exposed through search engines may reveal sensitive information to attackers.
 
---
 
## 3. Maltego OSINT Assessment
 
Maltego was used to gather Open Source Intelligence (OSINT).
 
### Objectives
 
- Discover publicly exposed organizational information
- Enumerate email addresses
- Visualize relationships between entities
 
### Findings
 
Using email transforms, public email addresses associated with:
 
```text
networkwalks.com
```
 
were identified.
 
### Security Impact
 
Public email exposure increases the risk of:
 
- Phishing attacks
- Social engineering
- Credential harvesting campaigns
 
---
 
## 4. theHarvester Assessment
 
theHarvester was used against:
 
```text
microsoft.com
```
 
### Data Sources
 
- Baidu
- Multiple public OSINT providers
 
### Information Collected
 
- Email addresses
- Hostnames
- Subdomains
 
### Security Impact

Public information can assist attackers in mapping organizational infrastructure.
 
---
 
## 5. Network Scanning Using Zenmap
 
Zenmap was used to perform host discovery on an authorized local network.
 
### Objectives
 
- Identify live hosts
- Discover active devices
- Enumerate network services
 
### Information Gathered
 
- IP Addresses
- MAC Addresses
- Device Vendors
- Reachable Hosts
 
### Outcome
 
Multiple live hosts were successfully identified within the target subnet.
 
---
 
# Risk Analysis
 
| Finding | Impact | Risk |
|----------|---------|------|
| Website technologies exposed | Enables technology fingerprinting | Medium |
| Public IP address discovery | Reveals infrastructure location | Low |
| HTTP headers exposed | Assists information gathering | Low |
| WAF identification | Reveals defensive architecture | Low |
| DNS records exposed | Enables infrastructure mapping | Medium |
| Search engine indexed cameras | Sensitive device exposure | Medium |
| Public email addresses | Phishing and social engineering risks | Medium |
| Exposed subdomains | Assists attack planning | Medium |
| Multiple discoverable network hosts | Expands attack surface | Medium |
 
---
 
# Recommendations
 
## Web Applications
 
- Minimize exposed technology information
- Regularly update CMS platforms and plugins
- Review HTTP response headers
 
## Infrastructure Security
 
- Audit DNS records periodically
- Monitor exposed assets and subdomains
- Maintain WAF protection
 
## Internet-Facing Devices
 
- Protect administrative interfaces
- Require authentication
- Prevent search engine indexing
 
## Email Security
 
- Limit unnecessary exposure of email addresses
- Conduct phishing awareness training
- Monitor for external exposure
 
## Network Security
 
- Maintain an updated asset inventory
- Perform periodic internal network scans
- Investigate unknown devices immediately
- Document network architecture
 
## Governance
 
- Conduct testing only with written authorization
- Maintain defined testing scopes
- Follow responsible disclosure practices
 
---
 
# Key Lessons Learned
 
This assessment demonstrated how attackers and security professionals can gather valuable intelligence during the early phases of a penetration test.
 
Important discoveries included:
 
- Technology fingerprinting
- DNS reconnaissance
- Email enumeration
- OSINT relationship mapping
- Search engine reconnaissance
- Internal network discovery
 
The exercise reinforced the importance of reducing information exposure and maintaining a strong security posture.
 
---
 
# Conclusion
 
During Week 2 of the Cybersecurity & Ethical Hacking Internship at Networkwalks, practical exercises involving footprinting, OSINT gathering, reconnaissance, and network scanning were successfully completed.
 
The assessment demonstrated how publicly available information, DNS records, email addresses, subdomains, web technologies, and active network hosts can be discovered and analyzed during the initial stages of a penetration testing engagement.
 
These exercises strengthened practical skills in ethical hacking while reinforcing the importance of conducting security assessments responsibly, ethically, and within authorized boundaries.
 
---
 
**Author:** Fredrick Musonda

**Role:** Cybersecurity Professional

**Assessment Type:** Reconnaissance, Footprinting & Network Scanning
`
