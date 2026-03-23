# Metrics

> **Toolkit connection:** These metrics measure whether the *content system works* (leading indicators). For metrics that measure whether content *achieves coherence* for users (lagging indicators), see the [Coherence Metrics Canvas](../distributed-coherence-toolkit/05-coherence-metrics-canvas.md). Use both: when these metrics are green but the Canvas metrics are red, you have an efficient system producing incoherent content. See the [unified metrics map](#unified-metrics-map) below.

## Efficiency

- Cycle time per content item
- Authoring time saved
- Reuse rate

## Quality

- Structural pass rate
- LCR rework rate
- Accessibility pass rate

## Risk

- Compliance incidents
- Rollback frequency
- High-risk content without human review

## Impact

- Reduction in related support tickets
- Task success
- Abandonment in key flows

## Unified Metrics Map

These operational metrics are **leading indicators** of the coherence outcomes measured by the DCT's Coherence Metrics Canvas. Here's how they connect:

| This Playbook (Leading) | Predicts → | DCT Canvas (Lagging) |
|--------------------------|-----------|---------------------|
| **Cycle time per content item** | Fast, well-governed content → | **Time to content** (Operational Coherence) |
| **Structural pass rate** | Pattern-compliant content → | **Cross-channel recognition** (Brand Coherence) |
| **LCR rework rate** | Low rework = stable patterns → | **Coherence drift** (Operational Coherence) |
| **Accessibility pass rate** | Accessible content everywhere → | **Information parity** (Functional Coherence) |
| **Compliance incidents** | Low incidents = trustworthy content → | **Trust transfer** (Brand Coherence) |
| **Reduction in support tickets** | Clear content at point of need → | **Task completion by channel** (Functional Coherence) |
| **Task success** | Users can act on content → | **Cross-channel journey completion** (Functional Coherence) |

### Reading the Dashboard Together

| If Playbook Metrics Are... | And DCT Metrics Are... | Then... |
|---------------------------|----------------------|---------|
| Green | Green | System is working AND content is coherent. Keep going. |
| Green | Red | Efficient system producing incoherent content. Rules are being followed but they aren't creating felt unity. Revisit coherence markers. |
| Red | Green | Content is coherent despite system failures. Unsustainable — fix the system before coherence degrades. |
| Red | Red | Both need work. Start with playbook metrics (fix the system), then measure coherence outcomes. |

---

[← Back to README](README.md) | [← Previous: Operating Model](operating-model.md) | [Next: Examples →](examples.md)
