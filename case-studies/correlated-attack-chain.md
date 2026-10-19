# Correlated Attack Chain — Capstone Case

**Status: Scenario outline; lab evidence pending.** This capstone describes how an analyst could assess a possible multi-stage sequence. It is not a report of observed compromise. Populate stages only when the corresponding Wazuh and endpoint evidence has been collected.

## Scope and evidence standard

Use only the isolated, authorized lab. The sequence below is a hypothesis to test across a bounded time window and identified endpoint(s). Correlate events using timestamps with timezone, host/agent, account, source, process identifiers, and event details. Similar event types or close timing alone do not prove a shared actor or causal chain. Keep unavailable stages marked **not observed / requires verification**.

## Hypothesis and validation

| Stage | Possible telemetry to examine | What would support the stage | Current status |
|---|---|---|---|
| Authentication attempts | Windows Security 4625; Wazuh event/rule | Failures from a consistent source across multiple accounts in a bounded interval | Pending verification |
| Successful access | Windows Security 4624 | A success on the same endpoint/account/source, with logon type and context reviewed | Pending verification |
| Suspicious execution | Sysmon 1 or Security 4688; process lineage and command line | An unexpected process chain and corroborating command or follow-on activity | Pending verification |
| Account or privilege change | Security 4720, 4728/4732 or applicable local group event | Actor, target, group scope, and resulting membership confirmed | Pending verification |
| Scheduled task or other persistence | Security 4698/4702; task XML and action | A task configuration and creator that are unexpected and attributable | Pending verification |
| Lateral movement | Authentication and endpoint telemetry on another host | A source-to-destination relationship with matching account/time and remote logon context | Pending verification |
| Possible data transfer | Available endpoint/network telemetry | A specific transfer event with destination, process, and data context | Pending verification |
| Log clearing | Security 1102 or relevant provider event | A verified clear event with host, actor, and surrounding context | Pending verification |

Event availability depends on Windows audit policy, Sysmon configuration, Wazuh collection/decoding, and retention. Event IDs above are search leads; verify the provider and rendered fields in the actual records. A missing event is a visibility gap, not evidence that the activity did not happen. Network transfer or exfiltration cannot be concluded from endpoint alerts alone without supporting telemetry.

## Analyst assessment and disposition

**Disposition: Not assessed — evidence pending.** No compromise, successful access, persistence, lateral movement, exfiltration, or log clearing is claimed by this scenario outline. After evidence collection, state separately which stages are confirmed, likely, suspicious, possible, not observed, or require verification. Explain the correlation basis and alternative benign explanations. If only isolated alerts exist, report them as separate observations rather than a confirmed chain.

## Evidence to add

Record the search window and timezone, endpoint/agent identities, source event IDs and Wazuh rule IDs where present, relevant account/process/path details, and links to original event exports or screenshots. Preserve original records and note any redactions. Do not enter sample or invented values.

## MITRE ATT&CK (conditional)

Map techniques only after behavior is verified. Candidate areas include Brute Force (T1110), Valid Accounts (T1078), PowerShell (T1059.001), Account Manipulation (T1098), Scheduled Task/Job (T1053.005), Remote Services (T1021), Exfiltration Over C2 Channel (T1041), and Clear Windows Event Logs (T1070.001). These are hypotheses for analyst reference, not findings or a claim that the techniques occurred.
