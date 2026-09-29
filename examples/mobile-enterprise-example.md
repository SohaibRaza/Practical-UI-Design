# Example . Dense Mobile Enterprise Form

## Scenario
A field worker creates a new customer record on a phone while moving between locations. The current screen shows 20+ fields in one long form.

## Agent reasoning

### Problems
- Too many fields compete for attention.
- Several values can be inferred from user, route, location, or organization context.
- Long dropdowns add scrolling and precision interactions.
- Optional commercial details slow the core creation task.
- The primary action is only visible at the bottom.

### Rule subset
- FUND-03 interaction cost
- FUND-04 cognitive load
- LESS-04 progressive disclosure
- LESS-08 reduce choice
- FORM-01 single-column flow
- FORM-02 minimize fields
- FORM-04 opt-in disclosure
- FORM-11 autocomplete for long lists
- FORM-16 multi-step long forms
- LAYOUT-12 related actions close
- BTN-02 single primary action

### Recommended flow
1. **Identity** . customer name, owner/contact, phone
2. **Location** . capture GPS, address assist, duplicate check
3. **Classification** . channel/type/segment using controlled selections
4. **Review & create** . compact summary, edit links, submit
5. **Optional enrichment after creation** . tax, credit, documents, extended notes

### Interaction choices
- Auto-fill sales rep, route, distributor, date, and GPS when reliable.
- Use searchable selectors for large master-data lists.
- Use visible radio/chip choices only for small known option sets.
- Keep a sticky primary CTA for the current step.
- Save progress locally if connectivity is unreliable.

### Expected benefit
The workflow reduces visible complexity and avoids forcing low-value data entry before the record exists. The design is not optimized merely for fewer screens. It is optimized for lower total effort and lower error risk.
