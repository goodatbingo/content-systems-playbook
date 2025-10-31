# Content Systems Playbook
## Canva Presentation Outline

---

## Slide 1: Title Slide
**Content Systems Playbook**
Bridging Pattern Libraries to Systematic Content Operations

A focused framework for AI-enabled content operations in regulated financial services

---

## Slide 2: Purpose & Vision
**Purpose**
High-level steps and considerations for bridging pattern libraries to systematic content operations

**The Challenge**
Moving from ad-hoc content decisions to systematic operations

**The Solution**
A complete framework for scalable, consistent, and AI-ready content design systems

---

## Slide 3: Five Key Components

1. **Decision frameworks** that guide content choices
2. **Anatomical patterns** that define content structure
3. **Principle hierarchies** that resolve conflicts
4. **AI-ready systems** that enable automation
5. **Maturity assessments** that guide evolution

---

## Slide 4: Current Context
**Environment Snapshot**

- Legacy enterprise with strong AI leadership interest
- Internal AI tool exists, built before comprehensive strategy
- Compliance is critical: FINRA/SEC constraints + internal governance
- Content team: ~20 within ~100 design org
- CMS exists (AEM) but not yet optimized for content workflows
- Other functions (research, brand, marketing) seeking access

---

## Slide 5: Decision Frameworks
**The Problem**
When teams don't agree on balancing short vs. thorough, decisions stall and quality slips

**The Solution**
Turn fuzzy debates into clear choices in under a minute

**Key Tension**
Conciseness vs. Completeness

**Framework Steps**
1. Assess User Context (mid-task, decision point, error, onboarding)
2. Evaluate Risk Level (high/medium/low)
3. Apply the Formula
4. Test Against Principles

---

## Slide 6: Decision Frameworks - Risk-Based Approach

**HIGH RISK** (Financial, Legal, Privacy)
→ Completeness Wins
- Include all necessary information
- Use progressive disclosure
- Provide expandable details

**MEDIUM RISK** (Account settings, Preferences)
→ Balanced Approach
- Core information inline
- Details on demand
- Clear learn more paths

**LOW RISK** (Navigation, UI interactions)
→ Conciseness Wins
- Minimum viable message
- Action-focused
- Trust user knowledge

---

## Slide 7: Pattern Anatomy
**The Problem**
Patterns are great until you hit a case the examples don't cover

**The Solution**
Turn "copy-and-paste the closest thing" into "assemble the right message from core parts"

**Core Structure Components**
1. **WHAT HAPPENED** (Required) - 5-10 words max
2. **WHY IT HAPPENED** (Contextual) - Include when user can prevent recurrence
3. **USER IMPACT** (Contextual) - When consequences aren't obvious
4. **RECOVERY ACTION** (Required) - Specific next step
5. **SUPPORT PATH** (Contextual) - When self-service unlikely to succeed

---

## Slide 8: Pattern Anatomy - Examples

**Low Risk + User Fixable**
- What: Your email address isn't valid
- Recovery: Check for typos and try again

**High Risk + Technical Issue**
- Severity: ⚠️ Payment Error
- What: Your payment couldn't be processed
- Why: The bank declined this transaction
- Impact: Your order hasn't been placed
- Recovery: Try a different payment method
- Support: If this continues, contact support (Error: PAY-4429)

---

## Slide 9: Principle Hierarchy
**The Problem**
Flat voice-and-tone lists break when principles collide

**The Solution**
Clear hierarchy so teams know what wins when

**Level 1 (Non-negotiable)**
- Accuracy → wins over everything
- Accessibility → wins over brevity/aesthetics

**Level 2 (Strategic)**
- Clarity → prioritize over brevity in high-stakes contexts
- Efficiency → support quick task completion when safe

**Level 3 (Brand)**
- Warmth → permitted when it never obscures risk, facts, or next steps

---

## Slide 10: Principle Hierarchy - Conflict Resolution

**Resolution Process**
1. Any Level 1 involved? → Level 1 wins
2. Level 2 vs Level 2? → Apply context rules
3. Level 3 always yields to Levels 1-2

**Context Matrix Examples**
- Error states: Clarity wins, brevity yields, warmth yields
- Legal content: Clarity wins, formality wins, warmth loses
- Onboarding: Clarity wins, warmth wins
- Power user tools: Brevity wins

---

## Slide 11: AI-Ready Rules
**Making It Machine-Actionable**

**AI Role Definition**
- Expertise: Senior content designer
- Domain: Financial services regulation, WCAG 2.1, mobile-first patterns
- Authority: Can decide wording within guidelines
- Constraints: Grade 8 reading level, forbidden phrases, no guarantees

**Rules Engine**
- Structured YAML schemas for each content type
- Context assembly (persistent + session + request)
- Quality gates with validation thresholds
- Human-in-loop triggers for high-risk content

---

## Slide 12: AI-Ready Rules - Quality Gates

**Validators**
- Structural: Ensure required elements present
- Compliance: Forbidden phrases, disallowed constructs
- Accessibility: Reading level max grade 8
- Accuracy: Assertion sources required

**Human Review Triggers**
- Money movement
- Financial advice
- Pricing or rate mentions
- Confidence below threshold

**Audit Fields**
Assertion source, risk level, reviewer, review date, change log reference

---

## Slide 13: 90-Day Maturity Roadmap

**Phase 1: Foundation (Weeks 1-2)**
- Inventory top content types in authenticated journeys
- Define "good" with examples mapped to anatomy
- Stand up terminology and forbidden claims list

**Phase 2: AI Integration (Weeks 3-5)**
- Convert patterns to prompts and schemas
- Implement validation checks
- Pilot within content design team

**Phase 3: Compliance by Design (Weeks 6-8)**
- LCR partnership: codify do/don't patterns
- Add audit fields and review workflows
- Define rollback procedures

**Phase 4: Scale & Learn (Weeks 9-12)**
- Expand to more content types
- Capture edit deltas to evolve rules
- Report on metrics and update roadmap

---

## Slide 14: Operating Model

**RACI**
- Accountable: AI Director Content Strategy
- Responsible: Content design guild, tool owner, taxonomy owner
- Consulted: LCR, brand, research, marketing, engineering
- Informed: Design leadership, product owners

**Workflows**
1. **Authoring**: Designer uses AI with business rules → structural pass → compliance lint
2. **Review**: LCR receives diff with rule citations
3. **Publish**: Change log auto-updated, rollback plan attached
4. **Learn**: Edits and outcomes feed back to rules

---

## Slide 15: Key Artifacts

**Pattern Library as System**
- Anatomy + rules + examples

**Prompt Packs**
- By content type and severity

**Compliance Glossary**
- Disallowed constructs

**Audit Schema**
- assertion_source, risk_level, review_status
- reviewer, review_date, change_log

---

## Slide 16: Metrics Framework

**Efficiency**
- Cycle time per content item
- Authoring time saved
- Reuse rate

**Quality**
- Structural pass rate
- LCR rework rate
- Accessibility pass rate

**Risk**
- Compliance incidents
- Rollback frequency
- High-risk content without review

**Impact**
- Reduction in support tickets
- Task success
- Abandonment in key flows

---

## Slide 17: Implementation Strategy

**Start Internal First**
De-risk in internal operations before client-facing experiences

**Structure Knowledge for AI**
- Taxonomy, metadata, authoritative sources
- Fix search as part of AI readiness

**CMS Alignment**
Configure AEM for content team governance and versioned change logs

**Access Model**
Limited expansion to research/brand with clear boundaries and audits

---

## Slide 18: Next Steps - Immediate Actions

1. **Confirm pilot scope and owners**
   - Define initial content types to target
   - Assign accountability and responsibility

2. **Integrate compliance lint rules into internal tool**
   - Forbidden phrases check
   - Structural validation
   - Human-in-loop triggers

3. **Stand up dashboards for four metric families**
   - Efficiency, Quality, Risk, Impact

4. **Schedule LCR "diff clinic"**
   - Codify do/don't patterns
   - Create review workflow
   - Establish escalation paths

---

## Slide 19: Example - High-Risk Payment Failure

**Scenario**: Mobile, authenticated user, payment declined

**What**: Your payment couldn't be processed

**Why**: This card was declined by your bank

**Impact**: Your order wasn't placed

**Recovery**: Try a different card or contact your bank

**Support**: If this continues, chat with support and share ID PAY-####

---

## Slide 20: Why This Matters

**From Pattern Library to System**
Moving from static examples to generative frameworks

**AI-Enabled Operations**
Machine-actionable guidance with human oversight

**Compliance Built-In**
Regulatory guardrails automated and auditable

**Scalable Quality**
New team members can construct appropriate content for novel situations

---

## Slide 21: The Transformation

**Before: Ad-hoc**
- Copy closest example
- Debate each decision
- Inconsistent quality
- Slow to scale

**After: Systematic**
- Assemble from anatomy
- Apply decision framework
- Consistent quality
- AI-enabled speed

---

## Slide 22: Key Takeaways

1. **Decision frameworks** turn debates into clear choices
2. **Pattern anatomy** enables assembly vs. copying
3. **Principle hierarchy** resolves conflicts systematically
4. **AI-ready rules** make guidance machine-actionable
5. **90-day roadmap** provides clear path to implementation

---

## Slide 23: Questions & Discussion

**Get Started**
- New to the system? Start with Context
- Need to make a content decision? See Decision Frameworks
- Creating new patterns? Reference Pattern Anatomy
- Implementing AI tools? Review AI-Ready Rules
- Planning rollout? Follow the Maturity Roadmap

---

## Slide 24: Thank You

**Content Systems Playbook**
From pattern libraries to systematic content operations

For more information, visit:
github.com/goodatbingo/content-systems-playbook
