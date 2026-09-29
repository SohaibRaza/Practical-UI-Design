# UI Anti-Patterns for Agent Review

| Anti-pattern | Why it fails | Preferred correction | Related rule families |
|---|---|---|---|
| Icon-only critical actions | Meaning can be ambiguous | Add concise labels or proven familiar icons with accessible names | fundamentals, accessibility, copy |
| Multiple primary buttons | Competing hierarchy | Choose one primary or reduce equal actions to secondary | buttons, hierarchy |
| Disabled CTA with no explanation | User can become stuck | Keep actionable and validate, or explain exact requirement nearby | buttons, forms |
| Placeholder-only input | Label disappears and can be low contrast | Persistent label above field | forms, accessibility |
| Long dropdown | High search and scroll cost | Autocomplete, radio group, or staged selector | forms, interaction-cost |
| Optional fields shown by default | Adds clutter and apparent work | Ask for opt-in, then reveal required field | forms, progressive-disclosure |
| Dense multi-column form | Increases scanning and missed fields | Single downward flow | forms, cognitive-load |
| Helper text hidden in tooltip | Critical guidance can be missed | Make critical guidance visible before input | forms, discoverability |
| Error shown only in red | Excludes color-blind users | Add text/icon and semantic structure | accessibility, colour |
| Low-contrast borders | Controls become hard to discover | Increase non-text contrast | accessibility, forms |
| Decorative color everywhere | Weakens hierarchy | Reserve strong color for semantic and interactive emphasis | colour, hierarchy |
| Arbitrary spacing values | Produces inconsistent grouping | Use a constrained spacing scale | layout, design-system |
| Equal spacing between everything | Destroys relationship cues | Use tighter spacing within groups and larger gaps between groups | layout |
| Center-aligned long body text | Slows scanning | Left-align long prose in left-to-right languages | typography |
| Very light body text | Legibility risk | Increase contrast and use robust weight | typography, accessibility |
| All information visible at once | Overloads decision-making | Progressive disclosure and grouping | less-is-more |
| Critical information hidden to look minimal | Aesthetic minimalism harms task | Restore visible or obvious discoverability | less-is-more |
| Novel control for familiar task | Forces new mental model | Prefer platform/common pattern | fundamentals |
| Destructive action beside primary CTA with equal prominence | Accidental activation and competing hierarchy | Lower prominence and add confirmation/friction | buttons |
| Vague CTA such as “Continue” when consequence matters | User cannot predict action | Use specific verb + object where practical | copy, buttons |
| Error message without recovery instruction | User knows failure but not resolution | State problem and next step | copy, forms |
