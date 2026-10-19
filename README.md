# Wazuh SOC Investigation Lab

A training portfolio of independent Windows/Sysmon investigations using Wazuh. The seven cases below are separate scenarios; only the capstone presents a hypothetical correlated sequence.

> **Training disclaimer:** Authorized, controlled lab and portfolio work only. This is not production SOC employment. Investigation observations and screenshots remain pending until captured from the actual lab; no evidence or exact event values are invented.

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
| [02 — Suspicious PowerShell](investigations/02-suspicious-powershell.md) | Process lineage and command context |
| [03 — Privileged account change](investigations/03-privileged-account-change.md) | Local group membership changes |
| [04 — File integrity monitoring](investigations/04-file-integrity-monitoring.md) | Monitored file changes |
| [05 — Network reconnaissance visibility](investigations/05-network-recon-detection-gap.md) | Telemetry coverage and detection limits |
| [06 — False-positive triage](investigations/06-false-positive-triage.md) | Attribution of an expected file update |
| [07 — Scheduled-task review](investigations/07-scheduled-task-persistence.md) | Task creation/change review |

## Correlated capstone

[Correlated attack-chain case study](case-studies/correlated-attack-chain.md) is a hypothesis to validate from evidence, not a report of observed compromise. It distinguishes verified events from possible stages and treats missing telemetry as a visibility gap.

## Analyst workflow

Validate source and time window; examine event, host, account, and process context; preserve observations; assess collection limits; then document a qualified disposition. A single event does not prove intent. Map MITRE ATT&CK only when the observed behavior supports it.

## Repository map

```text
Wazuh-SOC-Investigation-Lab/
├── README.md
├── investigations/ (seven independent cases)
├── case-studies/correlated-attack-chain.md
├── screenshots/README.md
├── incident-timeline.md
└── lessons-learned.md
```

## Evidence and lab safety

Screenshots belong under [screenshots/](screenshots/) and must come from the actual lab. See the [capture checklist](screenshots/README.md). Redact credentials, tokens, and unrelated personal data. Use only isolated systems and accounts authorized for testing; keep exercises scoped and reversible.
