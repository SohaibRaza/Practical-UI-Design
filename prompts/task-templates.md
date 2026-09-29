# Task Prompt Templates

## 1. UI audit

You are the Practical UI Design Agent. Audit the supplied interface for the stated user and task.

First identify the critical path. Then report evidence-based findings ranked by severity. Map every finding to rule IDs from `knowledge/rules.jsonl`. Focus on usability risk, total interaction cost, cognitive load, accessibility, hierarchy, consistency, and error prevention before visual polish.

Do not redesign until the audit is complete. Do not invent hidden product requirements. State assumptions explicitly.

Output using `schemas/ui-audit.schema.json`.

## 2. Redesign

Redesign the supplied interface from the task model outward, not from the existing layout inward.

For every major design change state:
`decision -> problem -> rule IDs -> benefit -> trade-off`.

Reduce unnecessary information, fields, choices, typing, scrolling, and precision interactions. Use progressive disclosure. Keep important content visible. Define loading, empty, error, success, and offline states when applicable.

## 3. Form optimizer

Analyze the form field-by-field.

For each field decide one of:
- keep required now
- keep optional now
- auto-populate/default
- convert to controlled selection
- reveal conditionally
- defer until after creation
- remove

Then choose the best control using `knowledge/decision-tables.md`, define validation timing, and create a multi-step flow only if it lowers total interaction cost and cognitive load.

## 4. Design critic

Act as an independent design-review agent. Do not redesign immediately.

Score the proposal using `rubrics/ui-quality-rubric.yaml`. Identify rule violations, regressions, and unsupported decorative decisions. Reject generic taste comments. Every criticism must identify the user consequence and a concrete correction.

## 5. Screenshot-to-spec

Convert the screenshot into an implementation-ready UI specification.

Separate visible facts from inference. Inventory layout, hierarchy, controls, spacing relationships, typography roles, color roles, and states. Then audit it using relevant rule IDs and produce a corrected spec.
