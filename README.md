# Wazuh SOC Investigation Lab

## Objective

The objective of this project was to build a small SOC investigation lab using Wazuh, a Windows endpoint, and Sysmon telemetry.

The goal was not only to generate security events, but to investigate them from an analyst perspective, correlate related activity, identify suspicious patterns, and document incident-response decisions.

## Lab Environment

- Wazuh
- Windows Endpoint
- Wazuh Agent
- Sysmon
- Kali Linux
- VirtualBox

## Scenarios Investigated

- Failed login attempts
- Successful login correlation
- Suspicious PowerShell execution
- Local user creation
- Administrator group modification
- File Integrity Monitoring
- Basic reconnaissance observation
- Multi-event correlation

## Investigation Approach

The investigation focused on correlating authentication, process execution, account modification, and file integrity events rather than treating each alert independently.

Key investigation areas included:

- User and host context
- Event timestamps
- Authentication activity
- PowerShell command execution
- Parent/child process relationships
- Account creation
- Privilege changes
- File modification events
- Incident severity and escalation decisions

## Incident Response Workflow

The following workflow was used during investigations:

1. Verify the alert
2. Correlate related activity
3. Determine the affected user and host
4. Assess severity
5. Preserve relevant evidence
6. Recommend containment
7. Escalate when necessary
8. Document findings

## Key Windows Events

- Event ID 4625 — Failed logon
- Event ID 4624 — Successful logon
- Event ID 4720 — New user account created
- Event ID 4732 — User added to a local group
- Sysmon Event ID 1 — Process creation

## Example Attack Chain

A simulated incident was correlated across multiple security events:

```text
Failed login attempts
→ Successful login
→ Suspicious PowerShell execution
→ New local user created
→ User added to Administrators
→ File modification activity
