---
name: bot-worklog
description: Maintain Markdown worklogs for successive bot generations, including predecessor reading, daily entries, and explicit continuity links.
---

# Bot Worklog

Keep one Markdown file per bot generation under a user-selected worklog root, using `<member>/<member>_YYYYMMDD.md`. The date is the generation's start date in the agreed timezone. Append later daily entries to that file; do not create a new generation file every day.

## Starting a generation

1. Read the durable handover and its referenced previous worklog before starting work. Follow continuity links or referenced artifacts when needed to understand unfinished work. If the predecessor record is missing, record the gap rather than fabricating history.
2. Create a new file using [the worklog template](../../templates/worklog-template.md), if available, or the format below. Never overwrite a predecessor's file.
3. If a same-day rotation collides with the required filename, select a separate generation-specific worklog root and retain `<member>/<member>_YYYYMMDD.md` beneath it. Record the actual root and full continuity references in the handover; do not silently reuse the earlier file.
4. Record the logical member, generation reference, start date, timezone, handover reference, and previous worklog path. Update the handover's current worklog reference.

## Record format

Use this structure, repeating the dated entry section as work progresses:

```markdown
# Worklog: <member>

- Generation reference: <generation-reference>
- Started: <YYYY-MM-DD>
- Timezone: <timezone>
- Handover document: <document-reference>
- Previous worklog: <previous-worklog-path-or-none>
- Next worklog: <next-worklog-path-or-pending>

## <YYYY-MM-DD> <HH:MM> <timezone>

### Completed
- Action, result, and evidence or artifact reference.

### Decisions
- Decision, reason, and relevant user authorization reference.

### Open items and blockers
- Item, status, dependency or awaited role, and next step.

### Next actions
- Concrete next action and success criteria.

### Durable updates
- Handover sections updated and why, or none.
```

Append entries after meaningful work and before handoff. Preserve earlier entries; correct mistakes with an explicit dated correction. Record failures and partial completion accurately. Store stable rules and operational knowledge in the handover and link to them from the worklog. Never include secret values.

At rotation, add a final entry with completed work, remaining items, and the successor reference when known. Link the next worklog after it exists, preserving a navigable chain between generations.
