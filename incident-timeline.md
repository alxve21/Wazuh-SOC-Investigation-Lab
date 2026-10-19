# Investigation Register and Timeline

This file tracks evidence collection status for the independent Wazuh investigations. It is a case register, not a shared incident timeline. The cases below are not linked to one another unless separately verified evidence supports correlation.

**Current evidence status:** Four published dashboard overviews show searches for failed logons, group-change alerts, Syscheck alerts, and network events. They are preliminary search views and do not complete the scenario-specific validation. No shared incident sequence is established.

| Case | Investigation | Time observed (with timezone) | Evidence status | Case record |
|---|---|---|---|---|
| 01 | Failed login analysis | Broad selected search range; compact test window not established | Seven 4625 results visible; password-spray pattern not verified | [Investigation 01](investigations/01-failed-login-analysis.md) |
| 02 | Suspicious PowerShell | Not established | No Office-to-PowerShell lineage verified; available process search shows command-prompt alert descriptions | [Investigation 02](investigations/02-suspicious-powershell.md) |
| 03 | Privileged account change | Not established from overview | Two 4732 search results visible; actor, member, resulting membership, and authorization unverified | [Investigation 03](investigations/03-privileged-account-change.md) |
| 04 | File integrity monitoring | Not established from overview | Four Syscheck results visible; dedicated marker path and controlled exercise unverified | [Investigation 04](investigations/04-file-integrity-monitoring.md) |
| 05 | Network visibility review | Broad selected range; bounded exercise window not established | Seventy Event ID 3 results visible; documented single-host probe unverified | [Investigation 05](investigations/05-network-recon-detection-gap.md) |
| 06 | False-positive triage | Not established | Authorized updater attribution is missing; benign disposition unsupported | [Investigation 06](investigations/06-false-positive-triage.md) |
| 07 | Scheduled task review | Search interval and timezone not available | No matching task event was reported in the reviewed search; audit and collection coverage unknown | [Investigation 07](investigations/07-scheduled-task-persistence.md) |

## Evidence entry guidance

After examining the actual Wazuh event, add its timestamp and timezone, host/agent, source event or rule, concise observed facts, and a link to relevant evidence. Keep separate cases separate. Do not infer a causal sequence from case numbering or from scenario descriptions. If no event is found, document the search window and relevant collection or retention limitation as a visibility gap.
