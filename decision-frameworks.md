# Decision Frameworks for Regulated Flows

When teams don't agree on how to balance short vs. thorough, decisions stall and quality slips. This section shows how decision frameworks turn fuzzy debates into clear choices across five components: what decision needs to be made, the anatomy you'll use to structure it, the principles that break ties, how AI will apply the rules, and how we'll measure maturity.

<aside>

**Scenario:** A checkout or transfer error appears mid-flow. Do we keep it short so people finish, or add context so they don't panic? Use the framework to decide in under a minute.

</aside>

```yaml
decision_framework:
  conciseness_vs_completeness:
    defaults:
      mid_task_flow: always_concise
      decision_point: default_complete
      error_state: balanced
      onboarding: progressive_disclosure
    risk_overrides:
      high_financial_risk: completeness
      medium_admin_change: balanced
      low_nav: concision
    parameters:
      concise_max_words: 15
      complete_max_words: 75
      progressive_disclosure: true
validation_order:
  - accuracy
  - accessibility
  - clarity
  - efficiency
  - brand
```

## The Tension

Every content designer faces this daily: Should we keep it short so users can move quickly, or provide full information so they can make informed decisions?

## Decision Framework

### Step 1: Assess User Context

**Where is the user in their journey?**

| Context | Default to | Why |
| --- | --- | --- |
| Mid-task flow | Conciseness | Interruptions are costly |
| Decision point | Completeness | Information reduces anxiety |
| Error state | Balanced | Need clarity AND next steps |
| Onboarding | Progressive disclosure | Start simple, reveal complexity |

### Step 2: Evaluate Risk Level

**What happens if the user makes the wrong choice?**

```
HIGH RISK (Financial, Legal, Privacy)
↓
COMPLETENESS WINS
• Include all necessary information
• Use progressive disclosure if needed
• Provide expandable details

MEDIUM RISK (Account settings, Preferences)
↓
BALANCED APPROACH
• Core information inline
• Details on demand
• Clear learn more paths

LOW RISK (Navigation, UI interactions)
↓
CONCISENESS WINS
• Minimum viable message
• Action-focused
• Trust user knowledge
```

### Step 3: Apply the Formula

**Concise Version Structure:**

```
[What] + [Action]
"Payment failed. Try again"
```

**Complete Version Structure:**

```
[What] + [Why] + [Impact] + [Action] + [Help]
"Payment failed because your card was declined. Your order hasn't been placed. Please update your payment method or try a different card. Contact support if this continues."
```

### Step 4: Test Against Principles

✓ **Clarity Check:** Can users understand what happened/what to do?

✓ **Cognitive Load:** Are we adding necessary or unnecessary complexity?

✓ **User Capability:** Does the user have the knowledge to fill gaps?

✓ **Recovery Path:** Can users fix problems with the information provided?

## Real-World Application

### Scenario: Subscription Cancellation

**Pattern Library Approach:**

"Here's our cancellation message: 'Your subscription has been cancelled. You'll have access until [date].'"

**Systematic Approach:**
1. Assess: User at major decision point → Lean toward completeness
2. Risk: Medium-High (losing access to service) → Include key information
3. Apply: Use complete structure with progressive disclosure
4. Result:

```
Immediate confirmation (Concise):
"Subscription cancelled successfully"

Full context (Complete):
"What happens next:
• Access continues until [date]
• Downloads remain available
• You can resubscribe anytime
• We'll email a confirmation"
```

## AI Implementation

This framework translates directly to AI prompts and business rules for training:

```python
content_rules = {
    "decision_framework": {
        "conciseness_vs_completeness": {
            "high_risk_context": "always_complete",
            "mid_task_flow": "always_concise",
            "decision_point": "default_complete",
            "parameters": {
                "concise_max_words": 15,
                "complete_max_words": 75,
                "progressive_disclosure": true
            }
        }
    }
}
```

## Measurement

Track which approach performs better:
- Concise: Task completion time, flow abandonment
- Complete: Support tickets, error recovery rate
- Balanced: User satisfaction, task success rate

---

*This framework scales because it provides thinking tools, not just examples. Teams can apply it to novel situations without needing new patterns.*

---

[← Back to README](README.md) | [Next: Pattern Anatomy →](pattern-anatomy.md)
