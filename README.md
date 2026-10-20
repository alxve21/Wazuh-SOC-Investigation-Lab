# Wazuh SOC Investigation Lab

A Windows endpoint investigation lab using Wazuh, Windows Security events, Sysmon, and file-integrity and network telemetry. The repository contains seven independent case studies and a separate capstone hypothesis. The cases describe the available lab observations and their limits; they do not claim a confirmed compromise or a single connected incident.

## Investigations

| Case | Topic | Current assessment |
|---|---|---|
| [01 — Failed login analysis](investigations/01-failed-login-analysis.md) | Windows 4625 events | Seven results appear in a broad search; a password-spray pattern is not established. |
| [02 — Office-launched PowerShell](investigations/02-suspicious-powershell.md) | Sysmon process lineage | The available process capture does not show Office-launched PowerShell. |
| [03 — Privileged group change](investigations/03-privileged-account-change.md) | Windows 4732 events | Two results appear; actor, member, and authorization are not verified. |
| [04 — File integrity monitoring](investigations/04-file-integrity-monitoring.md) | Wazuh Syscheck | Four results appear; the dedicated marker-file exercise is not verified. |
| [05 — Network visibility review](investigations/05-network-recon-detection-gap.md) | Sysmon network events | Seventy results appear; the documented probe is not verified. |
| [06 — False-positive triage](investigations/06-false-positive-triage.md) | Software-update attribution | Available details do not establish an authorized updater; disposition is inconclusive. |
| [07 — Scheduled-task review](investigations/07-scheduled-task-persistence.md) | Windows task events | No matching result was found in the reviewed search; coverage is unknown. |

Cases 01, 03, 04, and 05 have overview screenshots. Cases 02, 06, and 07 are text-only records of the review and its limits; they do not depend on screenshots to explain the question or assessment. The [screenshot guide](screenshots/README.md) describes exactly what each published capture shows.

## Correlated capstone

[Correlated attack-chain case study](case-studies/correlated-attack-chain.md) is a hypothesis for future validation. The separate case searches do not establish a shared host, actor, or sequence.

## Lab approach

Use authorized, isolated lab systems. Start with the event source and time range, inspect host, account, process, and event details, then record what the data supports and what remains unknown. A search result alone does not establish intent. Map MITRE ATT&CK only when the observed behavior supports it.

## Repository map

- Seven independent investigations: [01](investigations/01-failed-login-analysis.md), [02](investigations/02-suspicious-powershell.md), [03](investigations/03-privileged-account-change.md), [04](investigations/04-file-integrity-monitoring.md), [05](investigations/05-network-recon-detection-gap.md), [06](investigations/06-false-positive-triage.md), and [07](investigations/07-scheduled-task-persistence.md)
- [Capstone hypothesis](case-studies/correlated-attack-chain.md)
- [Investigation register](incident-timeline.md)
- [Screenshot guide](screenshots/README.md)
- [Lessons learned](lessons-learned.md)

Screenshots are genuine captures from the lab. They show preliminary searches, not full validation of every case. Remove credentials and unrelated personal information before publishing any additional evidence.
