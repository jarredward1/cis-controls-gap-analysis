# CIS Controls v8 Gap Analysis: Luigi's Inc. Incident Case Study

> A CIS Controls v8 gap analysis of a network intrusion at a fictional company, Luigi's Inc., mapping the incident's root causes to the specific CIS Controls and Safeguards that would have prevented or reduced the impact of the attack.

---

## 📌 Overview

Luigi's Inc. suffered a data breach after an employee connected a personal laptop, unknowingly infected with malware, to the corporate wireless network. The device received a corporate IP address, scanned the internal network on the attacker's command, and located an anonymously-accessible internal FTP server. Over a three-day holiday weekend, the attacker exfiltrated patents, proprietary drawings, price quotes, and legal documents over an encrypted VPN tunnel while the resulting anomaly was handled as a routine help-desk ticket.

This gap analysis identifies the security and process failures that allowed the incident to occur and maps each failure to the CIS Controls v8 and Safeguards Luigi's should implement to prevent recurrence.

---

## 🏢 Case Study

[View the case study (PDF)](./Luigis_Company_Case_Study.pdf)

### Incident Summary

- An employee brought an **infected personal laptop** into the facility and connected it to the corporate wireless network
- The device received a **corporate IP address via DHCP** with no verification of ownership or security posture
- The malware (**PSL**) connected to a command-and-control server, which then directed the laptop to scan the internal network
- The scan found an **internal FTP server with anonymous access** enabled
- The attacker exfiltrated **patents, proprietary drawings, price quotes, and legal documents** over an encrypted outbound VPN connection
- The NOC observed the large encrypted transfer but lacked **correlated evidence** to recognize it as a security incident
- The organization's malicious-destination list was **four months out of date**
- The incident was treated as a **routine desktop-support ticket** and closed once the laptop was confiscated, without a full investigation

---

## 🎯 Objectives

- Identify every security control and process gap that contributed to the Luigi's Inc. incident
- Map each gap to the relevant CIS Controls v8 Control and Safeguard
- Explain why each Control would have helped prevent, detect, or contain the attack
- Recommend specific Safeguards for implementation, prioritized by IG1 baseline requirements

---

## 🛠️ CIS Controls Applied

| CIS Control | Title |
|---|---|
| 1 | Inventory and Control of Enterprise Assets |
| 2 | Inventory and Control of Software Assets |
| 3 | Data Protection |
| 4 | Secure Configuration of Enterprise Assets and Software |
| 5 | Account Management |
| 6 | Access Control Management |
| 7 | Continuous Vulnerability Management |
| 8 | Audit Log Management |
| 9 | Email and Web Browser Protections |
| 10 | Malware Defenses |
| 11 | Data Recovery |
| 12 | Network Infrastructure Management |
| 13 | Network Monitoring and Defense |
| 14 | Security Awareness and Skills Training |
| 15 | Service Provider Management |
| 17 | Incident Response Management |

---

## 🔍 Key Issues Identified

The full report documents 28 distinct issues; the most significant include:

1. **Unauthorized personal device access** — no BYOD policy, device verification, or endpoint protection check before granting network access
2. **Excessively permissive DHCP and network access** — an unmanaged device received a full corporate IP address
3. **Exposed, anonymously-accessible FTP service** — sensitive files reachable without authentication
4. **Default-allow firewall posture** — no default-deny egress/ingress policy
5. **No data classification or sensitivity-based segmentation** — proprietary and legal records stored without restricted access
6. **Outdated threat intelligence** — malicious-destination list four months stale
7. **Insufficient log correlation and monitoring** — indicators existed but were never correlated into a single incident
8. **No inactivity session lock** — device stayed authenticated and connected throughout the weekend
9. **Weak after-hours incident escalation** — response delayed until the following business day
10. **Incomplete incident response** — ticket closed before containment, scoping, or root-cause review were complete

See the [full gap analysis](./CIS_Controls_Gap_Analysis.pdf) for the complete list of issues and Safeguard-level recommendations.

---

## 📄 Documents

[View the full CIS Controls gap analysis (PDF)](./CIS_Controls_Gap_Analysis.pdf)

[View the case study (PDF)](./Luigis_Company_Case_Study.pdf)

---

## 👥 Project Team

This was a group engagement completed by:

- Stephanie Greene
- Kayla Hodge
- Mark VanDike
- Jarred Ward

---

## 👤 Author

**Jarred Ward**

[![LinkedIn](https://img.shields.io/badge/LinkedIn-blue?logo=linkedin&style=for-the-badge)](https://www.linkedin.com/in/jarredward1/)
