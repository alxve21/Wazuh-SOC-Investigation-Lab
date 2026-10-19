# Investigation 02 — Office-Launched PowerShell

**Status:** No case-matching event has been verified in the reviewed captures. The available process-search result shows command-prompt alert descriptions; it does not show Office-launched PowerShell or the parent-child details required by this scenario.

## Scenario

A Windows endpoint reports a document application launching PowerShell. The alert raises a phishing-style execution hypothesis because Office-to-script-engine process relationships can be abused, but the parent-child relationship alone does not prove that a document was malicious or that code caused harm. This case does not depend on the authentication, account-change, FIM, network, or task cases.

## Lab boundary and safe setup

Use only the isolated Windows lab VM. If generating telemetry, use a harmless marker command and a controlled test document or launcher. Do not use a real malicious document, download payloads, disable protections, or execute untrusted macros. If the Office parent relationship cannot be reproduced safely, record that as a detection gap rather than inventing an event.

## Detection and investigation

- Primary telemetry: **Sysmon Event ID 1** (process creation). Windows Security **4688** may provide a second source if process auditing is enabled.
- Wazuh search starting point: `data.win.system.eventID:1`; refine by the observed process image or parent image.
- Record event time, endpoint, user, process image, parent image, command line, parent command line, process identifiers, and rule ID/level when present. Field names can vary with the installed Sysmon decoder; use the fields shown in the actual alert.
- Inspect the parent and child process lineage, executable path and signature, document source, and any related file or network events in the same time window. Script Block Logging events are useful only if that logging is already configured.
- Redact sensitive document names or user details before adding any public evidence.

## Assessment criteria

Raise concern when the observed process chain is unexpected and the command line or surrounding evidence shows suspicious behavior, such as hidden or encoded execution, an untrusted document source, or follow-on activity. An Office process spawning PowerShell is a lead for investigation, not a verdict by itself. Record a benign, suspicious, or inconclusive disposition only after reviewing the available evidence.

## Evidence status

No Office-to-PowerShell process chain is verified in the reviewed material. The available process-search result displays command-prompt-related alert labels, not the parent image, PowerShell command line, and event details needed for this case. Keep the scenario unconfirmed until a matching event and lineage are reviewed.

## Observed evidence to add

| Field | Observed value |
|---|---|
| Exercise time and timezone | Pending |
| Windows agent/hostname and user | Pending |
| Parent process image | Pending |
| PowerShell image and command line | Pending |
| Sysmon/4688 event and Wazuh rule | Pending |
| Related file or network event | Pending |
| Analyst disposition and rationale | Pending |
