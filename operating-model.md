# Operating Model

## RACI Snapshot

- **Accountable**: AI Director Content Strategy
- **Responsible**: Content design guild, tool owner, taxonomy owner
- **Consulted**: LCR, brand, research, marketing, engineering, Apps and Infra teams
- **Informed**: Design leadership, product owners

## Workflows

### 1. Authoring

Designer uses AI with business rules → structural pass → compliance lint → submit for review if trigger

### 2. Review

LCR receives diff with rule citations; approve, amend, or reject with structured reasons

### 3. Publish

Change log auto-updated; rollback plan attached; metrics hooks registered

### 4. Learn

Edits and outcomes feed back to rules and examples

## Content Source Types

Governance expectations differ by content type. Using the DCT's [Content Source Types Matrix](../distributed-coherence-toolkit/04-content-source-types-matrix.md):

| Content in This Playbook | DCT Source Type | Governance Model |
|--------------------------|----------------|------------------|
| Legal disclaimers, pricing, compliance | **Reference** | Centrally maintained, LCR review required |
| Error messages, confirmations, notifications | **Operational** | Template-based via Pattern Anatomy + YAML schemas |
| AI chatbot/tool responses | **Conversational** | AI-guided with guardrails from AI-Ready Rules |
| Value propositions, brand messaging | **Core** | Principle-driven, distributed creation |

## Artifacts

- **Pattern library as system**: anatomy + rules + examples
- **Prompt packs** by content type and severity
- **Compliance glossary** and disallowed constructs
- **Audit schema**: assertion_source, risk_level, review_status, reviewer, review_date, change_log

---

[← Back to README](README.md) | [← Previous: Maturity Roadmap](maturity-roadmap.md) | [Next: Metrics →](metrics.md)
