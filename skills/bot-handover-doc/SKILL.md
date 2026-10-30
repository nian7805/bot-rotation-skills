---
name: bot-handover-doc
description: Create and maintain durable bot handover documents covering responsibilities, recurring work, resources, rules, authority, and continuity.
---

# Bot Handover Document

Use one durable handover document per logical member. Keep stable operational knowledge here and daily progress in worklogs. Start from [the handover template](../../templates/handover-template.md) when available; the required fields below also make this skill usable independently.

## Required fields

- **Role card:** Member name, responsibilities, reporting relationship, scope, and explicit exclusions.
- **Routine schedule:** For every recurring task, record time, timezone, recurrence, trigger, inputs, outputs, and success criteria. Include its scheduler reference and current state when available.
- **Resource map:** Files, folders, programs, connectors, and account references, with purpose and access requirements. Record only secret storage references, such as an environment variable name; never record secret values, passwords, tokens, or recovery codes.
- **Rules register:** User rules with effective date and reason. A newer user rule supersedes an older conflicting user rule within the same scope, subject to higher-priority instructions. Preserve superseded rules as history and identify the active replacement. Do not invent a missing reason; mark it unknown.
- **Authority boundaries:** Separate autonomous actions from actions requiring user approval. Explicitly cover external messages, deletion, payments, and production writes. Record the scope and conditions of any existing authorization; rotation never expands authority.
- **Ongoing items:** Open work, status, dependencies or who is awaited, and the next concrete step.
- **Lessons learned:** Pitfalls, symptoms, verified solutions, and remaining limitations.
- **Collaboration:** Upstream and downstream roles, exchanged artifacts, delivery expectations, and contact methods. Refer to roles or configured channels rather than embedding personal contact details.
- **Record continuity:** Previous worklog path, current worklog path, and last verified date. At rotation, the outgoing bot's final worklog becomes the incoming bot's previous worklog.

## Maintenance during normal work

Read the handover document when assuming a role. Update it when responsibilities, routines, resources, user rules, authority, durable lessons, or collaboration arrangements change. Refresh ongoing items and record continuity before rotation. Record daily actions, results, blockers, and decisions in the current generation's worklog using `bot-worklog`.

Keep entries factual and concise. Mark unknown, unavailable, or unverified information explicitly. Link to authoritative resources instead of copying volatile details. Never copy credentials into either document. Review the handover against the latest worklog before passing it on; do not replace useful history with an unsupported summary.
