# Lessons Learned

These are analyst practices for the Wazuh lab. They are guidance, not claims that a specific alert or outcome has already been observed.

## Validate before concluding

- A single alert is a lead. Review the underlying event, host, user, time, collection source, and surrounding context before assigning intent.
- Distinguish raw event visibility from Wazuh alerting. An event can exist without a matching alert rule.
- Treat missing telemetry as a possible audit, collection, parsing, or retention gap. Do not present absence from Wazuh as proof that activity did not happen.

## Keep investigations evidence-based

- Record timestamps with timezone and preserve relevant event identifiers, agent/host, paths, hashes, process context, and rule details when present.
- Separate observed facts from hypotheses and identify what remains unknown.
- Correlate events only when evidence supports the relationship through time, host, account, source, process lineage, or another reliable identifier. Case numbering and scenario descriptions do not establish a shared incident.
- Use a defensible disposition: authorized, suspicious, benign with attribution, inconclusive, or visibility gap, with a short evidence-based rationale.

## Consider event-specific context

- Failed logons need context such as account, source, logon type, timing, and any verified successful authentication.
- PowerShell and other administrative tools are legitimate; inspect process lineage, command context, user, and related activity.
- Account/group changes and scheduled tasks require verification of the actor, scope, configuration, authorization, and audit coverage.
- FIM reports file changes; it does not identify intent by itself. Verify path, hashes, owner, process context, and approved changes.
- Network observations depend on configured event sources. Separate observed connections from alerting and from conclusions about intent.

## Preserve safe, useful evidence

- Keep lab exercises authorized, scoped, isolated, and reversible.
- Capture the overview and expanded event details needed to support the write-up. Redact secrets and unrelated personal data.
- Do not fill evidence fields or claim a result until the corresponding Wazuh data has been reviewed.
