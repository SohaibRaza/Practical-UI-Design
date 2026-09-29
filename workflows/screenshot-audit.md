# Screenshot Audit Procedure

## Input
A screenshot or set of screens, plus any known user/task context.

## Phase 1 . Observe, do not redesign yet
Record:
- screen purpose
- primary action
- secondary actions
- visible information groups
- form fields
- navigation
- statuses
- alerts/errors
- density and scroll implication
- likely device/platform

Do not infer hidden data as fact.

## Phase 2 . Task-risk analysis
Ask:
- Can the user tell what to do next?
- What can be misread or missed?
- Which actions require precision or memory?
- What is being typed that could be selected, inferred, scanned, or auto-filled?
- Is important information hidden?
- Are rare options competing with frequent ones?
- What happens in loading, error, empty, offline, or partial states?

## Phase 3 . Rule-mapped findings
Each finding must include:

`finding_id | severity | screenshot evidence | rule_ids | consequence | recommendation`

Avoid generic comments such as “make it cleaner” unless you can explain what is removed, why, and what task benefit results.

## Phase 4 . Redesign specification
Define:
- information order
- progressive disclosure
- primary action
- control types
- validation timing
- error recovery
- accessibility constraints
- responsive/mobile behavior

## Phase 5 . Verification
Compare before and after on:
- visible choices
- required typing
- scroll distance
- number of fields
- interaction cost
- error opportunities
- readability
- target size
- task clarity

Quantify when possible, but do not invent precise time savings without measurement.
