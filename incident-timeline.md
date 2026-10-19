# Investigation Register and Timeline

This file tracks evidence collection status for the independent Wazuh investigations. It is a case register, not a shared incident timeline. The cases below are not linked to one another unless separately verified evidence supports correlation.

**Current evidence status:** Pending. No Wazuh event timestamps, outcomes, or incident sequence have been entered yet.

| Case | Investigation | Time observed (with timezone) | Evidence status | Case record |
|---|---|---|---|---|
| 01 | Failed login analysis | Pending | Evidence pending | [Investigation 01](investigations/01-failed-login-analysis.md) |
| 02 | Suspicious PowerShell | Pending | Evidence pending | [Investigation 02](investigations/02-suspicious-powershell.md) |
| 03 | Privileged account change | Pending | Evidence pending | [Investigation 03](investigations/03-privileged-account-change.md) |
| 04 | File integrity monitoring | Pending | Evidence pending | [Investigation 04](investigations/04-file-integrity-monitoring.md) |
| 05 | Network visibility review | Pending | Evidence pending | [Investigation 05](investigations/05-network-recon-detection-gap.md) |
| 06 | False-positive triage | Pending | Evidence pending | [Investigation 06](investigations/06-false-positive-triage.md) |
| 07 | Scheduled task review | Pending | Evidence pending | [Investigation 07](investigations/07-scheduled-task-persistence.md) |

## Evidence entry guidance

After examining the actual Wazuh event, add its timestamp and timezone, host/agent, source event or rule, concise observed facts, and a link to the supporting screenshot. Keep separate cases separate. Do not infer a causal sequence from case numbering or from scenario descriptions. If no event is found, document the search window and relevant collection or retention limitation as a visibility gap.
