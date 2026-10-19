# Wazuh SOC Investigation Lab

A training portfolio of four independent Windows/Sysmon investigations using Wazuh. The published case pages retain their original lab IDs (01, 03, 04, and 05); the capstone remains a hypothetical correlated sequence.

> **Training disclaimer:** Authorized, controlled lab and portfolio work only. This is not production SOC employment. Four genuine Wazuh dashboard overview captures are included under [screenshots/](screenshots/). They show preliminary search results, not full verification of every scenario. Each published case page states what its evidence does and does not establish. No malicious outcome or correlated incident is claimed without supporting event details.

## Lab components

| Component | Role in the lab |
|---|---|
| Wazuh | Alert and event review |
| Windows endpoint | Monitored security and system telemetry |
| Sysmon | Process telemetry when configured |
| Kali Linux / VirtualBox | Isolated test environment when used |

## Independent investigations

| Case | Focus |
|---|---|
| [01 — Failed login analysis](investigations/01-failed-login-analysis.md) | Authentication failure patterns |
| [03 — Privileged account change](investigations/03-privileged-account-change.md) | Local group membership changes |
| [04 — File integrity monitoring](investigations/04-file-integrity-monitoring.md) | Monitored file changes |
| [05 — Network reconnaissance visibility](investigations/05-network-recon-detection-gap.md) | Telemetry coverage and detection limits |

## Correlated capstone

[Correlated attack-chain case study](case-studies/correlated-attack-chain.md) is a hypothesis to validate from evidence, not a report of observed compromise. It distinguishes verified events from possible stages and treats missing telemetry as a visibility gap.

## Analyst workflow

Validate source and time window; examine event, host, account, and process context; preserve observations; assess collection limits; then document a qualified disposition. A single event does not prove intent. Map MITRE ATT&CK only when the observed behavior supports it.

## Repository map

- Four independent investigation pages: Cases 01, 03, 04, and 05
- [Correlated capstone](case-studies/correlated-attack-chain.md)
- [Screenshot guide and four overview captures](screenshots/README.md)
- [Investigation register](incident-timeline.md)
- [Lessons learned](lessons-learned.md)

## Evidence and lab safety

Screenshots belong under [screenshots/](screenshots/) and must come from the actual lab. See the [capture guide](screenshots/README.md) for the four published overview captures and their limitations. Redact credentials, tokens, and unrelated personal data before publishing further detail. Use only isolated systems and accounts authorized for testing; keep exercises scoped and reversible.
