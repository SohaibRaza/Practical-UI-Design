# Decision Tables for UI Agents

These tables operationalize the book's guidance into deterministic defaults. They are defaults, not laws.

## Selection control

| Situation | Default control | Why | Override when |
|---|---|---|---|
| 2 states, change takes effect after submit | Checkbox | Compact, familiar, low interaction cost | The domain convention strongly uses radios |
| 2 states, change takes effect immediately | Toggle | Communicates immediate on/off state | Immediate effect would be risky or surprising |
| 2 to ~10 mutually exclusive options | Radio group | Options stay visible and comparable | Space is severely constrained |
| Long list, user knows the item | Autocomplete / searchable selector | Avoids long scrolling | Users primarily browse rather than search |
| Long unfamiliar taxonomy | Hierarchical selector or staged fields | Reduces overwhelming list length | Search terminology is reliably known |
| Small numeric changes | Stepper plus editable number | Fast repeated increments | Large numeric ranges or arbitrary values |
| Date/time | Platform-native or familiar picker | Existing mental model | Domain requires a custom scheduling visualization |

## Form structure

| Condition | Default |
|---|---|
| Short form | Single column, labels above inputs |
| Long form | Break into a small number of logical steps |
| Short related fields | May sit side-by-side inside the single-column flow |
| Optional information | Prefer opt-in progressive disclosure |
| Required/optional mix | Mark both states clearly |
| Complex instructions | Put concise helper text before the field |
| Reviewable high-impact data | Add review step before final commit |

## Validation timing

| Input type / risk | Default validation |
|---|---|
| Ordinary form with low implementation budget | Validate on submit, summarize errors, link to fields |
| Format-sensitive field such as email | Validate after leaving the field |
| Password rules, username availability, live constraints | Debounced live validation after user pauses |
| Grouped controls | Validate group after interaction or submit |
| Expensive destructive action | Validate prerequisites before confirmation |

## Action hierarchy

| Action type | Weight |
|---|---|
| Single most important next action | Primary |
| Alternative / equal-importance action | Secondary |
| Low priority utility | Tertiary |
| Destructive | Usually tertiary/destructive treatment plus explicit friction |

## Progressive disclosure

Reveal a field or section only when at least one is true:
1. it is required for the current decision;
2. it prevents a likely error before the user acts;
3. the user explicitly opts into that branch;
4. the field becomes relevant because of a previous answer.

Defer it when:
- it is informational but not needed now;
- it is rarely used;
- it can be inferred or auto-populated;
- it belongs to advanced configuration;
- it can be completed after the primary task is successfully created.

## UI agent rule of thumb for optimization

Do not optimize only for screen count or tap count. Estimate:

`total interaction cost = taps + typing + scrolling + visual search + decisions + memory + precision + waiting + recovery`

A multi-step flow can be better than a single screen if it lowers total cost and error probability.
