# Practical UI . Agent Knowledge Base

## Core model

A strong interface is not merely attractive. Every meaningful detail should serve a reason connected to usability, accessibility, task completion, hierarchy, consistency, or business constraints.

### 1. Minimize usability risk
Prefer clear, familiar, legible patterns. If an element is ambiguous, hard to see, easy to misinterpret, or requires users to learn a novel convention, the design carries unnecessary risk.

### 2. Minimize total interaction cost
Count more than taps. Include visual searching, scrolling, reading, remembering, typing, precision movement, waiting, and decision-making. A design with fewer taps can still be worse if it adds thought or search cost.

### 3. Minimize cognitive load
Remove irrelevant information and unnecessary styling. Group related content. Maintain consistency. Use familiar patterns. Create an obvious hierarchy.

### 4. Use progressive disclosure
Show what is needed for the current decision. Keep secondary detail easy to reveal. Do not hide critical information.

### 5. Reduce choice
Decision time increases with the number and complexity of choices. Remove irrelevant options, group them, stage them, or recommend a smaller subset.

### 6. Build a design system
Constrain decisions with semantic tokens, reusable components, templates, and usage rules. Consistency improves speed for both users and design/development teams.

### 7. Accessibility is a usability requirement
Design for low vision, color vision differences, motor limitations, cognitive limitations, screen readers, screen magnifiers, bright environments, temporary impairment, and situational constraints.

### 8. Prefer common patterns
Build on existing mental models. Innovation should solve a real problem, not create a new way to perform a familiar interaction without measurable benefit.

## Less is more

- Remove nonessential information.
- Remove styles that do not communicate meaning.
- Do not equate minimalism with simplicity.
- Preserve visible or discoverable critical information.
- Design from constrained/small screens so prioritization happens early.
- Reduce decision complexity through fewer options and progressive steps.

## Color

- Maintain sufficient contrast for text and controls.
- Never communicate state by color alone.
- Use semantic system colors consistently for statuses such as success, warning, and error.
- Use color to support hierarchy, not decorate everything.
- Keep a small semantic palette with named roles.
- Apply the primary brand color purposefully, commonly to interactive emphasis.
- Use elevation, shadows, and tonal differences carefully to communicate depth.
- Define dark-mode colors independently rather than mechanically inverting light mode.
- Use state overlays or tonal variants consistently.

## Layout and spacing

- Group related items using proximity, containers, similarity, and alignment.
- Present information in order of importance.
- Use size, contrast, spacing, position, and depth as hierarchy controls.
- Use a small spacing scale rather than arbitrary values.
- Smaller spacing implies stronger relationship. Larger spacing separates groups.
- Use whitespace to reduce crowding and reveal structure.
- Maintain a clear grid and a limited number of alignments.
- Keep actions near the objects they affect.
- Design layouts to survive long content, localization, scaling, small screens, and empty states.

## Typography

- Keep the type system small and predictable.
- Use a type scale, not arbitrary sizes.
- Use generous line height for long text.
- Reduce line height as display text gets larger.
- Keep readable line lengths for prose.
- Prefer left alignment for long English text.
- Protect text contrast over imagery.
- Avoid extremely light text and harsh pure-black-on-white combinations when they reduce comfortable reading.

## UI copy

- Be concise.
- Prefer sentence case.
- Use plain language over jargon.
- Put the important information first.
- Structure long content from most important to supporting detail.
- Avoid unexplained abbreviations and acronyms.
- Use descriptive headings and scannable lists.
- Use vocabulary consistently.
- Use descriptive links and action labels.
- Error messages should explain what happened and how to recover.

## Buttons

- Maintain three action prominence levels: primary, secondary, tertiary.
- Use one primary action when one action clearly matters most.
- Use equal prominence for genuinely equal choices.
- Reduce prominence of destructive or low-priority actions.
- Avoid disabled buttons when users would not understand how to enable them. Validation on action can be clearer.
- Use action-oriented labels.
- Provide generous hit areas and spacing.
- Add deliberate friction for destructive actions.

## Forms

- Prefer a single downward flow with labels above controls.
- Remove nonessential fields.
- Mark optional and required status when ambiguity is possible.
- Prefer opt-in disclosure for nonessential fields.
- Size fields to reflect expected input when practical.
- Use conventional field affordances.
- Put critical helper text before the input so users can act on it before making a mistake.
- Keep persistent labels.
- Keep labels close to controls.
- For small visible sets, radio groups can outperform dropdowns.
- For long known-item lists, use search/autocomplete.
- For small numeric increments, use steppers.
- Use checkbox for binary choice committed with a form. Use toggle for immediate state change.
- Phrase binary labels positively.
- Break long forms into meaningful steps with progress, review, and confirmation.
- Group related fields under clear headings.
- Ensure control boundaries have sufficient contrast.
- Choose validation timing based on the task and cost of errors.
