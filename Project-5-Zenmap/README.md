# `NEXUS // MODULE 02`

## NETWORK SCANNING & HOST DISCOVERY

<p align="center">
  <img src="https://img.shields.io/badge/MODULE-02-00ff9c?style=for-the-badge&labelColor=080d12" />
  <img src="https://img.shields.io/badge/TOOL-ZENMAP_7.99-00d9ff?style=for-the-badge&labelColor=080d12" />
  <img src="https://img.shields.io/badge/STATUS-COMPLETED-00ff9c?style=for-the-badge&labelColor=080d12" />
</p>

<p align="center">
  <code>root@nexus:~$ nmap -sn 10.0.0.0/24</code>
</p>

---

## `01` // MISSION BRIEF

**Assessment:** Network Scanning

**Target Network:** `10.0.0.0/24`

**Scanning Environment:** Kali Linux on VirtualBox

**Primary Tools:** Zenmap and Nmap

The objective was to understand network discovery and identify active hosts within a controlled virtual network.

The exercise covered scanning-tool identification, local network configuration, ping scanning, live-host counting, IP identification and MAC address analysis.

## `02` // LAB CONFIGURATION

| Component | Configuration |
|---|---|
| Operating System | Kali Linux |
| Virtualization | Oracle VirtualBox |
| Scanning Interface | Zenmap |
| Nmap Version | 7.99 |
| Network Interface | `eth0` |
| Kali IP | `10.0.0.2/24` |
| Gateway | `10.0.0.1` |
| Subnet | `10.0.0.0/24` |
| Scan Type | Ping Scan |

## `03` // NETWORK TOPOLOGY

```text
               VIRTUALBOX NAT NETWORK
                     10.0.0.0/24
                           |
                +----------+----------+
                |                     |
           10.0.0.1               10.0.0.2
         NAT GATEWAY             KALI LINUX
                                    eth0
```

**Topology evidence:**

- [Open Network Topology PNG](./zenmap-topology.png)
- [Open Network Topology PDF](./zenmap-topology.pdf)
- [Zenmap Topology Screenshot](./09-zenmap-topology.png)

## `04` // SCAN EXECUTION

### `TASK_01` — SCANNING TOOL IDENTIFICATION

**Objective:** Identify the installed Zenmap version.

**Command:**

```bash
zenmap --version
```

**Recorded version:** `7.99`

**Evidence:**

- [Zenmap Version Screenshot](./01-zenmap-version.png)
- [Terminal Output](./task1-zenmap-version.txt)

---

### `TASK_02` — NETWORK INTERFACE ANALYSIS

**Objective:** Examine local IP addressing and routing configuration.

**Commands:**

```bash
ip addr
ip route
```

**Observed configuration:**

```text
INTERFACE : eth0
IP        : 10.0.0.2/24
GATEWAY   : 10.0.0.1
NETWORK   : 10.0.0.0/24
```

**Evidence:**

- [Local IP and Subnet Screenshot](./02-local-ip-subnet.png)
- [Network Configuration Output](./task2-network-info.txt)

---

### `TASK_03` — PING SCAN

**Objective:** Discover active hosts in the configured subnet.

**Command:**

```bash
nmap -sn 10.0.0.0/24
```

**Scan parameters:**

| Parameter | Value |
|---|---|
| Scan Type | Host Discovery |
| Network | `10.0.0.0/24` |
| Address Range | 256 addresses |

**Result:** 2 live hosts discovered.

**Evidence:**

- [Live Host Discovery Screenshot](./03-live-host-discovery.png)
- [Zenmap Ping Scan Screenshot](./08-zenmap-ping-scan.png)
- [Ping Scan Output](./task3-ping-scan.txt)

---

### `TASK_04` — LIVE HOST COUNT

**Objective:** Determine the number of active hosts detected.

**Scan result:**

```text
TOTAL ADDRESSES : 256
LIVE HOSTS      : 2
```

**Evidence:**

- [Live Host Count Screenshot](./04-live-host-count.png)
- [Live Host Count Output](./task4-live-host-count.txt)

---

### `TASK_05` — IP ADDRESS IDENTIFICATION

**Objective:** Identify the IP addresses of discovered hosts.

**Discovered hosts:**

| IP Address | Identification |
|---|---|
| `10.0.0.1` | Virtual Network Gateway |
| `10.0.0.2` | Kali Linux VM |

**Evidence:**

- [Live IP Addresses Screenshot](./05-live-ip-addresses.png)
- [IP Address Output](./task5-live-ip-addresses.txt)

---

### `TASK_06` — MAC ADDRESS ANALYSIS

**Objective:** Examine MAC address information returned by the network scan.

**Observed gateway MAC:**

```text
52:54:00:12:35:00
```

**Vendor identification:** QEMU virtual NIC.

**Additional observation:** The Kali VM's MAC address was not displayed in the scan results.

**Evidence:**

- [MAC Address Screenshot](./06-live-host-mac.png)
- [MAC Address Output](./task6-mac-addresses.txt)

## `05` // NETWORK INTELLIGENCE

| Metric | Result |
|---|---|
| Network | `10.0.0.0/24` |
| Addresses Scanned | 256 |
| Live Hosts | 2 |
| Gateway IP | `10.0.0.1` |
| Kali VM IP | `10.0.0.2` |
| Gateway MAC | `52:54:00:12:35:00` |
| MAC Vendor | QEMU virtual NIC |

## `06` // ZENMAP VISUALIZATION

Zenmap provides a graphical interface for Nmap, making it easier to configure scans, inspect results and visualize discovered hosts.

**Interface evidence:**

- [Zenmap Interface](./07-zenmap-interface.png)
- [Zenmap Topology](./09-zenmap-topology.png)

## `07` // ANALYST NOTES

- The scan was performed inside my own VirtualBox NAT Network.
- Host discovery identified two live hosts in the scanned subnet.
- The gateway MAC address was visible in the scan results.
- The Kali VM's MAC address was not displayed by the scan.
- The exercise focused on network discovery, not exploitation.

## `08` // SKILLS DEVELOPED

`NMAP` `ZENMAP` `PING SCANNING` `NETWORK INTERFACES` `IP ADDRESSING` `SUBNETTING` `HOST DISCOVERY` `MAC ANALYSIS` `EVIDENCE DOCUMENTATION`

---

<p align="center">
  <code>root@nexus:~$ module_02 --complete</code>
  <br/><br/>
  <strong>NEXUS // NETWORK DISCOVERY DIVISION</strong>
  <br/>
  <sub>SCAN • IDENTIFY • ANALYZE • DOCUMENT</sub>
</p>
