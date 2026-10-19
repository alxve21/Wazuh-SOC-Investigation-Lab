# 🛡️ Wazuh SOC Investigation Lab

<p align="left">
  <img src="https://img.shields.io/badge/SIEM-Wazuh-005571?style=flat-square">
  <img src="https://img.shields.io/badge/Telemetry-Sysmon-5C2D91?style=flat-square">
  <img src="https://img.shields.io/badge/Endpoint-Windows-0078D6?style=flat-square">
  <img src="https://img.shields.io/badge/Framework-MITRE%20ATT%26CK-red?style=flat-square">
</p>

Hands-on SOC investigation lab focused on **Windows security telemetry, alert triage, event correlation, and incident-response analysis** using Wazuh and Sysmon.

> This is an authorized lab environment created for practical SOC training and portfolio demonstration.

---

## 🎯 What This Project Demonstrates

- Wazuh SIEM monitoring
- Windows Event Log analysis
- Sysmon process investigation
- Authentication analysis
- Alert triage and event correlation
- Account and privilege-change investigation
- File Integrity Monitoring
- Incident-response decision making
- MITRE ATT&CK mapping

---

## 🧪 Lab Environment

| Component | Role |
|---|---|
| **Wazuh** | SIEM / alert investigation |
| **Windows Endpoint** | Monitored host |
| **Sysmon** | Process and endpoint telemetry |
| **Kali Linux** | Controlled testing system |
| **VirtualBox** | Lab virtualization |

### Architecture

```mermaid
flowchart LR
    K[Kali Linux] --> W[Windows Endpoint]
    W --> S[Sysmon]
    W --> E[Windows Security Logs]
    S --> A[Wazuh Agent]
    E --> A
    A --> M[Wazuh Manager]
    M --> D[Wazuh Dashboard]

🔎 Investigations
Scenario	Evidence
Failed login analysis	Event ID 4625
Successful login correlation	Event ID 4624
Suspicious PowerShell execution	Sysmon Event ID 1
New local user creation	Event ID 4720
Administrator group modification	Event ID 4732
File modification	Wazuh FIM
Multi-event correlation	Combined telemetry


🚨 Example Investigation Chain
Failed Logins
      ↓
Successful Login
      ↓
PowerShell Execution
      ↓
New User Created
      ↓
User Added to Administrators
      ↓
File Modification

The important part of the investigation was not treating each event separately.

Events were correlated using:

Timestamp • User • Host • Source • Process • Command Line • Follow-on Activity

📄 [View Incident Timeline](./incident-timeline.md)
⚔️ MITRE ATT&CK Mapping
Technique	ID
Brute Force	T1110
PowerShell	T1059.001
Create Account	T1136.001
Account Manipulation	T1098
Valid Accounts	T1078


🧠 Analyst Approach
Validate Alert
      ↓
Check Context
      ↓
Correlate Events
      ↓
Determine Scope
      ↓
Assess Severity
      ↓
Preserve Evidence
      ↓
Contain / Escalate
      ↓
Document Findings

A major lesson from this lab was learning to avoid unsupported conclusions.

For example:
- A successful login does not automatically confirm compromise.
- PowerShell is not automatically malicious.
- Account creation requires context.
- Multiple related events provide stronger evidence than a single alert.
🛠️ Skills Demonstrated
Wazuh Sysmon Windows Event Logs PowerShell Analysis Alert Triage Event Correlation Incident Response MITRE ATT&CK File Integrity Monitoring
📂 Repository
Wazuh-SOC-Investigation-Lab/
├── README.md
├── incident-timeline.md
├── lessons-learned.md
└── screenshots/

📘 [Lessons Learned](./lessons-learned.md)
📸 Evidence
The screenshots folder will contain evidence from the actual lab, including:
- Wazuh agent activity
- Failed authentication events
- Sysmon PowerShell telemetry
- User creation
- Administrator group modification
- File Integrity Monitoring events
💡 Key Takeaway
SOC analysis is not about reacting to one alert — it is about correlating evidence and building a defensible investigation.

🔐 Authorized Lab Only
All activity in this repository was performed in a controlled environment for cybersecurity learning and defensive security practice.
