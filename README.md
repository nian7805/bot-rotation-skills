# Bot Rotation Skills

## Purpose

A portable set of skills for handing over AI bot responsibilities between generations. Durable knowledge lives in a handover document; daily progress lives in a generation worklog. Rotation preserves task ownership, schedules, and continuity while leaving old bot deletion to the user.

## Contents

- `skills/bot-handover-doc/SKILL.md`: Durable operational knowledge and maintenance rules.
- `skills/bot-worklog/SKILL.md`: Markdown worklogs and predecessor continuity.
- `skills/bot-rotation/SKILL.md`: Initial scheduling, recurring rotation, and immediate rotation.
- `templates/handover-template.md`: Reusable handover document.
- `templates/worklog-template.md`: Reusable generation worklog.

## Install

Place the three skill folders in the skill discovery directory supported by your agent host. If the host supports a shared skill search root, register this package's `skills` directory directly. Keep `templates` beside `skills` to preserve the relative template links. When installing the skill folders separately, copy the templates to a shared accessible location and update the template links in the installed copies. Each skill also describes its essential fields or format for independent use.

Enable the host capabilities needed for bot creation, scheduling, avatar updates, and member mapping maintenance. These skills provide instructions, not a bot management service or scheduler. Unsupported operations are reported as manual steps.

## Usage

1. Invoke `bot-handover-doc` to create a handover for each logical member. Choose operational storage locations and fill in the template with relevant resources and authority boundaries. Store only references to secrets.
2. Invoke `bot-worklog` when a generation starts. Read the previous worklog before creating `<member>/<member>_YYYYMMDD.md` beneath the selected worklog root. Append daily entries to that generation's file. For same-day filename collisions, use a distinct generation-specific root without overwriting the predecessor.
3. Invoke `bot-rotation` to configure rotation. On first setup, the skill asks for cadence, timezone, first execution time, and covered members, proposes weekly by default, and creates the confirmed schedule when supported.
4. Request `Rotate <member> now` for an immediate rotation. The skill reads the handover and latest worklog, creates and briefs the successor, starts its worklog, uses a saved image for its avatar when possible, transfers schedules, updates the member mapping, and reports the outcome.
5. Review the reported old bot list and manually delete bots that are ready for removal. Old schedules must be verified paused before corresponding successor schedules run.

User authorization remains bounded across generations. External messages, deletion, payments, and production writes require approval unless already authorized within the recorded scope. Runtime member mappings may contain actual bot identifiers; this reusable package contains only generic placeholders.

## License

MIT. See [LICENSE](LICENSE).
