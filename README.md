# SOC Incident Investigation – NetSupport Manager RAT

## Incident Overview

A Security Operations Center (SOC) alert identified suspicious network activity involving NetSupport Manager Remote Access Trojan (RAT) communicating with the external IP:

45.131.214.85

The malicious traffic occurred over TCP port 443 and began on:

2026-02-28 19:55 UTC

A packet capture (PCAP) was analyzed to determine which internal system within the network was compromised.

---

## Network Environment

LAN Range: 10.2.28.0/24  
Domain: easyas123.tech  
Active Directory Domain: EASYAS123  
Domain Controller: 10.2.28.2 (EASYAS123-DC)  
Gateway: 10.2.28.1  

---

## Investigation Objectives

Identify:

- Infected Windows client
- MAC address of infected host
- Hostname
- Logged-in user account
- Full name of the user

---

## Tools Used

- Wireshark
- Network protocol analysis
- Threat intelligence correlation

---

## Investigation Methodology

The PCAP file was analyzed using Wireshark.

The investigation followed these steps:

1. Identify internal host communicating with malicious infrastructure.
2. Extract host details using NBNS traffic.
3. Identify Windows authentication activity.
4. Determine user account information.

---

## Key Findings

Infected Host IP:  
10.1.28.88  

MAC Address:  
00:19:d1:b2:4d:ad  

Hostname:  
DESKTOP-TEYQ2NR  

User Account:  
brolf  

Full Name:  
Becka Rolf

---

## Indicators of Compromise

Malicious IP Address  
45.131.214.85

Protocol  
TCP 443

Malware  
NetSupport Manager RAT

---

## Attack Timeline

| Time | Event |
|------|-------|
| 19:55 | Infected host initiates connection to malicious server |
| 19:55 | TLS session established over TCP 443 |
| 19:56 | Continued encrypted communication with RAT infrastructure |

---

## MITRE ATT&CK Mapping

Technique | Description
--------- | -----------
Command and Control | Communication with external RAT infrastructure
Remote Access Software | NetSupport Manager RAT

---

## Skills Demonstrated

- Network traffic analysis
- Incident response investigation
- IOC extraction
- Threat intelligence correlation
- Wireshark forensic analysis