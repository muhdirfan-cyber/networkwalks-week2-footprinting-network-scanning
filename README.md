# `CYBER OPERATIONS`

<p align="center">
  <img src="https://img.shields.io/badge/NEXUS-CYBER_OPERATIONS-00ff9c?style=for-the-badge&labelColor=080d12" />
  <img src="https://img.shields.io/badge/NETWORKWALKS-WEEK_02-00d9ff?style=for-the-badge&labelColor=080d12" />
  <img src="https://img.shields.io/badge/STATUS-COMPLETED-00ff9c?style=for-the-badge&labelColor=080d12" />
</p>

<p align="center">
  <strong>RECONNAISSANCE // ENUMERATION // NETWORK DISCOVERY</strong>
  <br/>
  <code>root@nexus:~$ ./launch-assessment.sh</code>
</p>

---

## `01` // SYSTEM OVERVIEW

> Initializing Week 02 cybersecurity practical assessment...

This repository contains my Week 02 practical work as part of the **NetworkWalks Cybersecurity Internship**.

The assessment focuses on two foundational penetration-testing activities: website footprinting and network scanning.

The objective was to understand how information can be gathered, analyzed, and documented during the early stages of a security assessment.

```text
[ASSESSMENT CONFIGURATION]

PROGRAM       : NetworkWalks Internship
MODULE        : Week 02
PHASE 01      : Website Footprinting
PHASE 02      : Network Scanning
ENVIRONMENT   : Kali Linux
DOCUMENTATION : Technical Evidence & Final Report

[INITIALIZATION COMPLETE]
```

## `02` // MISSION MODULES

### <code>MODULE_01 :: WEBSITE FOOTPRINTING</code>

**Target:** `networkwalks.com`

Information gathering and reconnaissance using publicly observable website and domain information.

| Tool | Operation |
|---|---|
| WHOIS | Domain information lookup |
| WhatWeb | Technology identification |
| Nslookup | DNS lookup |
| cURL | HTTP header inspection |
| WAFW00F | WAF detection |
| DNSRecon | DNS enumeration |

**Module output:** Domain, DNS, website technology and HTTP-related observations.

[ `ACCESS MODULE 01 →` ](./Project-1-Footprinting/README.md)

---

### <code>MODULE_02 :: NETWORK SCANNING</code>

**Target:** Personal VirtualBox NAT Network

Host discovery and network scanning using Zenmap and Nmap within a controlled virtual lab.

| Tool | Operation |
|---|---|
| Zenmap | Graphical network scanning |
| Nmap | Host discovery |
| Kali Linux | Scanning environment |
| VirtualBox | Lab virtualization |

**Module output:** Network configuration, live hosts, IP addresses and MAC address observations.

[ `ACCESS MODULE 02 →` ](./Project-5-Zenmap/README.md)

---

## `03` // OPERATIONAL WORKFLOW

```text
                  ┌──────────────────────┐
                  │   INITIALIZATION     │
                  │   NETWORKWALKS W02   │
                  └──────────┬───────────┘
                             |
                  ┌──────────▼───────────┐
                  │   RECONNAISSANCE     │
                  │   WEBSITE FOOTPRINT  │
                  └──────────┬───────────┘
                             |
                  ┌──────────▼───────────┐
                  │   DNS & WEB ANALYSIS │
                  │   ENUMERATION        │
                  └──────────┬───────────┘
                             |
                  ┌──────────▼───────────┐
                  │   NETWORK DISCOVERY  │
                  │   ZENMAP / NMAP      │
                  └──────────┬───────────┘
                             |
                  ┌──────────▼───────────┐
                  │   EVIDENCE REVIEW    │
                  │   REPORT GENERATION  │
                  └──────────────────────┘
```

## `04` // ENVIRONMENT & CONFIGURATION

| Component | Configuration |
|---|---|
| Operating System | Kali Linux |
| Virtualization | Oracle VirtualBox |
| Network Interface | `eth0` |
| Lab IP Address | `10.0.0.2/24` |
| Default Gateway | `10.0.0.1` |
| Lab Subnet | `10.0.0.0/24` |
| Scanning Tool | Zenmap / Nmap |

## `05` // INTELLIGENCE SUMMARY

<details>
<summary><strong>MODULE 01 — FOOTPRINTING OBSERVATIONS</strong></summary>

- Apache web server identified.
- WordPress technology detected.
- Domain resolved to `192.232.216.135`.
- HTTP/2 200 response observed.
- ModSecurity (SpiderLabs) identified by WAFW00F.
- DNS enumeration performed.

</details>

<details>
<summary><strong>MODULE 02 — NETWORK DISCOVERY RESULTS</strong></summary>

| Metric | Result |
|---|---|
| Subnet | `10.0.0.0/24` |
| Addresses scanned | 256 |
| Live hosts | 2 |
| Gateway | `10.0.0.1` |
| Kali VM | `10.0.0.2` |
| Gateway MAC | `52:54:00:12:35:00` |

</details>

## `06` // REPOSITORY ARCHITECTURE

```text
NETWORKWALKS-WEEK02/
│
├── README.md
│
├── Project-1-Footprinting/
│   ├── README.md
│   ├── Screenshots
│   └── Output Files
│
├── Project-5-Zenmap/
│   ├── README.md
│   ├── Screenshots
│   ├── Output Files
│   └── Network Topology
│
└── W2-PM6-Final-Report.pdf
```

## `07` // EVIDENCE & DOCUMENTATION

All task-level screenshots and command outputs are organized inside their respective project directories.

**Final assessment report:**

[ `VIEW WEEK 02 FINAL REPORT (PDF) →` ](./W2-PM6-Final-Report.pdf)

## `08` // SECURITY & SCOPE

- Website footprinting was conducted as an educational information-gathering exercise.
- Network scanning was performed inside my own VirtualBox lab.
- No exploitation or unauthorized access was performed.
- Findings are limited to the evidence collected during the exercises.

## `09` // SKILLS DEVELOPED

`RECONNAISSANCE` `WHOIS` `DNS ENUMERATION` `WHATWEB` `HTTP ANALYSIS` `WAF DETECTION` `NMAP` `ZENMAP` `HOST DISCOVERY` `TECHNICAL REPORTING`

---

<p align="center">
  <code>root@nexus:~$ exit</code>
  <br/><br/>
  <strong>NEXUS // NETWORKWALKS WEEK 02</strong>
  <br/>
  <sub>LEARN THE SYSTEM. UNDERSTAND THE NETWORK. SECURE THE ENVIRONMENT.</sub>
</p>
