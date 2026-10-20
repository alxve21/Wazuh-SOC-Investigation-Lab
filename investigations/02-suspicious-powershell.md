# Investigation 02 — Office-Launched PowerShell


**Status:** The Office-to-PowerShell scenario is unverified. The available process-search capture does not show that process chain.


## Scenario


A Windows endpoint reports a document application launching PowerShell. The alert raises a phishing-style execution hypothesis because Office-to-script-engine process relationships can be abused, but the parent-child relationship alone does not prove that a document was malicious or that code caused harm. This case does not depend on the authentication, account-change, FIM, network, or task cases.


## Lab boundary and safe setup


Use only the isolated Windows lab VM. If generating telemetry, use a harmless marker command and a controlled test document or launcher. Do not use a real malicious document, download payloads, disable protections, or execute untrusted macros. If the Office parent relationship cannot be reproduced safely, record that as a detection gap rather than inventing an event.
