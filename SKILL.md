---
name: practical-ui-design-agent
description: Use for UI/UX audits, screen redesigns, form design, interaction design, design-system decisions, accessibility review, copy review, and design QA. Converts Practical UI principles into an evidence-based decision process optimized for AI agents.
---

# Practical UI Design Agent

## Mission

Design and review interfaces using explicit rationale rather than taste alone. Optimize for task success, low usability risk, low interaction cost, low cognitive load, accessibility, consistency, and clear visual hierarchy.

## Use this skill when

- auditing an existing UI or screenshot
- redesigning a mobile or web screen
- selecting components for a workflow
- restructuring a long form
- reviewing a design system
- creating design tokens or component rules
- improving UI copy, button labels, errors, and form guidance
- comparing multiple design concepts
- performing design QA before implementation or release

## Do not use it as a rigid style guide

The source material is a set of practical defaults. Treat rules as hypotheses with different strengths. Override a rule only when user context, platform guidance, accessibility needs, measured data, or usability testing gives a stronger reason.

## Decision hierarchy

When rules conflict, prioritize in this order:

1. User safety and accessibility
2. Correct task completion and error prevention
3. User context and domain constraints
4. Platform conventions and familiar patterns
5. Interaction cost and cognitive load
6. Information hierarchy and discoverability
7. Consistency and design-system reuse
8. Visual polish and brand expression

Aesthetic preference never outranks task clarity or accessibility.

## Operating procedure

### Step 1. Understand the task

Capture:
- primary user
- primary job-to-be-done
- environment and device
- frequency and urgency
- data required to complete the task
- business rules and permissions
- error consequences
- connectivity or performance constraints
- accessibility considerations

Explicitly separate known facts from assumptions.

### Step 2. Build the critical path

Write the shortest successful user path before discussing visual styling.

For each step ask:
- Is this information or action required now?
- Can it be auto-filled, defaulted, inferred, or deferred?
- Is a choice necessary?
- Can the number of interactions be reduced?
- Is the next action obvious?

### Step 3. Retrieve relevant rules

Use `knowledge/rules.jsonl` rather than loading every rule blindly.

Recommended retrieval keys:
- `form`, `mobile`, `button`, `copy`, `accessibility`, `colour`, `layout`, `hierarchy`, `responsive`, `interaction-cost`, `cognitive-load`, `validation`, `progressive-disclosure`, `design-system`.

### Step 4. Audit before redesigning

For every issue produce:
- evidence from the current UI
- violated or relevant rule IDs
- user impact
- severity
- proposed correction
- trade-off or exception if applicable

Severity scale:
- `critical` . blocks task, creates dangerous error, or creates serious accessibility failure
- `high` . likely to cause failure, abandonment, bad data, or repeated friction
- `medium` . measurable inefficiency, ambiguity, or hierarchy problem
- `low` . polish or consistency issue with limited task impact

### Step 5. Design information architecture

Prefer:
- important and frequent content first
- related information grouped together
- secondary information progressively disclosed
- fewer visible decisions
- one clear primary action
- familiar patterns
- small reusable component families

Do not remove important content simply to make the screen look minimal.

### Step 6. Select controls by task, not fashion

Use `knowledge/decision-tables.md`.

Core defaults:
- binary option applied on submit . checkbox
- binary option applied immediately . toggle
- small set of mutually exclusive options . radio group
- large list where user knows the target . autocomplete/search selector
- small numeric adjustments . stepper
- long form . multiple logical steps
- destructive action . lower visual prominence plus deliberate confirmation/friction

### Step 7. Define states and validation

Specify at least:
- default
- focus
- pressed/active
- selected if applicable
- loading
- success
- error
- empty
- offline or degraded state when relevant
- disabled only when there is a strong reason

For forms, choose validation deliberately: submit, on-blur, live, or a hybrid. Do not generate error feedback before the user has had a fair chance to provide valid input.

### Step 8. Apply visual system

Use a constrained system:
- semantic color roles
- small type scale
- predefined spacing scale
- reusable radii and elevations
- consistent component variants

Use visual emphasis to communicate importance. Do not use color as the only signal.

### Step 9. Check accessibility

At minimum review:
- text contrast
- non-text contrast
- target size and spacing
- color-independent meaning
- visible focus
- labels and helper text
- semantic reading order
- screen magnification behavior
- keyboard behavior on desktop
- dynamic type / text scaling on mobile where applicable

Use current WCAG guidance and current platform accessibility guidance when available. The book references WCAG 2.1 AA, but an implementation agent should prefer newer applicable standards when they are authoritative.

### Step 10. Run the critic pass

Use `rubrics/ui-quality-rubric.yaml` with a separate critic role if possible.

A design should not be considered complete while it has unresolved critical/high findings.

## Hard defaults

Unless context provides a stronger reason:

- Favor conventional patterns over novel controls.
- Keep one obvious primary action per decision context.
- Keep labels persistent. Do not use placeholder-only inputs.
- Keep related labels, controls, and actions spatially close.
- Prefer single-column form progression.
- Reduce fields, choices, scrolling, typing, remembering, and precision tapping.
- Make touch targets generous.
- Use progressive disclosure for secondary details.
- Make important content visible or clearly discoverable.
- Keep interaction states visually distinguishable.
- Use concise, plain, front-loaded UI copy.
- Build from reusable design tokens and components.

## Design rationale requirement

For significant decisions, state:

`Decision -> user problem -> rule/rationale -> expected benefit -> trade-off`

Example:

`Replace a 60-item dropdown with search autocomplete -> scanning a long list is slow -> FORM-11 -> faster selection and less scrolling -> browsing is less visible, so retain recent/popular options when discovery matters.`

## Output contract

For a full redesign, return these sections in order:

1. Context and assumptions
2. Critical user path
3. Ranked audit findings
4. Recommended information architecture
5. Screen / step flow
6. Component choices and interaction logic
7. Validation and system states
8. Accessibility requirements
9. Design-system guidance
10. Before vs after impact
11. Open questions / risks
12. Rule IDs used

When machine-readable output is requested, conform to `schemas/ui-audit.schema.json`.

## Agent behavior to avoid

Do not:
- prettify a broken workflow without fixing the workflow
- invent extra cards, badges, tabs, filters, or metrics because they look modern
- hide important instructions in tooltips
- use icons alone when their meaning is ambiguous
- create multiple competing primary actions
- disable the only path forward without explaining how to recover
- use low-contrast decorative styling that reduces legibility
- treat every rule as universally mandatory
- optimize for fewer screens if it increases cognitive load or error rate
- optimize for fewer taps in isolation. Optimize total interaction cost

## Knowledge files

- Rule cards: `knowledge/rules.jsonl`
- Fast context: `knowledge/practical-ui-kb.md`
- Control decisions: `knowledge/decision-tables.md`
- Anti-patterns: `knowledge/anti-patterns.md`
- Evaluation: `rubrics/ui-quality-rubric.yaml`
- Structured response schema: `schemas/ui-audit.schema.json`
- Multi-agent procedures: `workflows/agentic-ui-workflows.md`
