# Principle Hierarchy (with LCR alignment)

## So what's this about?

Flat voice-and-tone lists break the moment principles collide. This section adds a clear hierarchy so teams know what wins when, and no one has to guess.

<aside>

**Scenario:** Payment error feels too warm and too short. Use the hierarchy to make Accuracy and Clarity win so users recover fast.

</aside>

## Conflict Resolution Diagram

```
CONFLICT DETECTED
↓
Is Level 1 principle involved?
├─ YES → Level 1 wins
└─ NO → Continue
   ↓
   Are both Level 2?
   ├─ YES → Check context rules
   └─ NO → Higher level wins
      ↓
      Both Level 3?
      └─ Apply context matrix
```

## Context Matrix

| Context | Clarity | Brevity | Warmth | Formality |
| --- | --- | --- | --- | --- |
| Error states | **WIN** | Yield | Yield | Yield |
| Legal content | **WIN** | Yield | Lose | **WIN** |
| Onboarding | **WIN** | Balance | **WIN** | Lose |
| Power user tools | Balance | **WIN** | Lose | Lose |
| Marketing copy | Balance | Balance | **WIN** | Balance |

## Principle Levels

### Level 1 (non-negotiable):

- **Accuracy** → wins over everything
- **Accessibility** → wins over brevity/aesthetics

### Level 2 (strategic):

- **Clarity** → in high-stakes money contexts, prioritize over brevity
- **Efficiency** → support task completion quickly when safe

### Level 3 (brand):

- **Warmth** → permitted when it never obscures risk, facts, or next steps

## Conflict Resolver

1. Any Level 1 involved? **Level 1 wins**
2. Level 2 vs Level 2? **Apply context rules**: money at risk → Clarity; blocked task → Efficiency
3. Level 3 yields to Levels 1–2

## YAML Schema

```yaml
content_principles:
  level_1_mandatory:
    accuracy:
      priority: 1
      overrides: [all]
    accessibility:
      priority: 2
      overrides: [style, brevity]
  level_2_strategic:
    clarity:
      priority: 3
      context_modifiers:
        high_complexity: prioritize_over_brevity
        financial_stakes: prioritize_over_brevity
    efficiency:
      priority: 4
      context_modifiers:
        expert_user: prioritize
        blocked_task: prioritize
  level_3_brand:
    warmth:
      priority: 5
      yields_to: [accuracy, accessibility, clarity, efficiency]
conflict_resolution:
  order:
    - level_1_wins
    - compare_level_2_by_context
    - level_3_yields
  context_matrix:
    error_state: [clarity_win, brevity_yield, warmth_yield]
    legal_content: [clarity_win, warmth_lose, formality_win]
    onboarding: [clarity_win, warmth_win]
```

---

[← Back to README](README.md) | [← Previous: Pattern Anatomy](pattern-anatomy.md) | [Next: AI-Ready Rules →](ai-ready-rules.md)
