# SOC Incident Report: Ransomware Execution (Win32/Phobos)

## Case Overview
- **Case ID:** da3b694398-e332-4e1a-b15e-effc185977c9_1
- **Incident Title:** Ransomware Execution – Win32/Phobos
- **Date:** February 4, 2026
- **Severity:** High
- **Status:** Contained
- **Affected Host:** MTS-ContractorPC1

---

## Executive Summary
On February 4, 2026, ransomware activity associated with **Win32/Phobos** was detected on contractor workstation **MTS-ContractorPC1** under the **Administrator account**.

Multiple malicious executables were discovered, including ransomware and trojan-related files. External IP communications were also identified, indicating possible command-and-control activity.

Endpoint isolation and remediation actions were performed to contain the threat.

:contentReference Ransomware and trojan executables were detected under the administrator account with external IP communication observed.

---

## Investigation Timeline (UTC)

| Time | Event |
|------|------|
| 13:13:41 | Suspicious executable files detected |
| 13:14:05 | Ransomware alert triggered |
| 13:15:10 | Trojan detected in mouselock.exe |
| 13:16:30 | External IP communication observed |
| 13:18:00 | Host isolated from network |

:contentReference Host isolation occurred shortly after ransomware and trojan activity was detected.

---

## Incident Details (Who, What, When, Where, Why, How)

| Category | Details |
|---------|--------|
| Who | Administrator account |
| What | Ransomware and trojan execution |
| When | February 4, 2026 |
| Where | Contractor workstation |
| Why | Financially motivated ransomware attack |
| How | Malicious files executed with admin privileges |

---

## Affected System
- **Device:** MTS-ContractorPC1
- **User:** administrator
- **Parent Process:** explorer.exe

---

## Malicious Files Observed
- `.bug_osn.exe` (Ransomware: Win32/Phobos)
- `.bug_hand.exe`
- `NS.exe`
- `mouselock.exe` (Trojan: Win32/Casdet)
- `Advanced_IP_Scanner.exe`
- `everything.exe`

:contentReference - Multiple ransomware and trojan-related executables were present on the affected system.

---

## Indicators of Compromise (IOCs)

### File Hashes
- 26d5748ffe6bd95e3fee6ce184d388a1a681006dc23a0f08d53c083c593c193b
- b757cdd37ea2d179996a8f9452c1747867d2a26d8f4377985b7bcca1e0aa6c38
- f47e3555461472f23ab4766e4d5b6f6fd260e335a6abc31b860e569a720a5446
- f3ad7f8f00ffe7efce17f6b5b8667ef82c6df2c655bbafa9b637657465403a85


### Suspicious IPs
- 95.216.37.156
- 84.8.107.159
- 178.57.110.29
- 109.205.211.14

:contentReference - External IP communication was detected during the incident.

---

## MITRE ATT&CK Mapping

| Technique | Description |
|----------|-------------|
| T1486 | Data Encrypted for Impact |
| T1204 | User Execution |
| T1071 | Application Layer Protocol |

---

## Impact Assessment
- Ransomware artifacts detected.
- Administrator account involved.
- Presence of network scanning tools.
- High risk of system compromise.

:contentReference - Administrator account involvement increased risk severity.

---

## Containment Actions
- Host isolated from the network.
- Malicious files quarantined.
- External IPs blocked.
- Administrator credentials reset.

---

## Eradication and Recovery
- Full malware scan executed.
- System scheduled for reimaging.
- Password resets performed.
- Security patches verified.

---

## Root Cause
Likely execution of malicious files with administrator privileges.

---

## Security Recommendations
1. Enforce MFA for remote access.
2. Disable direct administrator logins.
3. Restrict RDP through VPN.
4. Implement application allow-listing.
5. Conduct enterprise IOC scans.
6. Provide security awareness training.

---

## Tools Used
- Microsoft Defender for Endpoint
- Endpoint Isolation
- IOC Analysis
- Threat Intelligence Correlation

---

## Skills Demonstrated
- Ransomware investigation
- Endpoint forensics
- IOC analysis
- Incident containment
- MITRE ATT&CK mapping
- SOC reporting
