# Investigation 01 — Controlled Password Spray

**Status:** Evidence pending. This page documents the lab scenario and investigation method. Add the observed event details and Wazuh screenshots after running the exercise; no timestamps, IPs, alert IDs, or outcomes are assumed here.

## Scenario

A single test source makes one failed SMB authentication attempt against several existing, disposable lab accounts on the Windows endpoint. The pattern of interest is one password tested across multiple users, rather than many passwords tested against one user. This case is independent of every other investigation in this repository.

## Lab boundary and safe setup

Run only on the isolated, host-only lab network. Use accounts created solely for this exercise and one deliberately incorrect lab password, at a low rate. Do not target personal, production, or third-party accounts. Stop if an account locks or traffic reaches an unexpected host. Do not create a successful login as part of this case; a later success would be a separate follow-up observation to document only if it actually occurs.

## Detection and investigation

- Primary Windows Security event: **4625** — failed logon.
- Wazuh search starting point: `data.win.system.eventID:4625`.
- Review the time range around the controlled exercise. Raw events may be present even when no custom password-spray correlation rule is configured; do not claim that an alert fired unless the dashboard shows it.
- Record the timestamp, endpoint/agent, target account, source IP, logon type, workstation name, failure status/substatus, and Wazuh rule ID/level when available.
- Group events by source IP and short time window. Count distinct targeted accounts and compare the pattern with the known test actions.
- Check for a matching **4624** successful logon from the same source and time range. A failed attempt alone does not establish compromise.

## Assessment criteria

Treat the pattern as a suspected password spray only when the observed events show the same source making failures against multiple accounts in a compact time window and the pattern is not explained by the documented test or approved activity. Escalate the assessment if evidence shows a successful logon, lockout, or additional suspicious behavior. Otherwise, document the result as an attempted authentication pattern and state the detection limits.

## Observed evidence to add

| Field | Observed value |
|---|---|
| Exercise time range and timezone | Pending |
| Windows agent/hostname | Pending |
| Source IP | Pending |
| Distinct targeted accounts | Pending |
| Logon type and failure status | Pending |
| Wazuh rule ID/level, if any | Pending |
| Related 4624 success found? | Pending |
| Analyst disposition | Pending |

## Screenshots

Add the overview and one expanded event under `../screenshots/` using the names listed in `../screenshots/README.md`. Keep usernames and IPs consistent with the lab, and do not include credentials in screenshots.
