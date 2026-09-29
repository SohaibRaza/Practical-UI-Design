# Agentic UI Workflows

## Workflow A . Single-agent audit and redesign

1. **Context pass**
   - identify user, job, constraints, platform, risk
   - list assumptions
2. **Task-model pass**
   - map current critical path
   - estimate interaction cost
3. **Audit pass**
   - retrieve relevant rule cards
   - produce evidence-based findings
4. **IA pass**
   - remove/defer/auto-fill/group/reorder information
5. **Interaction pass**
   - select controls and states
6. **Visual-system pass**
   - define hierarchy, type, spacing, color roles
7. **Accessibility pass**
   - contrast, targets, labels, focus, reading order
8. **Critic pass**
   - score rubric
   - resolve high-severity issues
9. **Handoff pass**
   - output screen spec, states, component rules, and rationale

## Workflow B . Multi-agent design team

### Agent 1 . Product / Context Analyst
Produces:
- user and job model
- business constraints
- critical actions
- error consequences
- assumptions

### Agent 2 . UX Auditor
Consumes context + existing UI.
Produces:
- ranked issues
- rule IDs
- evidence
- task-cost analysis

### Agent 3 . Information Architect
Produces:
- content priority
- groupings
- progressive-disclosure plan
- mandatory vs optional/deferred fields

### Agent 4 . Interaction Designer
Produces:
- step flow
- component selection
- state transitions
- validation and recovery behavior

### Agent 5 . Visual System Designer
Produces:
- typography roles
- spacing scale
- semantic color roles
- action hierarchy
- component variants

### Agent 6 . Accessibility Critic
Independently reviews:
- contrast
- color dependence
- target size
- focus and semantics
- screen-reader/magnifier risk
- error clarity

### Agent 7 . UI Copy Editor
Rewrites:
- labels
- CTA text
- helper text
- errors
- confirmations

### Agent 8 . Design QA / Judge
Uses `rubrics/ui-quality-rubric.yaml`.
Rejects output with unresolved critical/high issues.

## Workflow C . Planner -> Generator -> Critic loop

Use this for automated design generation:

1. Planner produces a design brief and rule subset.
2. Generator creates screen specification or image concept.
3. Critic evaluates against the exact rule subset and rubric.
4. Generator receives only actionable deltas, not generic taste comments.
5. Repeat until:
   - no critical/high defects remain;
   - score threshold is met;
   - no new regression is introduced.

Suggested threshold:
- prototype: 75/100
- production candidate: 85/100
- high-risk transaction or enterprise workflow: 90/100 plus explicit accessibility sign-off

## Workflow D . RAG retrieval strategy

Do not send the whole knowledge base for every task.

### Query construction
Build retrieval queries from:
- surface: mobile/web/desktop
- task: create/edit/search/checkout/onboard/configure
- components: forms/buttons/tables/navigation
- risk: destructive/payment/data-entry/accessibility
- known problems: clutter/scrolling/low contrast/too many choices

### Retrieval order
1. fundamentals
2. task-specific chapter
3. accessibility
4. layout/hierarchy
5. copy
6. visual style

Return 8-20 high-fit rules for most tasks. More is not automatically better.

## Workflow E . Screenshot -> structured spec

1. Inventory visible regions.
2. Infer hierarchy only from visible evidence.
3. Identify controls and likely states.
4. Flag ambiguous items as assumptions.
5. Audit with rule IDs.
6. Propose corrected IA.
7. Produce a screen spec before generating new visuals.
8. After visual generation, run the rubric again on the result.

## Workflow F . Design-system linting

An automated agent can scan a design or codebase for:
- more than one primary action in the same context
- arbitrary spacing values outside token scale
- inconsistent border radii
- placeholder-only fields
- missing labels
- target sizes below threshold
- low-contrast text/control borders
- color-only statuses
- inconsistent button labels
- unhandled loading/error/empty states

This turns the book into a design-lint layer rather than only a prompt reference.
