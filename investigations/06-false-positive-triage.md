# Investigation 06 — Benign Change False-Positive Triage

**Status:** Evidence pending. This is an independent triage exercise; do not mark an event benign until it is attributable to an authorized change.

## Scenario

A Wazuh FIM alert reports that an application file changed during a suspected routine software update. The analyst checks whether the file, signer, update window, and change record support a benign explanation.

## Safe lab boundary

Use an existing authorized update event or a disposable lab application and approved updater. Do not install untrusted software or alter production files. If no update event is available, document the investigation as not yet performed.

## Detection and investigation

- Review the actual FIM alert: agent, full path, event type, timestamp, and available before/after hashes.
- Verify the application owner, expected installation path, digital signature, file version, and hash using trusted system or vendor records.
- Compare the event time with an approved update/change window and available installer or update logs.
- Check for conflicting context such as an unexpected parent process, unusual location, unsigned replacement, or changes outside the approved window.
- Record the evidence supporting attribution. A familiar filename or timing alone is not sufficient to close the alert as benign.

## Assessment criteria

Disposition may be benign only when the file change is attributable to the expected authorized updater and matches the approved version/change record. Otherwise keep it suspicious or inconclusive and escalate according to the lab process. This case is separate from Investigation 04's unauthorized-change scenario.

## Observed evidence to add

| Field | Observed value |
|---|---|
| Alert time and timezone | Pending |
| Windows agent/hostname | Pending |
| File path and change type | Pending |
| Before/after hashes and version | Pending |
| Signer and verification result | Pending |
| Updater/process and update log | Pending |
| Approved change reference/window | Pending |
| Wazuh rule ID/level | Pending |
| Analyst disposition and rationale | Pending |

## Screenshots

Add the Wazuh FIM alert and relevant verification view under ../screenshots/ using ../screenshots/README.md. Redact secrets and unrelated data.
