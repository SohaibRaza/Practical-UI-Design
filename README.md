# Practical UI Agent Skill Pack

A vendor-neutral, agent-friendly distillation of **Practical UI, 2nd Edition** by Adham Dannaway.

This pack converts the book's UI guidance into operational artifacts for AI design agents. It is a **derived summary and workflow layer**, not a reproduction of the book.

## What is included

- `SKILL.md` . portable agent skill for UI/UX audit, redesign, and design review
- `knowledge/practical-ui-kb.md` . compact context file for prompt injection
- `knowledge/rules.jsonl` . retrieval-friendly rule cards with stable IDs and source pages
- `knowledge/decision-tables.md` . deterministic component and interaction selection rules
- `knowledge/anti-patterns.md` . common failure patterns and corrections
- `workflows/agentic-ui-workflows.md` . planner/critic/executor workflows for multi-agent systems
- `workflows/screenshot-audit.md` . screenshot-to-audit procedure
- `rubrics/ui-quality-rubric.yaml` . 100-point evaluator rubric
- `schemas/ui-audit.schema.json` . structured output contract for UI audits
- `prompts/task-templates.md` . reusable prompts for audit, redesign, forms, and review
- `examples/mobile-enterprise-example.md` . example of applying the skill to a dense field-work mobile form

## Recommended use

### 1. As a skill
Point an agent at `SKILL.md` and let it retrieve `knowledge/rules.jsonl` by rule ID, tag, or chapter.

### 2. As RAG knowledge
Chunk `rules.jsonl` line-by-line. Each record is intentionally self-contained and has stable metadata.

### 3. As an evaluator
Use `rubrics/ui-quality-rubric.yaml` with a separate critic agent after a design agent produces a proposal.

### 4. As a structured UI-audit service
Require the agent to return JSON matching `schemas/ui-audit.schema.json`.

## Design philosophy encoded by this pack

The skill treats UI design as a sequence of explainable decisions. It prioritizes task completion, usability risk, interaction cost, cognitive load, accessibility, consistency, and clear hierarchy before decorative novelty.

Rules are treated as strong defaults, not immutable laws. Context, platform conventions, user research, technical constraints, and usability testing can override a default when the agent can explain why.

## Copyright note

This pack contains original summaries, operational rules, schemas, and workflows derived from a user-provided copy of the book. It intentionally avoids reproducing the book's full text or visual examples.
# Practical-UI-Design
