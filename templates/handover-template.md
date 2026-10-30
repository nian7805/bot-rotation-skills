# Handover: <member>

- Last verified: <YYYY-MM-DD>
- Timezone: <timezone>
- Maintainer role: <role>

## Role Card

| Field | Value |
| --- | --- |
| Name | <logical-member-name> |
| Responsibilities | <responsibilities> |
| Reports to | <role> |
| In scope | <scope> |
| Out of scope | <exclusions> |

## Routine Schedule

| Task | Time and recurrence | Timezone | Trigger | Inputs | Outputs | Success criteria | Scheduler reference | State |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| <task> | <time-and-recurrence> | <timezone> | <trigger> | <input-references> | <output-references> | <observable-success> | <reference> | <enabled-or-paused> |

## Resource Map

| Type | Reference | Purpose | Access requirements | Secret storage reference only |
| --- | --- | --- | --- | --- |
| <file-folder-program-connector-or-account> | <resource-reference> | <purpose> | <access-method> | <environment-variable-name-or-secure-store-reference-or-none> |

Never include secret values, passwords, tokens, or recovery codes.

## Rules Register

| Effective date | User rule | Scope | Reason | Status | Supersedes |
| --- | --- | --- | --- | --- | --- |
| <YYYY-MM-DD> | <rule> | <scope> | <reason-or-unknown> | <active-or-superseded> | <earlier-rule-reference-or-none> |

Newer user rules replace older conflicting user rules in the same scope, subject to higher-priority instructions. Preserve superseded entries.

## Authority Boundaries

| Action | Autonomous scope | User approval required when | Existing authorization reference |
| --- | --- | --- | --- |
| Routine internal work | <scope> | <condition> | <reference-or-none> |
| External messages | <authorized-scope-or-none> | <condition> | <reference-or-none> |
| Deletion | <authorized-scope-or-none> | <condition> | <reference-or-none> |
| Payments | <authorized-scope-or-none> | <condition> | <reference-or-none> |
| Production writes | <authorized-scope-or-none> | <condition> | <reference-or-none> |

## Ongoing Items

| Item | Status | Waiting on | Next step | Success criteria |
| --- | --- | --- | --- | --- |
| <item> | <status> | <role-or-dependency-or-none> | <next-action> | <success> |

## Lessons Learned

| Pitfall or symptom | Verified solution | Evidence | Remaining limitation |
| --- | --- | --- | --- |
| <pitfall> | <solution> | <reference> | <limitation-or-none> |

## Collaboration

| Related role | Upstream or downstream | Handoff artifact | Delivery expectation | Contact method |
| --- | --- | --- | --- | --- |
| <role> | <direction> | <artifact-reference> | <expectation> | <configured-channel-reference> |

## Record Continuity

- Previous worklog path: <previous-worklog-path-or-none>
- Current worklog path: <current-worklog-path>
- Member mapping reference: <mapping-reference>
- Saved avatar image reference: <image-reference-or-none>

## Rotation Configuration

- Interval: <user-confirmed-interval>
- Timezone: <timezone>
- Covered members: <logical-member-references>
- Next execution: <timestamp-or-pending>
- Rotation schedule reference and state: <reference-and-state>
- Rotation state: <idle-or-in-progress-with-owner-and-start-time>

Keep stable knowledge here. Keep daily progress, actions, results, and blockers in the worklog.
