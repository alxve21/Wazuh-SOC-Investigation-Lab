# Incident Timeline

This timeline summarizes the sequence of security events investigated in the Wazuh SOC lab.

## Timeline

### 1. Failed Authentication Attempts
Multiple failed login attempts were observed on the Windows endpoint.

**Relevant Event**
- Event ID: 4625
- Purpose: Failed logon detection

The activity was reviewed to determine whether the failures represented normal user behavior or suspicious authentication attempts.

### 2. Successful Authentication
A successful login event was reviewed after the failed authentication activity.

**Relevant Event**
- Event ID: 4624
- Purpose: Successful logon detection

The login was correlated with the previous failed attempts using timestamps, username, host context, source information, and logon type.

### 3. Suspicious PowerShell Execution
PowerShell activity was detected through Sysmon process telemetry.

**Relevant Event**
- Sysmon Event ID: 1
- Process: powershell.exe

The investigation reviewed:
- User
- Image
- ParentImage
- CommandLine
- ParentCommandLine
- Execution time

PowerShell itself is legitimate, so the process was evaluated based on its execution context and related activity rather than being treated as malicious automatically.

### 4. New Local User Creation
A new local user account was created on the endpoint.

**Relevant Event**
- Event ID: 4720
- Purpose: User account creation

The account creation was correlated with the surrounding authentication and process activity.

### 5. Administrator Group Modification
A user was added to a privileged local group.

**Relevant Event**
- Event ID: 4732
- Purpose: Member added to a local security group

This activity increased the severity of the investigation because it represented a privilege-related account modification.

### 6. File Integrity Monitoring Activity
File Integrity Monitoring detected file changes within the monitored directory.

The investigation reviewed:
- File path
- Change type
- Timestamp
- Related user/host context

## Correlated Investigation

The events were not treated independently.

The investigation followed the sequence:

```text
Failed authentication activity
        ↓
Successful authentication
        ↓
PowerShell execution
        ↓
New user creation
        ↓
Administrator group modification
        ↓
File modification activity
