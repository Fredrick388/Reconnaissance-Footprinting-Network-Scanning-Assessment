# Penetration Testing Report
2
## Reconnaissance, Footprinting & Network Scanning Assessment
3
 
4
> Week 2 Practical Module (W2-PM-FINAL)
5
>
6
> Cybersecurity & Ethical Hacking Internship - Networkwalks
7
 
8
---
9
 
10
## Author
11
 
12
**Fredrick Musonda**
13
Cybersecurity Professional
14
 
15
- Program/Batch: B082-Networkwalks
16
- Date: 20 August 2026
17
- LinkedIn: https://www.linkedin.com/in/fredrick-musonda-b47286192
18
 
19
---
20
 
21
## Project Overview
22
 
23
This penetration testing assessment focused on the initial stages of ethical hacking:
24
 
25
- Reconnaissance
26
- Footprinting
27
- Open Source Intelligence (OSINT) Gathering
28
- Network Discovery
29
- Network Scanning
30
 
31
The assessment involved reconnaissance against the **networkwalks.com** domain using Kali Linux security tools and network scanning of an authorized local network using Zenmap.
32
 
33
All testing activities were performed within an authorized environment and under approved scope.
34
 
35
---
36
 
37
## Scope
38
 
39
### Target Systems
40
 
41
1. Networkwalks.com (authorized assessment)
42
2. Personal Local Area Network (LAN)
43
 
44
### Authorization
45
 
46
✅ Written authorization obtained
47
 
48
### Phases Covered
49
 
50
| Phase | Status |
51
|---------|---------|
52
| Reconnaissance & Footprinting | Completed |
53
| Scanning & Network Discovery | Completed |
54
| Enumeration & Exploitation | In Progress |
55
 
56
---
57
 
58
# Liability Disclaimer
59
 
60
This assessment was conducted solely on systems, networks, and devices for which explicit authorization was granted.
61
 
62
The information contained in this repository is intended for educational, research, and authorized security assessment purposes only.
63
 
64
Unauthorized use of the techniques or tools described may violate applicable laws and regulations.
65
 
66
---
67
 
68
# Objectives
69
 
70
The objectives of this assessment were:
71
 
72
- Gather publicly available information about a target organization
73
- Perform OSINT-based reconnaissance
74
- Discover exposed technologies and infrastructure
75
- Enumerate DNS and email-related information
76
- Identify active hosts on an authorized network
77
- Understand how attackers conduct the early stages of penetration testing
78
 
79
---
80
 
81
# Tools Used
82
 
83
| Tool | Purpose |
84
|--------|---------|
85
| Kali Linux | Reconnaissance and Footprinting |
86
| Windows OS | Network Scanning Environment |
87
| WHOIS | Domain Registration Enumeration |
88
| WhatWeb | Website Technology Detection |
89
| Nslookup | DNS Resolution |
90
| Curl | HTTP Header Inspection |
91
| Wafw00f | WAF Detection |
92
| DNSRecon | DNS Enumeration |
93
| Google Search (GHDB) | Advanced Search Reconnaissance |
94
| Maltego | OSINT Relationship Mapping |
95
| theHarvester | Email/Subdomain Enumeration |
96
| Zenmap (Nmap GUI) | Network Discovery |
97
| Windows CMD | Network Configuration Discovery |
98
 
99
---
100
 
101
# Activities Performed
102
 
103
## 1. Reconnaissance Using Kali Linux Tools
104
 
105
Reconnaissance was conducted against:
106
 
107
```text
108
networkwalks.com
109
```
110
 
111
### Tools Utilized
112
 
113
- WHOIS
114
- WhatWeb
115
- Nslookup
116
- Curl
117
- Wafw00f
118
- DNSRecon
119
 
120
### Key Findings
121
 
122
#### WHOIS
123
 
124
Collected:
125
 
126
- Domain registration information
127
- Registrar details
128
- Name server records
129
 
130
#### WhatWeb
131
 
132
Identified:
133
 
134
- WordPress 7.0.4
135
- WP Download Manager 3.3.58
136
 
137
#### Nslookup
138
 
139
Resolved domain to:
140
 
141
```text
142
192.232.216.135
143
```
144
 
145
#### Curl
146
 
147
Identified:
148
 
149
- HTTP response headers
150
- WordPress REST API endpoint
151
 
152
```text
153
/wp-json/
154
```
155
 
156
#### Wafw00f
157
 
158
Detected:
159
 
160
```text
161
ModSecurity (SpiderLabs)
162
```
163
 
164
#### DNSRecon
165
 
166
Enumerated:
167
 
168
- Name Servers
169
- Mail Servers
170
- TXT Records
171
- SPF Records
172
- Service Records
173
 
174
---
175
 
176
## 2. GHDB Footprinting
177
 
178
Google Hacking Database (GHDB) was used to perform search engine reconnaissance.
179
 
180
### Objectives
181
 
182
- Discover exposed resources
183
- Identify indexed systems
184
- Locate internet-facing devices
185
 
186
### Findings
187
 
188
Search results revealed:
189
 
190
- Publicly discoverable camera interfaces
191
- Indexed surveillance devices
192
- Internet-exposed management systems
193
 
194
### Security Impact
195
 
196
Improperly secured devices exposed through search engines may reveal sensitive information to attackers.
197
 
198
---
199
 
200
## 3. Maltego OSINT Assessment
201
 
202
Maltego was used to gather Open Source Intelligence (OSINT).
203
 
204
### Objectives
205
 
206
- Discover publicly exposed organizational information
207
- Enumerate email addresses
208
- Visualize relationships between entities
209
 
210
### Findings
211
 
212
Using email transforms, public email addresses associated with:
213
 
214
```text
215
networkwalks.com
216
```
217
 
218
were identified.
219
 
220
### Security Impact
221
 
222
Public email exposure increases the risk of:
223
 
224
- Phishing attacks
225
- Social engineering
226
- Credential harvesting campaigns
227
 
228
---
229
 
230
## 4. theHarvester Assessment
231
 
232
theHarvester was used against:
233
 
234
```text
235
microsoft.com
236
```
237
 
238
### Data Sources
239
 
240
- Baidu
241
- Multiple public OSINT providers
242
 
243
### Information Collected
244
 
245
- Email addresses
246
- Hostnames
247
- Subdomains
248
 
249
### Security Impact
250
 
251
Public information can assist attackers in mapping organizational infrastructure.
252
 
253
---
254
 
255
## 5. Network Scanning Using Zenmap
256
 
257
Zenmap was used to perform host discovery on an authorized local network.
258
 
259
### Objectives
260
 
261
- Identify live hosts
262
- Discover active devices
263
- Enumerate network services
264
 
265
### Information Gathered
266
 
267
- IP Addresses
268
- MAC Addresses
269
- Device Vendors
270
- Reachable Hosts
271
 
272
### Outcome
273
 
274
Multiple live hosts were successfully identified within the target subnet.
275
 
276
---
277
 
278
# Risk Analysis
279
 
280
| Finding | Impact | Risk |
281
|----------|---------|------|
282
| Website technologies exposed | Enables technology fingerprinting | Medium |
283
| Public IP address discovery | Reveals infrastructure location | Low |
284
| HTTP headers exposed | Assists information gathering | Low |
285
| WAF identification | Reveals defensive architecture | Low |
286
| DNS records exposed | Enables infrastructure mapping | Medium |
287
| Search engine indexed cameras | Sensitive device exposure | Medium |
288
| Public email addresses | Phishing and social engineering risks | Medium |
289
| Exposed subdomains | Assists attack planning | Medium |
290
| Multiple discoverable network hosts | Expands attack surface | Medium |
291
 
292
---
293
 
294
# Recommendations
295
 
296
## Web Applications
297
 
298
- Minimize exposed technology information
299
- Regularly update CMS platforms and plugins
300
- Review HTTP response headers
301
 
302
## Infrastructure Security
303
 
304
- Audit DNS records periodically
305
- Monitor exposed assets and subdomains
306
- Maintain WAF protection
307
 
308
## Internet-Facing Devices
309
 
310
- Protect administrative interfaces
311
- Require authentication
312
- Prevent search engine indexing
313
 
314
## Email Security
315
 
316
- Limit unnecessary exposure of email addresses
317
- Conduct phishing awareness training
318
- Monitor for external exposure
319
 
320
## Network Security
321
 
322
- Maintain an updated asset inventory
323
- Perform periodic internal network scans
324
- Investigate unknown devices immediately
325
- Document network architecture
326
 
327
## Governance
328
 
329
- Conduct testing only with written authorization
330
- Maintain defined testing scopes
331
- Follow responsible disclosure practices
332
 
333
---
334
 
335
# Key Lessons Learned
336
 
337
This assessment demonstrated how attackers and security professionals can gather valuable intelligence during the early phases of a penetration test.
338
 
339
Important discoveries included:
340
 
341
- Technology fingerprinting
342
- DNS reconnaissance
343
- Email enumeration
344
- OSINT relationship mapping
345
- Search engine reconnaissance
346
- Internal network discovery
347
 
348
The exercise reinforced the importance of reducing information exposure and maintaining a strong security posture.
349
 
350
---
351
 
352
# Evidence
353
 
354
### theHarvester Enumeration
355
![EMBEDDEDIMAGE](placeholder-0)
356
 
357
### Zenmap Network Discovery
358
![EMBEDDEDIMAGE](placeholder-1)
359
 
360
### DNS and Reconnaissance Activities
361
![EMBEDDEDIMAGE](placeholder-2)
362
 
363
### Footprinting Results
364
![EMBEDDEDIMAGE](placeholder-3)
365
 
366
### Additional Scan Results
367
![EMBEDDEDIMAGE](placeholder-4)
368
 
369
---
370
 
371
# Conclusion
372
 
373
During Week 2 of the Cybersecurity & Ethical Hacking Internship at Networkwalks, practical exercises involving footprinting, OSINT gathering, reconnaissance, and network scanning were successfully completed.
374
 
375
The assessment demonstrated how publicly available information, DNS records, email addresses, subdomains, web technologies, and active network hosts can be discovered and analyzed during the initial stages of a penetration testing engagement.
376
 
377
These exercises strengthened practical skills in ethical hacking while reinforcing the importance of conducting security assessments responsibly, ethically, and within authorized boundaries.
378
 
379
---
380
 
381
**Author:** Fredrick Musonda
382
**Role:** Cybersecurity Professional
383
**Assessment Type:** Reconnaissance, Footprinting & Network Scanning
384
`
