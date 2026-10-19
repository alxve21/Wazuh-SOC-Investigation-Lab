# Investigation 04 — Sensitive File Integrity Change

**Status:** Evidence pending. This page is a standalone FIM scenario. Add observed paths, hashes, and disposition only after reviewing the actual Wazuh event.

## Scenario

A monitored lab configuration file is modified outside its expected maintenance window. The investigation determines what changed, when it changed, and whether the activity was authorized. This uses a disposable lab fixture, not the Windows hosts file, production configuration, or files from another case.

## Lab boundary and safe setup

Configure Wazuh FIM to monitor a dedicated test directory named WazuhLab-FIM. Change only a harmless marker file in that directory. Do not alter operating-system, security, or business-critical files. Preserve the before/after contents and revert the marker after capturing evidence.

## Detection and investigation

- Primary telemetry: Wazuh File Integrity Monitoring (syscheck) alert for a file added, modified, or deleted.
- Search the Wazuh alert data for syscheck events and narrow to the observed file path and exercise time; field names can vary by Wazuh version.
- Record the agent, full path, event type, timestamp, user/process context if available, and before/after hashes shown in the event.
- Compare the change with the controlled test action and any approved maintenance record. FIM identifies a file change; it does not identify intent by itself.

## Assessment criteria

Treat an unexplained change to a sensitive monitored file as suspicious until the owner and expected content are verified. A controlled marker-file modification should be documented as a successful FIM validation only if the expected event and path appear in Wazuh. If the event is absent, record a collection or configuration gap rather than claiming detection.

## Observed evidence to add

| Field | Observed value |
|---|---|
| Exercise time and timezone | Pending |
| Windows agent/hostname | Pending |
| Monitored file path | Pending |
| FIM event type | Pending |
| Before/after hash values | Pending |
| Related user/process, if available | Pending |
| Wazuh rule ID/level | Pending |
| Analyst disposition | Pending |

## Screenshots

Add an overview and one expanded syscheck event under ../screenshots/ using the case filenames in ../screenshots/README.md. Exclude unrelated files and secrets.
