# Investigation 07 — Scheduled Task Creation Review

**Status:** No matching scheduled-task event was found in the Wazuh search you reviewed. The search window and audit, collection, and retention coverage have not been verified, so this remains an inconclusive visibility gap.

## Scenario

A new or modified Windows scheduled task is reviewed to determine whether its creator, principal, trigger, and action match an authorized administrative change. The review focuses on persistence-relevant task configuration without assuming malicious intent.

## Safe lab boundary

Use an existing authorized event or create only a temporary, harmless task in a disposable lab VM with approval. A test task may launch Notepad under the current user; do not create a task that runs scripts, downloads content, changes security settings, or executes with elevated privileges. Remove only the temporary test task after preserving the relevant event and task details.

## Detection and investigation

- Review Windows Security events 4698 (task created) and 4702 (task updated), if auditing is enabled and those events are collected by Wazuh.
- Record the task name/path, creating account, principal/run level, trigger, action/command, creation or update time, event provider/ID, agent, and Wazuh rule.
- Where available, inspect the task XML and correlate with the authorized change record and the creator's role.
- Treat encoded commands, unexpected paths, unusual accounts, or unexplained triggers as indicators requiring investigation; validate the actual recorded action before concluding.
- If events are absent, document audit/collection coverage and avoid claiming the task was detected.

## Assessment criteria

Close as authorized only when the task configuration and creator match an approved change. Otherwise document suspicious or inconclusive elements and follow the lab escalation process. This case is independent of the other investigations.

## Evidence status

The reviewed search found no matching 4698/4702 event. Its interval and timezone are unavailable, and audit, collection, and retention coverage have not been verified. The result therefore indicates an inconclusive visibility gap; it does not establish that no task was created.
