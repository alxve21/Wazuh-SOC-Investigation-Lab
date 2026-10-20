# Wazuh Investigation Register

These are seven separate investigations, not a shared incident timeline. The four published dashboard captures show preliminary searches; they do not verify each scenario or connect the cases.

| Case | What the reviewed material shows | Assessment | Record |
|---|---|---|---|
| 01 | Seven Windows 4625 results in a broad selected range. | The source/account pattern needed to identify a password spray is not established. | [Failed login analysis](investigations/01-failed-login-analysis.md) |
| 02 | The available process-search capture shows command-prompt alert descriptions. | Office-launched PowerShell and process lineage are not shown. | [Office-launched PowerShell](investigations/02-suspicious-powershell.md) |
| 03 | Two Windows 4732 results appear in the overview. | Actor, member, resulting membership, and authorization are unverified. | [Privileged group change](investigations/03-privileged-account-change.md) |
| 04 | Four Syscheck results appear in the overview. | The monitored path and dedicated marker-file exercise are not verified. | [File integrity monitoring](investigations/04-file-integrity-monitoring.md) |
| 05 | Seventy Event ID 3 results appear; SMB admin-share descriptions are visible. | The documented single-host probe and its source/destination details are not verified. | [Network visibility review](investigations/05-network-recon-detection-gap.md) |
| 06 | Reviewed Syscheck details lack the updater and change information needed for attribution. | Inconclusive; the change cannot be called benign from the available detail. | [False-positive triage](investigations/06-false-positive-triage.md) |
| 07 | No matching 4698/4702 result was found in the reviewed search. | The search window and audit/collection coverage are unknown. | [Scheduled-task review](investigations/07-scheduled-task-persistence.md) |

## Updating this register

For each case, record the event time and timezone, host or agent, source event or rule, the relevant observed fields, and a link to the supporting record. Keep separate investigations separate. If a search returns no event, include the search window and collection limits; do not treat that result as proof the activity did not occur.
