# NETWORK-SECURITY-ANALYSIS

## Objective
To perform a comprehensive security analysis of a network, identify vulnerabilities, misconfigurations, and provide remediation recommendations.

## Tools Used
- Nmap – Network mapping and port scanning
- Nessus / OpenVAS – Vulnerability scanning
- Wireshark – Packet analysis (optional)

## Network Scope
- IP Range: 192.168.1.0/24
- Devices: 15 (Workstations, Servers, IoT, Printer)

## Findings Summary

| Severity | Finding | Affected Device | Recommendation |
|----------|---------|----------------|----------------|
| Critical | Open Telnet port (23) | Printer-01 | Disable Telnet, use SSH |
| High | SMBv1 enabled | FileServer | Upgrade SMB or disable v1 |
| Medium | Weak SSH ciphers | LinuxServer | Update sshd_config |
| Low | ICMP timestamp replies | Router | Block ICMP timestamp requests |

## Open Ports (Nmap Scan)

PORT     STATE    SERVICE
22/tcp   open     SSH
23/tcp   open     Telnet
80/tcp   open     HTTP
443/tcp  open     HTTPS
445/tcp  open     SMB


## Risk Assessment
- Overall Risk Level: **Medium-High**
- Exploitable vulnerabilities: 2 critical, 4 high

## Remediation Plan

| Priority | Action | Timeline |
|----------|--------|----------|
| 1 | Disable Telnet, enable SSH | Immediate |
| 2 | Disable SMBv1 | Within 24 hours |
| 3 | Update SSH cipher suites | Within 1 week |

## Author
rashmivanneladas-arch


