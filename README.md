# SOC Analyst Investigation Writeups

These are hands-on alert investigations I’ve worked through on [LetsDefend](https://letsdefend.io/), a platform that simulates a real SOC. I use this repo to practice SIEM monitoring, log analysis, threat intelligence, and incident response, and to show how I approach each one.
Each writeup walks through how I handled the alert: triage, log analysis, evidence collection, IOC checks, MITRE ATT&CK mapping, my verdict, and the response actions I’d recommend.
I use Claude as a study aid, mostly to understand attacker techniques and malware families I haven’t run into before, and to check my findings for gaps I might have missed. The investigation, evidence, and conclusions are my own, and I verify all of it myself.



# About Me

I’m Vishakh, a recent B.Sc. Computer Science graduate moving into a SOC Analyst role. I completed the Advanced Diploma in Cyber Defense (ADCD) at RedTeam Hacker Academy and hold the Certified Ethical Hacker (CEH) certification.

This portfolio is where I practice and show my work. I investigate simulated security alerts, dig into attacker techniques I’m unfamiliar with, and map what I find to the MITRE ATT&CK framework. My main focus is SOC operations, phishing email analysis, log analysis, and threat detection, which are the skills I’d use day to day in a real SOC.

Certifications: Certified Ethical Hacker (CEH) · Advanced Diploma in Cyber Defense (ADCD)

Where I practice:[LetsDefend](https://letsdefend.io/) (SOC alert investigation) · [TryHackMe](https://tryhackme.com/) (security labs) · [Hack The Box](https://www.hackthebox.com/) (hands-on challenges) · [CyberDefenders](https://cyberdefenders.org/)  (Blue Team investigations and threat hunting)



#  What This Portfolio Demonstrates

- **Incident Triage** — analysing security alerts to assess severity, investigate suspicious activities, and determine whether an alert is a True Positive or False Positive.

- **Log Analysis** — examining and correlating security logs to identify suspicious activities, investigate security events, and understand potential attack sequences.

- **Threat Intelligence Analysis** — using VirusTotal and AbuseIPDB to investigate Indicators of Compromise (IOCs), analyse suspicious IP addresses, domains, URLs, and file hashes.

- **MITRE ATT&CK Mapping** — identifying relevant attacker tactics and techniques based on observed activities during security investigations.

- **Evidence-Based Reporting** — documenting investigation steps, analysing available evidence, presenting findings, and distinguishing confirmed facts from assumptions or unresolved questions.




- ## Investigation Index – Phishing Analysis

This section documents phishing-related security alert investigations completed through the LetsDefend platform. Each investigation focuses on analysing suspicious emails, identifying malicious indicators, examining attacker techniques, and understanding appropriate incident response actions.

| No. | Alert ID | Investigation Title | Category | Key Skills |
|---|---|---|---|---|
| 01 | SOC282 | Phishing Alert | Phishing | Email Analysis, IOC Investigation |
| 02 | TBD | Phishing Email Analysis | Phishing | Email Header Analysis, SPF, DKIM, DMARC |
| 03 | TBD | Suspicious URL Detection | Phishing | URL Analysis, VirusTotal |
| 04 | TBD | Malicious Attachment Detection | Phishing | File Hash Analysis, Malware Investigation |
| 05 | TBD | Email Spoofing Detection | Phishing | Sender Verification, Email Authentication |
| 06 | TBD | QR Code Phishing (Quishing) | Phishing | URL Investigation, Threat Intelligence |

*Portfolio in progress — additional phishing investigations will be added as I complete and document more LetsDefend labs.*




## Investigation Methodology

Every case in this repository follows the same structure:

1. **Alert Summary** — What triggered the alert and the initial context.
2. **Investigation Timeline** — Reconstructed chronology of the attack.
3. **Investigation Steps** — Log analysis across SIEM, EDR, firewall, proxy, and email sources, supported by evidence screenshots.
4. **Threat Intelligence Enrichment** — IOC lookups using VirusTotal and AbuseIPDB, including crowdsourced threat context where available.
5. **MITRE ATT&CK Mapping** — Identification of relevant attacker tactics and techniques.
6. **Verdict** — True Positive or False Positive determination with clear reasoning, distinguishing confirmed findings from unconfirmed or open items.
7. **Containment & Recommendations** — Prioritized response actions and security recommendations.
8. **Closure Note** — A concise investigation summary suitable for ticket closure.
   


10. ## Tools Used

- **SIEM / Log Management:** LetsDefend platform (Exchange, Proxy, Firewall, OS/Windows Event logs, EDR process telemetry).
- **Threat Intelligence:** VirusTotal, AbuseIPDB.
- **Frameworks:** MITRE ATT&CK.
- **Research/Review Aid:** Claude (Anthropic) — Used to research unfamiliar attacker techniques and malware families, and to review my draft findings for gaps, imprecise claims, or missed evidence before finalizing each writeup.



# Repository Structure
## Repository Structure

```text
SOC-Analyst-Writeups/
│
├── README.md
│
├── Investigations/
│   │
│   ├── Brute-Force/
│   │   ├── SOC176-RDP-Brute-Force.md
│   │   └── SOC-XXX-SSH-Brute-Force.md
│   │
│   ├── Phishing/
│   │   ├── SOC282-Phishing-Alert.md
│   │   └── SOC-XXX-Email-Spoofing.md
│   │
│   ├── Malware/
│   │   ├── SOC-XXX-Malware-Detected.md
│   │   └── SOC-XXX-Suspicious-File.md
│   │
│   ├── Web-Attacks/
│   │   ├── SOC-XXX-SQL-Injection.md
│   │   ├── SOC-XXX-XSS-Attack.md
│   │   └── SOC-XXX-Directory-Traversal.md
│   │
│   └── Data-Leakage/
│       ├── SOC-XXX-Data-Exfiltration.md
│       └── SOC-XXX-Suspicious-Data-Transfer.md
│
├── Screenshots/
│   │
│   ├── SOC176/
│   ├── SOC282/
│   └── SOC-XXX/
│
└── Templates/
    └── Investigation-Template.md
```


 # Connect

- **LinkedIn:** [Your LinkedIn Profile](YOUR_LINKEDIN_URL)
- **Email:** YOUR_EMAIL
- **GitHub:** [Your GitHub Profile](YOUR_GITHUB_URL)

