# Investigation 05 — Network Reconnaissance Visibility Review

**Status:** Evidence pending. This is a standalone, controlled visibility review; do not infer a detection from expected behavior.

## Scenario

An analyst reviews whether a low-volume connection probe against one authorized lab host is visible in the telemetry collected by Wazuh. The goal is to validate logging coverage and distinguish a genuine observation from a visibility gap.

## Safe lab boundary

Only perform a small, approved test against one host in an isolated lab network, within an agreed time window. Do not scan public addresses, production systems, or a subnet. If no approved test is available, use existing authorized lab telemetry and document that no exercise was run.

## Detection and investigation

- Identify the available endpoint or firewall telemetry before the exercise. Depending on configuration, relevant sources may include Sysmon network connection events, Windows Filtering Platform events, or firewall logs.
- Wazuh may not generate an alert from a connection probe unless the relevant event source is collected and a matching rule or query exists.
- Search within the actual exercise window and target host. Record the source, destination, port, event provider, event ID, agent, timestamp, and matching Wazuh rule/query if present.
- If the event is missing, check collection configuration and retention. Absence from Wazuh is a visibility gap, not proof that no connection occurred.

## Assessment criteria

State whether the expected telemetry was present, absent, or inconclusive. Separate raw event visibility from alerting: an event in Wazuh does not by itself establish malicious intent, and no alert does not establish that traffic was absent.

## Observed evidence to add

| Field | Observed value |
|---|---|
| Exercise time and timezone | Pending |
| Authorized target host | Pending |
| Source host | Pending |
| Event provider/ID and telemetry source | Pending |
| Destination and port(s) observed | Pending |
| Wazuh agent and rule/query | Pending |
| Visibility result and limitations | Pending |
| Analyst disposition | Pending |

## Screenshots

Add the relevant Wazuh overview and event (if available) under ../screenshots/ using the case filenames in ../screenshots/README.md. Remove secrets and unrelated data.
