# Wazuh Investigation Screenshots

This folder contains four genuine dashboard overview captures from the reviewed Wazuh lab archive. Each is a search-results view; the captures do not by themselves verify the full scenario described by an investigation.

## Published overview captures

| File | What is visible | What it supports and what remains unverified |
|---|---|---|
| [01-failed-logon-search.png](01-failed-logon-search.png) | Search for `data.win.system.eventID:4625`; seven results are displayed, including rule ID 60122. | Confirms that failed-logon alerts appear in the selected search. The broad selected range does not establish a compact password-spray window, repeated source, or multiple distinct target accounts. |
| [03-group-change-search.png](03-group-change-search.png) | Search for `data.win.system.eventID:4732`; two results are displayed with group-change alert descriptions. | Shows candidate local-group-change alerts. The overview does not identify the actor and member fields, confirm resulting membership, or establish authorization. |
| [04-syscheck-search.png](04-syscheck-search.png) | Search for `rule.groups:syscheck`; four results are displayed, including file-change rule descriptions. | Shows Syscheck alert visibility. It does not show the dedicated `WazuhLab-FIM` marker path or verify the controlled exercise described in Investigation 04. |
| [05-network-event-search.png](05-network-event-search.png) | Search for `data.win.system.eventID:3`; 70 results are displayed in a broad selected range, with SMB admin-share-related alert descriptions visible. | Shows network-event search visibility. It does not document the bounded, single-host connection probe in Investigation 05 or establish its source, destination, or port. |

## Evidence limitations

These overviews are preliminary evidence only. Use the individual investigation pages for the exact status and limitations of each case. Do not interpret a query result as proof of the scenario, intent, or correlation with another case.

Other captures from the archive were not published where they showed local account, host, or IP details, or where their contents did not match the investigation they were named for. In particular, the process-search capture shows command-prompt alert descriptions, not Office-launched PowerShell; the detailed FIM capture does not establish an authorized software update. No benign or malicious disposition should be inferred from those images.

Before publishing further event-detail captures, verify the event fields needed by the investigation and remove local identifiers that are not needed for the portfolio.
