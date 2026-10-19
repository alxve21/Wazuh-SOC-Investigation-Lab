# 🛡️ Wazuh SOC Investigation Lab

Hands-on SOC investigation scenarios using Wazuh and Windows security telemetry. Each investigation is independent and should be supported by evidence from the actual lab before any findings are recorded.

> **Evidence status:** Case write-ups are investigation plans. Observed values and screenshots are pending. No event outcomes or case conclusions are asserted until verified in Wazuh.

## What this lab demonstrates

- Wazuh alert review and Windows event investigation
- Authentication, process, account, group, file-integrity, network-visibility, and scheduled-task triage
- Evidence-based reasoning, scope assessment, and careful disposition
- MITRE ATT&CK mapping where supported by observed behavior

## Lab environment

| Component | Role |
|---|---|
| Wazuh | SIEM and alert investigation |
| Windows endpoint | Monitored host |
| Sysmon | Process and endpoint telemetry, when configured |
| Kali Linux | Controlled testing system, when used in the authorized lab |
| VirtualBox | Lab virtualization |

## Investigations

These are separate cases. Do not correlate them into one attack chain unless real evidence independently supports that relationship.

| Case | Investigation | Primary focus |
|---|---|---|
| 01 | [Failed login analysis](investigations/01-failed-login-analysis.md) | Repeated authentication failures and context |
| 02 | [Suspicious PowerShell](investigations/02-suspicious-powershell.md) | Process lineage and command context |
| 03 | [Privileged account change](investigations/03-privileged-account-change.md) | Local group or privilege modification |
| 04 | [File integrity monitoring](investigations/04-file-integrity-monitoring.md) | Controlled monitored-file change |
| 05 | [Network reconnaissance visibility](investigations/05-network-recon-detection-gap.md) | Telemetry coverage and limitations |
| 06 | [False-positive triage](investigations/06-false-positive-triage.md) | Attribution of an authorized file update |
| 07 | [Scheduled task review](investigations/07-scheduled-task-persistence.md) | Task creation/change review |

## Investigation approach

Validate the alert, identify its source and collection limits, examine relevant context, preserve the observed evidence, and document an evidence-based disposition. A single event does not prove malicious intent. Missing telemetry is recorded as a visibility gap, not as proof that activity did not occur.

## Repository structure


```
Wazuh-SOC-Investigation-Lab/
├── README.md
├── incident-timeline.md
├── lessons-learned.md
├── investigations/
│   ├── 01-failed-login-analysis.md
│   ├── 02-suspicious-powershell.md
│   ├── 03-privileged-account-change.md
│   ├── 04-file-integrity-monitoring.md
│   ├── 05-network-recon-detection-gap.md
│   ├── 06-false-positive-triage.md
│   └── 07-scheduled-task-persistence.md
└── screenshots/
    └── README.md
```

## Evidence and screenshots

Add screenshots from the actual Wazuh lab under [screenshots/](screenshots/), following its README. Redact credentials, tokens, private addresses where appropriate, and unrelated personal data. Leave evidence fields pending until verified.

## Authorized lab use

Use only systems and accounts you are authorized to test. Keep any active exercise isolated, scoped, and reversible.
