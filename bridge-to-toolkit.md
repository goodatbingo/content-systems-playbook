# Bridge: Content Systems Playbook ↔ Distributed Coherence Toolkit

## What This Is

This playbook is a **domain-specific implementation** of the [Distributed Coherence Toolkit](../distributed-coherence-toolkit/00-README.md) (DCT), scoped to regulated financial services, post-login experiences, and AI-enabled content operations.

Think of it this way: the DCT is the music theory — scales, chord progressions, the physics of harmony. This playbook is the chart for tonight's set — specific songs, specific arrangements, specific cues for the horn section. You need both.

This bridge document maps every concept between the two, so teams can move fluidly between the universal framework and the finserv implementation.

---

## Concept Map

| This Playbook | Distributed Coherence Toolkit | Relationship |
|---------------|-------------------------------|-------------|
| **Principle Hierarchy** (3 levels: Accuracy, Accessibility / Clarity, Efficiency / Warmth) | **Coherence Markers** (5 dimensions: User Agency, Complexity, Trust, Balance, Attention) | **Different levels of the same system.** Coherence markers define the *relationship with users* (strategic). The principle hierarchy defines *content quality rules* (tactical). Markers inform principles — not the other way around. |
| **Decision Frameworks** (Conciseness vs. Completeness) | **Decision Framework Cards** (7 trade-off cards) | **This playbook deep-dives one card.** The DCT's Card 2 (Comprehensive vs. Minimal) is the closest match. The finserv framework adds risk overrides, YAML schemas, and regulatory context. For the other six trade-offs (Personalize vs. Standardize, Match vs. Adapt, Proactive vs. Reactive, Urgent vs. Patient, Explain vs. Direct, Brand vs. Clarity), use the DCT cards directly. |
| **Pattern Anatomy** (Error messages only) | **Adaptive Content Patterns** (6 patterns: Feature Intro, Error, Onboarding, Help, Confirmation, Empty State) | **This playbook elaborates one of six patterns.** The error message anatomy here is a regulated-finserv adaptation of DCT Pattern 2. See [variation rationale](#error-pattern-variation-rationale) below for documented departures. For the other five patterns, use the DCT templates and adapt using this playbook's compliance hooks. |
| **AI-Ready Rules** (YAML schemas, prompt templates, quality gates) | Not present in DCT | **This playbook extends the toolkit.** The DCT provides the governance philosophy; this playbook provides the machine-actionable implementation. AI rules here encode DCT principles (especially Content Principle Cards 07) into YAML that AI systems can consume. |
| **Metrics** (Efficiency, Quality, Risk, Impact) | **Coherence Metrics Canvas** (Brand, Functional, Value, Operational) | **Leading vs. lagging indicators.** Playbook metrics measure whether the *content system works* (operational efficiency). DCT metrics measure whether content *achieves coherence* (user outcomes). Use both: when playbook metrics are green but DCT metrics are red, you have an efficient system producing incoherent content. |
| **Operating Model** (RACI, workflows) | **Content Source Types Matrix** (4 types with governance models) | **Complementary governance layers.** The DCT classifies content by type (Core, Reference, Operational, Conversational); this playbook defines roles and workflows. Combining them: classify content with DCT source types, then apply this playbook's workflows within each type. |
| **Maturity Roadmap** (90-day plan) | **Getting Started** paths (Quick and Thorough) | **Sequential.** Complete the DCT's Coherence Markers Worksheet first (to establish foundations), then execute this playbook's 90-day rollout. |
| Not present | **Variation Rationale Log** | **Use directly.** When this playbook's rules are adapted for new contexts, log the variation using the DCT template. |
| Not present | **Theoretical Foundations (Campbell)** | **Read this.** The cognitive science behind every decision in this playbook. Understanding the cohesion → continuity → coherence chain transforms these rules from compliance requirements into design thinking. |

---

## Arbitration: When Frameworks Overlap

When both document sets offer guidance on the same decision, here's the precedence:

### For strategic content decisions (what relationship are we building with users?)
→ Use **DCT Coherence Markers** (Resource 01)

### For content quality decisions (is this specific piece good enough?)
→ Use **Playbook Principle Hierarchy** (principle-hierarchy.md)

### For content trade-offs in finserv regulated flows
→ Use **Playbook Decision Frameworks** (decision-frameworks.md)

### For content trade-offs in non-finserv or cross-domain contexts
→ Use **DCT Decision Framework Cards** (Resource 03)

### For measuring content system health
→ Use **Playbook Metrics** (leading indicators: is the system working?)
→ Use **DCT Coherence Metrics Canvas** (lagging indicators: is the content coherent?)

---

## Error Pattern Variation Rationale

This playbook's error message anatomy departs from DCT Pattern 2 in three documented ways:

### Departure 1: Impact moved from Required to Conditional

| | DCT Pattern 2 | This Playbook |
|--|---------------|---------------|
| **Impact element** | Required | Conditional (include when consequences aren't obvious) |

**Rationale:** In regulated financial services, the impact of an error (e.g., "your payment wasn't processed") is almost always obvious from context — the user knows what they were trying to do. Making Impact conditional reduces message length in the 80% case where stating the impact would be redundant, while preserving it for cases like delayed processing or data loss where consequences are genuinely unclear.

**Coherence markers preserved:** Trust (still transparent), Attention (respects finite attention), Complexity (reduces unnecessary information).

### Departure 2: Severity Indicator added

| | DCT Pattern 2 | This Playbook |
|--|---------------|---------------|
| **Severity Indicator** | Not present | Present (Critical / Warning / Info) |

**Rationale:** Regulatory compliance in financial services requires triaging content by risk level. The Severity Indicator maps directly to the DCT's adaptation-by-severity table (Minor → Moderate → Severe → Critical) but makes it an explicit structural element rather than adaptation guidance — because AI systems and compliance linters need a machine-readable severity signal.

**Coherence markers preserved:** Trust (explicit about severity), User Agency (user can calibrate response to severity).

### Departure 3: YAML schemas added throughout

| | DCT Pattern 2 | This Playbook |
|--|---------------|---------------|
| **Machine-readable rules** | Not present | YAML schemas for every element |

**Rationale:** The DCT is designed for human teams making decisions. This playbook extends that to AI-assisted content operations where rules need to be both human-readable and machine-actionable. YAML schemas encode the same principles — they don't change the content philosophy, they make it executable.

---

## Content Source Type Classification

Using the DCT's four content source types (Resource 04), here's how this playbook's content maps:

| Content in This Playbook | DCT Source Type | Governance Model |
|--------------------------|----------------|------------------|
| Legal disclaimers, pricing, compliance statements | **Reference** | Centrally maintained, locally linked. LCR review required. |
| Error messages, confirmations, status notifications | **Operational** | Template-based via Pattern Anatomy. AI-generated within YAML schemas. |
| AI chatbot/tool responses | **Conversational** | AI-guided with principle guardrails from AI-Ready Rules. |
| Value propositions, brand messages, marketing | **Core** | Principle-driven using Coherence Markers. Distributed creation. |

This classification clarifies which governance model applies to each content type in the playbook's [Operating Model](operating-model.md).

---

## Reading Path

If you're new to both document sets, here's the recommended sequence:

1. **DCT 08: Theoretical Foundations** — Understand why coherence works (15 min)
2. **DCT 01: Coherence Markers Worksheet** — Define your non-negotiables (60-90 min with team)
3. **This bridge document** — Understand how the two sets connect (10 min)
4. **Playbook: Decision Frameworks** → **Pattern Anatomy** → **Principle Hierarchy** — The finserv implementation
5. **Playbook: AI-Ready Rules** — Machine-actionable governance
6. **DCT 05: Coherence Metrics Canvas** + **Playbook: Metrics** — Combined measurement framework
7. **Playbook: Maturity Roadmap** — 90-day rollout plan

---

*This bridge document connects the [Distributed Coherence Toolkit](../distributed-coherence-toolkit/00-README.md) (universal framework) to the Content Systems Playbook (regulated finserv implementation). Both by Scott Pierce / Good at Bingo.*
