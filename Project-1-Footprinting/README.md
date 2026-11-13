# `NEXUS // MODULE 01`

## WEBSITE FOOTPRINTING & RECONNAISSANCE

<p align="center">
  <img src="https://img.shields.io/badge/MODULE-01-00ff9c?style=for-the-badge&labelColor=080d12" />
  <img src="https://img.shields.io/badge/PHASE-RECONNAISSANCE-00d9ff?style=for-the-badge&labelColor=080d12" />
  <img src="https://img.shields.io/badge/STATUS-COMPLETED-00ff9c?style=for-the-badge&labelColor=080d12" />
</p>

<p align="center">
  <code>root@nexus:~$ ./footprinting.sh --target networkwalks.com</code>
</p>

---

## `01` // MISSION BRIEF

**Target:** `networkwalks.com`

**Assessment:** Website Footprinting

**Environment:** Kali Linux

The objective of this practical task was to gather publicly observable information about the target domain and examine its website technologies, DNS information, HTTP response characteristics and WAF indicators.

The collected information was documented through terminal outputs and screenshots.

## `02` // RECONNAISSANCE TOOLKIT

| TOOL | FUNCTION |
|---|---|
| WHOIS | Domain registration information |
| WhatWeb | Website technology fingerprinting |
| Nslookup | DNS resolution |
| cURL | HTTP response inspection |
| WAFW00F | WAF identification |
| DNSRecon | DNS enumeration |

## `03` // ATTACK-SURFACE DISCOVERY FLOW

```text
 TARGET: networkwalks.com
             |
     +-------+-------+
     |       |       |
   WHOIS  WHATWEB  NSLOOKUP
     |       |       |
     +-------+-------+
             |
       HTTP ANALYSIS
             |
        WAF DETECTION
             |
       DNS ENUMERATION
             |
      EVIDENCE REVIEW
```

## `04` // TASK EXECUTION

### `TASK_01` — WHOIS INTELLIGENCE

**Objective:** Retrieve publicly available domain registration information.

**Command:**

```bash
whois networkwalks.com
```

**Evidence files:**

- [WHOIS Screenshot 01](./task1-whois-1.png)
- [WHOIS Screenshot 02](./task1-whois-2.png)
- [WHOIS Terminal Output](./task1-whois.txt)

---

### `TASK_02` — TECHNOLOGY FINGERPRINTING

**Tool:** WhatWeb

**Objective:** Identify technologies and frameworks observable on the website.

**Command:**

```bash
whatweb https://networkwalks.com
```

**Observed technologies:**

| Component | Observation |
|---|---|
| Web Server | Apache |
| CMS | WordPress 7.1.4 |
| Plugin | WordPress Download Manager 3.3.76 |
| JavaScript Library | jQuery 3.7.1 |
| Framework | Bootstrap |

**Evidence:**

- [WhatWeb Screenshot](./task2-whatweb.png)
- [WhatWeb Output](./task2-whatweb.txt)

---

### `TASK_03` — DNS INTELLIGENCE

**Tool:** Nslookup

**Objective:** Resolve the target domain and examine its DNS response.

**Command:**

```bash
nslookup networkwalks.com
```

**Observed result:**

```text
TARGET   : networkwalks.com
IP       : 192.232.216.135
```

**Evidence:**

- [DNS Lookup Screenshot](./task3-nslookup.png)
- [DNS Lookup Output](./task3-nslookup.txt)

---

### `TASK_04` — HTTP RESPONSE ANALYSIS

**Tool:** cURL

**Objective:** Inspect HTTP response headers returned by the target website.

**Command:**

```bash
curl -I https://networkwalks.com
```

**Observations:**

- HTTP/2 200 response.
- Apache server information observed.
- WordPress REST API reference observed in the response headers.

**Evidence:**

- [HTTP Header Screenshot](./task4-curl-headers.png)
- [HTTP Header Output](./task4-curl-headers.txt)

---

### `TASK_05` — WAF IDENTIFICATION

**Tool:** WAFW00F

**Objective:** Check for identifiable Web Application Firewall indicators.

**Command:**

```bash
wafw00f https://networkwalks.com
```

**Observation:**

WAFW00F identified ModSecurity (SpiderLabs) as a WAF indicator.

**Evidence:**

- [WAF Detection Screenshot](./task5-wafw00f.png)
- [WAF Detection Output](./task5-wafw00f.txt)

---

### `TASK_06` — DNS ENUMERATION

**Tool:** DNSRecon

**Objective:** Perform DNS enumeration against the target domain.

**Command:**

```bash
dnsrecon -d networkwalks.com
```

**Evidence:**

- [DNSRecon Screenshot](./task6-dnsrecon.png)
- [DNSRecon Output](./task6-dnsrecon.txt)

## `05` // RECONNAISSANCE INTELLIGENCE SUMMARY

| Assessment Area | Observation |
|---|---|
| Target Domain | `networkwalks.com` |
| Resolved IP | `192.232.216.135` |
| Web Server | Apache |
| CMS | WordPress |
| HTTP Response | HTTP/2 200 |
| WAF Indicator | ModSecurity (SpiderLabs) |
| DNS Enumeration | Performed |

## `06` // ANALYST NOTES

Technology fingerprinting and WAF identification provide useful reconnaissance information, but they do not independently prove that a vulnerability exists.

The collected observations represent the information visible during the assessment. No exploitation or vulnerability validation was performed.

## `07` // SKILLS DEVELOPED

- Domain reconnaissance.
- Website technology identification.
- DNS lookup and enumeration.
- HTTP response analysis.
- WAF detection.
- Evidence collection and documentation.

---

<p align="center">
  <code>root@nexus:~$ module_01 --complete</code>
  <br/><br/>
  <strong>NEXUS // RECONNAISSANCE DIVISION</strong>
  <br/>
  <sub>INFORMATION GATHERING • TECHNICAL ANALYSIS</sub>
</p>
