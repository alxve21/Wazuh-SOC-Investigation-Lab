# Wazuh Investigation Register

This register summarizes evidence status for four independent Wazuh investigations. It is not a shared incident timeline. The cases are not linked to one another unless separately verified evidence supports correlation. Case IDs retain their original lab numbering.

**Current evidence status:** Four published dashboard overviews show searches for failed logons, group-change alerts, Syscheck alerts, and network events. They are preliminary search views and do not complete the scenario-specific validation. No shared incident sequence is established.

| Case | Investigation | Evidence status | Case record |
|---|---|---|---|
| 01 | Failed login analysis | Seven 4625 results visible in a broad selected range; password-spray pattern not verified | [Investigation 01](investigations/01-failed-login-analysis.md) |
| 03 | Privileged account change | Two 4732 search results visible; actor, member, resulting membership, and authorization unverified | [Investigation 03](investigations/03-privileged-account-change.md) |
| 04 | File integrity monitoring | Four Syscheck results visible; dedicated marker path and controlled exercise unverified | [Investigation 04](investigations/04-file-integrity-monitoring.md) |
| 05 | Network visibility review | Seventy Event ID 3 results visible; documented single-host probe unverified | [Investigation 05](investigations/05-network-recon-detection-gap.md) |

## Evidence entry guidance

When event-level evidence is reviewed, record its timestamp and timezone, host/agent, source event or rule, concise observed facts, and a link to relevant evidence. Keep separate cases separate. Do not infer a causal sequence from case numbering or scenario descriptions. If no event is found, document the search window and relevant collection or retention limitation as a visibility gap.
