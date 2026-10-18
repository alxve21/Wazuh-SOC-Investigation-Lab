# Lessons Learned

This lab helped reinforce several important SOC investigation principles.

## 1. A Single Alert Does Not Confirm an Attack

One alert can be suspicious, but context is required before deciding whether activity is malicious.

Authentication events, process activity, user behavior, and host context should be reviewed together.

## 2. Correlation Is More Valuable Than Isolated Events

Multiple events become more meaningful when they are connected through:

- Timestamp
- Username
- Host
- Source IP
- Process relationships
- Follow-on activity

For example, failed logins followed by a successful login, suspicious PowerShell execution, and account changes create a much stronger investigation story than any single event alone.

## 3. PowerShell Is Not Automatically Malicious

PowerShell is a legitimate administrative tool.

It becomes suspicious depending on:

- Parent process
- Command line
- Encoded commands
- Network connections
- Child processes
- Related account or file activity

## 4. Parent-Child Process Relationships Matter

Process relationships provide important context.

For example:

```text
winword.exe
    ↓
powershell.exe
