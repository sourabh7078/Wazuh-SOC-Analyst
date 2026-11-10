# Wazuh SOC Home Lab — 22-Day Practical Project

A hands-on Security Operations Center (SOC) home-lab project documenting Wazuh deployment, endpoint onboarding, security telemetry, Windows event monitoring, and investigation exercises.

> **Evidence note:** The original `Wazuh.zip` supplied for this project contained 242 screenshots. The prepared package preserves their filenames and capture dates and includes a SHA-256 manifest. Screenshot dates are not automatically mapped to Day 1–22 because the archive did not contain a verified day-to-date mapping.

## Project goals
- Deploy and operate a Wazuh manager in an isolated virtual lab.
- Enroll and monitor Windows, Kali Linux, and Ubuntu endpoints.
- Collect and review endpoint telemetry and security events.
- Enable and validate Windows audit telemetry, including process creation monitoring.
- Practice alert triage, event validation, investigation, and evidence documentation.

## Lab environment
| Component | Role |
|---|---|
| Wazuh Manager | Ubuntu-based Wazuh server and dashboard |
| Windows 11 endpoint | Windows endpoint telemetry and Sysmon |
| Kali Linux | Linux endpoint monitoring and security testing |
| Ubuntu endpoint | Linux endpoint monitoring |
| Windows Server 2022 | Active Directory lab environment |
| Virtualization | VMware Workstation Pro; isolated/NAT lab networking |

## Work documented
- Wazuh manager and dashboard health checks.
- Agent enrollment and status verification for Windows, Kali, and Ubuntu.
- Windows Security auditing and logon event review.
- Sysmon telemetry collection and validation.
- Process creation auditing using Windows Security Event ID 4688.
- Wazuh rule validation, custom local rules, and endpoint process monitoring.

The source archive also contains a CIS Windows 11 Enterprise assessment export (`checks.csv`). It is a configuration-assessment artifact, not Wazuh alert output.

## Repository layout
- `docs/PROJECT-PLAN.md` — template for documenting each practical day.
- `docs/PUBLIC-RELEASE-CHECKLIST.md` — security review before public sharing.
- `evidence/DATE-WISE-INDEX.md` — date-wise screenshot counts for all 22 capture dates.
- `evidence/SCREENSHOT-MANIFEST.csv` — screenshot inventory and SHA-256 hashes (included in the prepared ZIP).
- `evidence/assessment/checks.csv` — assessment export from the supplied archive.
- `evidence/screenshots/YYYY-MM-DD/` — original screenshots grouped by capture date in the prepared ZIP; binary images still need to be uploaded to this repository.

## Evidence inventory
- Screenshots in source archive: **242**
- Capture dates: **22** (2026-09-23 through 2026-11-09)
- Date-wise index: [`evidence/DATE-WISE-INDEX.md`](evidence/DATE-WISE-INDEX.md)
- Date range: **2026-09-23 to 2026-11-09**
- Assessment CSV records: **482** (123 passed / 351 failed)

## Suggested 22-day documentation index
| Day | Focus |
|---:|---|
| 01 | Lab planning and architecture |
| 02 | Wazuh manager installation and validation |
| 03 | Dashboard access and health checks |
| 04 | Windows endpoint onboarding |
| 05 | Agent connectivity and status checks |
| 06 | Windows event collection |
| 07 | Sysmon installation and configuration |
| 08 | Sysmon event validation |
| 09 | Linux endpoint onboarding |
| 10 | Linux telemetry review |
| 11 | Active Directory lab integration |
| 12 | Authentication event monitoring |
| 13 | Failed logon investigation |
| 14 | Alert triage fundamentals |
| 15 | Wazuh rules and severity review |
| 16 | Custom rule preparation |
| 17 | Rule validation and troubleshooting |
| 18 | Practical monitoring and investigation notes |
| 19 | Endpoint telemetry review |
| 20 | Windows audit policy validation |
| 21 | Process creation auditing — Event ID 4688 |
| 22 | Process monitoring and alert review |

This is a suggested index, not a claim that every topic is independently proven by a particular screenshot. Mark a day complete only after matching its notes and evidence to the actual session.

## Safe lab practices
1. Keep the manager and agents on a private, authorized lab network.
2. Verify manager and agent health before generating test events.
3. Generate only benign, controlled test activity on systems you own or are authorized to test.
4. Confirm events reach Wazuh; record timestamp, agent, rule ID, severity, and investigation outcome.
5. Add a `Day-XX.md` note with objective, commands, validation, evidence, and lessons learned.

## Disclaimer
For education, defensive security monitoring, and authorized lab use only. Do not test systems without permission.

## Evidence safety
Before publishing screenshots, inspect and redact credentials, enrollment keys, private keys, internal IPs, hostnames, usernames, personal data, and organization details. Do not expose dashboards or management services to the public internet.
