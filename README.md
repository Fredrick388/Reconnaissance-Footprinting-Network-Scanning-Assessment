PENETRATION TESTING REPORT
Reconnaissance, Footprinting & Network Scanning Assessment
W2-PM-FINAL | CYBERSECURITY | NETWORKWALKS



Pentester Name
(Cybersecurity Professional)	FREDRICK MUSONDA
Program/Batch	B082-Networkwalks
Date	 20 August 2026
Modules completed	W2-PM1 (Multiple Kali Tools)
W2-PM2 (GHDB based Footprinting Attacks)
W2-PM3 (Maltego based Footprinting Attacks)
W2-PM4 (theHarvester based Footprinting Attacks)
W2-PM5 (Zenmap Scanning)
Client/Target	1. Networkwalks (secured written permission already)
2. My own local LAN Network
Permission secured from client?	Yes
Phases covered	Phase 1: Reconnaissance & Footprinting
Phase 2: Scanning & Network Discovery
Phase 3-5: In Progress









1.	Liability Disclaimer

This penetration testing assessment was conducted only on systems, networks, and devices for which explicit authorization was obtained. All activities were performed within the agreed scope and for legitimate security assessment purposes. The information contained in this report is intended solely for authorized use. Any unauthorized use of the techniques, tools, or findings described herein may violate applicable laws and regulations. The author assumes no liability for any misuse of this information, and all actions taken based on this report remain the sole responsibility of the user.


 
2. Introduction
This report documents the Footprinting and Network Scanning phases conducted as part of my Week 2 internship activities at Networkwalks. The assessment involved footprinting the networkwalks.com domain using various Kali Linux reconnaissance tools and scanning my own local network using Zenmap.
The assessment was divided into five modules. W2-PM1 involved footprinting a target domain using multiple Kali Linux tools to gather publicly available information. W2-PM2 focused on Google Hacking Database (GHDB) techniques to discover sensitive information exposed through search engine indexing. W2-PM3 utilized Maltego to perform Open-Source Intelligence (OSINT) gathering and visualize relationships between domains, IP addresses, email addresses, and other entities. W2-PM4 employed theHarvester to enumerate email addresses, subdomains, and hosts from publicly available sources. Finally, W2-PM5 involved network scanning and host discovery using Zenmap to identify active devices, open ports, and exposed services within an authorized local network.
The objective of these exercises was to demonstrate the initial stages of a penetration testing engagement, where an attacker first gathers publicly available information about a target and then identifies active hosts and services within a network. All testing activities were performed in an authorized environment using Kali Linux for footprinting and a Windows system running Zenmap for network scanning.
Each section of this report includes the commands executed, observed results, supporting screenshots, and a brief analysis of the security significance of the findings. This approach provides a practical understanding of how reconnaissance and network discovery contribute to the overall penetration testing process.












3. Tools and Environment
 
The table below summarizes the tools and platforms used throughout the footprinting, OSINT gathering, and network scanning activities.
Tool	Purpose
Kali Linux & Windows OS	operating systems used for footprinting, reconnaissance, and information gathering activities.
WHOIS	Retrieves domain registration information, including ownership, registrar details, registration dates, and name servers.
whatweb	Identifies web technologies, web servers, CMS platforms, frameworks, and plugins used by a website.
nslookup	Queries DNS records and resolves domain names to IP addresses.
curl -I	Retrieves HTTP response headers to identify server information and security configurations.
wafw00f	Detects the presence and type of Web Application Firewall (WAF) protecting a website.
dnsrecon	Enumerates DNS records such as NS, MX, TXT, SPF, and SRV records.
Google Search (GHDB)	Uses advanced search operators (Google Dorks) to discover publicly exposed information indexed by search engines.
Google Hacking Database (GHDB)	Repository of Google Dorks used to locate sensitive files, directories, login portals, and exposed information.
Maltego	Performs Open-Source Intelligence (OSINT) gathering and visualizes relationships between domains, IP addresses, email addresses, and organizations.
To Email Address Transform	Used in Maltego to identify publicly available email addresses associated with a domain.
theHarvester	Collects email addresses, subdomains, hostnames, and other publicly available information from multiple OSINT sources.
Zenmap (Nmap GUI)	Performs host discovery, network mapping, port scanning, and service enumeration.
Windows Command Prompt (CMD)	Used to view local IP addresses, MAC addresses, and network configuration information.



4. Activities Performed

4.1 Footprinting & Reconnaissance Using Multiple Kali Linux Tools
I performed reconnaissance against the networkwalks.com domain using six Kali Linux tools: WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, and DNSRecon. Each tool was used to collect a different type of information about the target.
•	First, I used WHOIS to obtain publicly available domain registration information and identify the domain's name servers. The results provided details about domain registration and hosting infrastructure.
•	I then used WhatWeb to identify technologies used by the website. The results identified WordPress 7.0.4 and WP Download Manager 3.3.58, along with additional information exposed by the web application.
•	Using Nslookup, I resolved the domain name to its IP address. The results identified 192.232.216.135 as the address associated with the target domain.
•	I used Curl with the -I option to inspect the HTTP response headers. This provided additional information about the web application and revealed the WordPress REST API endpoint /wp-json/.
•	Next, I used Wafw00f to determine whether a Web Application Firewall (WAF) was protecting the website. The results identified ModSecurity (SpiderLabs).
•	Finally, I used DNSRecon to enumerate DNS records. The results provided information relating to name servers, mail servers, SPF/TXT records, service records, and DNS software information.

4.2 GHDB-Based Footprinting Attacks
I used the Google Hacking Database (GHDB) to perform reconnaissance through advanced Google search queries, commonly known as Google Dorks. The objective of this exercise was to identify publicly accessible information that had been indexed by search engines.
During the assessment, GHDB queries were used to search for internet-connected camera interfaces and surveillance systems that were publicly exposed online. The results demonstrated how misconfigured or improperly secured devices can be discovered through search engines when sensitive pages or camera feeds are indexed.
This activity highlighted the security risks associated with exposing networked devices to the internet without proper access controls. From an attacker's perspective, such information can be used to identify potential targets and gather intelligence about an organization's infrastructure. The exercise emphasized the importance of securing internet-facing devices, implementing authentication controls, and preventing sensitive resources from being indexed by search engines.

4.3 Maltego-Based Footprinting Attacks 
I used Maltego to perform Open-Source Intelligence (OSINT) gathering against the networkwalks.com domain. The primary objective was to identify publicly available email addresses associated with the target domain using Maltego's built-in transforms and data sources.
Starting with the target domain, I executed email discovery transforms to search for email addresses linked to networkwalks.com. The results provided insight into email accounts that were publicly exposed or referenced online and helped illustrate how information from multiple public sources can be correlated automatically.
This exercise demonstrated how attackers and security professionals can use OSINT tools to gather contact information about an organization. Such information may be used for legitimate security assessments, vulnerability investigations, or awareness of potential social engineering risks. The findings emphasized the importance of limiting unnecessary public exposure of organizational email addresses and implementing user awareness training to reduce phishing-related threats.


4.4 theHarvester-Based Footprinting Attacks
I used theHarvester in Kali Linux to gather publicly available email addresses and subdomains associated with microsoft.com. In the first exercise, Baidu was used as the data source with a result limit of 1000. In the second exercise, theHarvester was configured to use all available sources with a result limit of 50. The results identified email addresses, hostnames, and subdomains related to the target organization, demonstrating how information from multiple public sources can be collected and correlated during the reconnaissance phase of a security assessment.

4.5 Network Scanning and Enumeration Using Zenmap.
I performed network scanning on an authorized local network using Zenmap, the graphical version of Nmap. The objective was to identify active hosts, IP addresses, MAC addresses, and accessible network services.
The scanning process discovered live hosts within the subnet, along with information about their network addresses and device vendors where available. This activity demonstrated how active reconnaissance techniques can be used to map network infrastructure and identify potential entry points within a target environment.
Information gathered during this phase provides valuable insight into the network attack surface and helps security professionals identify systems that may require further security assessment and hardening.


























5. Risk Analysis / Impact
Based on the information collected during the footprinting and network scanning activities, the following potential risks were identified.
#	Risk / Finding	Evidence / Observation	Potential Impact	Risk Level
1	Web technology information exposed	WhatWeb identified WordPress and WP Download Manager	Attackers may use exposed technology information to identify software requiring further security review.	● Medium
2	Server IP address identifiable	Nslookup resolved the domain to 192.232.216.135	Provides information about the network location of the web service.	● Low
3	HTTP technical information exposed	Curl returned HTTP response headers and exposed /wp-json/	May assist technology fingerprinting and further enumeration.	● Low
4	WAF technology identifiable	Wafw00f identified ModSecurity (SpiderLabs)	Reveals information about the website's security architecture.	● Low
5	DNS infrastructure information exposed	DNSRecon identified DNS, mail, and service-related records	DNS information can help build a broader infrastructure profile.	● Medium
6	Publicly accessible cameras discoverable through search engines	GHDB queries returned indexed camera interfaces	Exposed devices may reveal sensitive information and could become targets for unauthorized access attempts.	● Medium
7	Organizational email addresses publicly discoverable	Maltego identified email addresses related to networkwalks.com	Public email addresses may be used for phishing, social engineering, or targeted attacks.	● Medium
8	Email addresses and subdomains exposed through OSINT sources	theHarvester identified email addresses and subdomains associated with microsoft.com	Publicly available organizational information can assist reconnaissance and attack planning.	● Medium
9	Multiple live hosts visible on local network	Zenmap identified active hosts on the local network	Unknown or unauthorized devices may potentially be present on a network.	● Medium
Risk Level Key: ● Critical  ● Medium ● Low

6. Recommendations
Based on the observations gathered during the footprinting, OSINT, and network scanning activities, the following security improvements are recommended:
1.	Review publicly exposed technology information
Organizations should regularly assess what information about web technologies, content management systems (CMS), plugins, and infrastructure is publicly visible to reduce unnecessary information disclosure.
2.	Keep software and plugins updated
Web applications, CMS platforms, plugins, and supporting services should be regularly updated and reviewed against current security advisories to minimize potential security risks.
3.	Review HTTP response headers
HTTP headers should be examined periodically to ensure that unnecessary technical information is not exposed to external users.
4.	Review DNS records regularly
DNS records should be audited to ensure that only required services and information are publicly accessible.
5.	Maintain and monitor Web Application Firewalls (WAFs)
WAF solutions should remain enabled, properly configured, and continuously monitored to detect and mitigate malicious web traffic.
6.	Protect internet-facing devices from search engine indexing
Security cameras, administration interfaces, and other sensitive systems should be protected with strong authentication and configured to prevent indexing by search engines.
7.	Limit public exposure of organizational email addresses
Publicly available email addresses should be reviewed and minimized where possible to reduce the risk of phishing, spam, and social engineering attacks.
8.	Monitor publicly exposed subdomains and assets
Organizations should regularly identify and review exposed subdomains, hosts, and online assets to ensure they remain secure and properly managed.
9.	Perform regular internal network discovery and asset inventories
Periodic network scans should be conducted to identify active devices and maintain visibility over organizational assets.
10.	Investigate unauthorized or unknown devices
Any unexpected devices discovered during network scans should be promptly investigated and verified to prevent unauthorized network access.
11.	Maintain accurate network documentation
Network diagrams, IP addressing information, and asset inventories should be kept up to date to support security monitoring and incident response.
12.	Conduct security testing only with proper authorization
Reconnaissance, footprinting, and scanning activities should only be performed within approved scopes and with appropriate written authorization.



7.	Conclusion
During Week 2 of my Cybersecurity & Ethical Hacking Internship at Networkwalks, I completed practical exercises in footprinting, OSINT gathering, reconnaissance, and network scanning. Using tools such as WHOIS, WhatWeb, Nslookup, Curl, Wafw00f, DNSRecon, GHDB, Maltego, theHarvester, and Zenmap, I gathered information about target domains and identified active hosts on a network.
These activities demonstrated how publicly available information, email addresses, subdomains, DNS records, web technologies, and network devices can be discovered during the early stages of a security assessment. The exercises enhanced my understanding of reconnaissance techniques and highlighted the importance of identifying and managing information exposure.
Overall, the practical labs reinforced the role of information gathering in penetration testing and the importance of conducting all security assessments ethically, responsibly, and within an authorized scope.

8.	EVIDENCE COLLECTED
  
 

      



Author: FREDRICK MUSONDA
Cybersecurity Professional
LinkedIn: www.linkedin.com/in/fredrick-musonda-b47286192  


