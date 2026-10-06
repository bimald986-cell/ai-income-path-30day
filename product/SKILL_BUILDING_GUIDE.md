# AI Skill Building Guide

> **Status:** Living working document
>
> This document captures the principles, decision logic, market lessons, and quality standards learned during the 30-day AI income path. It is the guiding document for designing, reviewing, testing, and improving every AI skill we build. Update it when later lessons produce a better rule.

## 1. Purpose

We are not building prompt collections that merely produce polished text. We are building useful AI skills that can receive imperfect real-world information, reason through a defined workflow, identify uncertainty, make appropriate decisions when evidence is sufficient, ask for clarification when it is not, and save meaningful human time and effort.

The initial product direction under validation is a **Client Operations Assistant for freelancers and solo businesses**. Individual skills may later become components of this broader assistant.

---

## 2. Owner's Three Core Principles

A good AI skill should:

1. **Make the right decision with the information it has.**
2. **Work independently and seek clarification when more information is needed.**
3. **Handle complex tasks in a way that saves human time and effort.**

These are foundational requirements, not optional features.

---

## 3. The Core Decision Loop

Every operational skill should follow this pattern where appropriate:

**Observe → Gather → Verify → Decide or Escalate → Recommend → Human Approval when required → Act → Document**

### Observe
Understand the request, event, document, or change that triggered the skill.

### Gather
Collect the relevant available information before reaching a conclusion. Depending on the skill, this may include contracts, proposals, prior messages, approved requirements, project records, invoices, policies, or user-provided context.

### Verify
Compare the new request or situation against the authoritative information. Do not treat assumptions as facts.

### Decide or Escalate
If the evidence is sufficient, classify the situation and explain the reasoning. If the evidence is incomplete, contradictory, or ambiguous, explicitly record what is missing and ask the owner for clarification.

### Recommend
Give practical options, consequences, and suggested next steps rather than only describing the problem.

### Human Approval When Required
A skill must distinguish internal analysis from external action. Decisions with meaningful contractual, financial, legal, reputational, publishing, or customer consequences should use an appropriate owner-approval gate unless the owner has explicitly delegated that class of action.

### Act
After the required approval or when operating within clearly delegated authority, perform or prepare the next action.

### Document
Preserve the decision, evidence used, uncertainty, approval, and outcome when that history will matter later.

---

## 4. The Most Important Uncertainty Rule

**Never manufacture confidence.**

When a skill cannot confidently determine the correct answer:

1. Gather additional relevant information that is already available.
2. Identify the exact ambiguity or conflict.
3. List the missing information required to resolve it.
4. State what can and cannot currently be concluded.
5. Ask the owner or appropriate human for the smallest useful clarification.
6. Do not take an irreversible or external action while the required decision remains unresolved.

A useful internal output format is:

- **Status:** Determined / Likely / Ambiguous / Insufficient information
- **Known:** Verified facts
- **Evidence:** Where those facts came from
- **Missing:** Information still required
- **Assessment:** What can currently be concluded
- **Recommended next step:** What should happen next
- **Approval required:** Yes / No, with reason
- **External action taken:** None until authorized, when approval is required

---

## 5. Example: Scope Guardian Logic

### Situation
Original agreement:

> Five-page informational business website: Home, About, Services, Contact, FAQ. Includes two revision rounds.

Client later asks for customer accounts, login functionality, and a dashboard showing previous orders.

### Correct skill behavior

The skill should not immediately draft and send a friendly acceptance.

It should:

1. Retrieve and inspect the original agreement and related approved requirements.
2. Compare each requested feature with the agreed deliverables.
3. Determine whether the request appears inside or outside the documented scope.
4. Explain the evidence behind that assessment.
5. Identify likely implications for work, time, cost, testing, or delivery.
6. Recommend the appropriate next steps.
7. Prepare a response or change-request draft for owner review when useful.
8. Avoid communicating externally until the appropriate approval exists.

### Ambiguous version

Suppose the agreement instead says:

> Business website including standard customer functionality and up to two revision rounds.

The phrase **standard customer functionality** is ambiguous.

The skill should search available project records for an agreed definition. If none exists, it should not decide that the new features definitely are or are not included. It should document the ambiguity and seek clarification from the owner before responding to the client.

This example gives us an important reusable principle:

> **Investigate first. Escalate uncertainty. Never hide missing information behind a confident answer.**

---

## 6. From Prompt to Real Skill

A weak prompt might say:

> Write a professional response to this client.

A real operational skill asks:

- What is the client requesting?
- What was originally agreed?
- Which source is authoritative?
- Has the request changed the scope?
- What information is missing?
- How confident is the classification?
- What are the likely consequences?
- What options does the owner have?
- Does the next action require approval?
- What should be documented for future decisions?

The value comes from the **decision process**, not merely fluent writing.

---

## 7. Market Lesson: Build Around Pain, Not Novelty

Before building a skill, distinguish three levels:

### Interesting problem
Something that sounds useful but may not justify paying for a solution.

Example: "Writing proposals takes time."

### Painful problem
Something that repeatedly costs the user time, money, customers, attention, or stress.

Example: "I spend hours turning messy client messages into proposals, and prospects sometimes disappear afterward."

### Product opportunity
A repeated painful problem where an AI skill can perform meaningful work reliably.

Example workflow:

**Messy Client Brief → Extract Requirements → Identify Missing Information → Clarify → Define Scope → Risk Check → Proposal Draft → Owner Review**

---

## 8. Three Questions for Validating Every Skill Idea

Before investing substantial effort, ask:

### Frequency
Does this problem happen repeatedly to the target user?

### Pain
Does it cost meaningful time, money, customers, attention, or stress?

### AI Fit
Can a well-designed AI skill reliably perform meaningful parts of the work rather than merely provide generic advice?

A skill idea becomes more promising when all three are strong.

---

## 9. Current Product Direction: Client Operations Assistant

During Day 3, the preferred direction became **Client Operations Assistant**, rather than treating Proposal Builder or Scope Guardian as isolated products.

The reasoning is that freelancers and solo businesses face a connected sequence of operational work. A broader assistant can contain focused skills that cooperate while each remains testable and understandable.

Potential components include:

- Client intake and brief structuring
- Missing-information detection
- Proposal building
- Scope Guardian / change-request detection
- Client follow-ups
- Weekly client summaries
- Invoice follow-up support
- Recurring administrative reviews
- Project-risk checks
- Decision and approval tracking

This list is exploratory until the final skill list is locked during the 30-day plan.

---

## 10. Example Component: Proposal Builder

A stronger proposal skill should not simply "write a proposal."

Potential workflow:

**Raw client information → Structure brief → Detect missing requirements → Ask targeted questions → Define scope → Identify assumptions/risks → Prepare proposal → Owner review**

Human judgment should remain explicit for information the skill cannot legitimately infer, such as unprovided pricing, commercial commitments, or timelines requiring owner confirmation.

---

## 11. Example Component: Scope Guardian

Potential inputs:

- Original contract or statement of work
- Approved proposal
- Approved requirements
- Relevant project history
- New client request

Potential outputs:

- Scope classification
- Evidence and reasoning
- Confidence/uncertainty status
- Missing information
- Possible schedule/work/cost implications
- Recommended next step
- Suggested clarification questions
- Draft client response or change request
- Approval requirement

The skill should never reduce a nuanced contractual question to a confident yes/no when the underlying documentation is ambiguous.

---

## 12. Independence Does Not Mean Uncontrolled Autonomy

A good skill should complete as much work as it safely can without repeatedly asking the human obvious questions.

However, independence does not mean guessing or taking consequential external actions without authority.

A mature skill knows the difference between:

- information it can retrieve,
- conclusions supported by evidence,
- reasonable recommendations,
- decisions reserved for the owner,
- and actions it has actually been authorized to perform.

The goal is **maximum useful independence with appropriate escalation**, not maximum action at any cost.

---

## 13. Skill Design Template

Every new skill should eventually answer these questions before it is considered ready:

### Problem
What painful repeated problem does this solve?

### Target user
Who experiences this problem?

### Trigger
What causes the skill to run?

### Inputs
What information can it receive or retrieve?

### Authoritative sources
Which inputs should take precedence when information conflicts?

### Workflow
What ordered steps should it follow?

### Decision rules
What can it decide from evidence?

### Uncertainty rules
When must it seek clarification?

### Boundaries
What must it never assume or do automatically?

### Outputs
What useful result should it produce?

### Approval gates
Which actions require human authorization?

### Verification
How does it check its own work?

### Documentation
What decision history should be preserved?

### Completion criteria
How do we know the task is actually finished?

### Failure behavior
What should happen when required information, tools, permissions, or confidence are missing?

---

## 14. Quality Checklist

Before calling an AI skill good, verify that it:

- solves a specific repeated problem;
- uses available evidence before guessing;
- distinguishes facts, assumptions, and missing information;
- asks focused clarification questions only when necessary;
- can perform multi-step work independently;
- provides reasoning or evidence for important classifications;
- produces actionable outputs rather than generic advice;
- has explicit boundaries;
- knows when owner approval is required;
- verifies important work before declaring success;
- documents consequential decisions where useful;
- has measurable completion criteria;
- saves meaningful human effort;
- fails safely when information or permissions are insufficient.

---

## 15. Working Rule for Future Skill-Building Sessions

When designing or reviewing any skill in this repository, use this document as the default guide.

Do not blindly follow it when a future lesson reveals a better method. Instead:

1. identify the new lesson,
2. test whether it improves the framework,
3. update this document,
4. then apply the improved rule to future skills.

The guide should become stronger as the project progresses.

---

## 16. Lessons Captured So Far

### Day 2
- Good skills make decisions from available information.
- Good skills work independently.
- Good skills ask for clarification when information is genuinely insufficient.
- Good skills handle complex work and save human effort.
- Useful procedural skills need boundaries, verification, examples, and measurable completion criteria.

### Day 3
- Validate painful recurring problems before building.
- Frequency, pain, and AI fit are useful screening criteria.
- Client operations appears broader and potentially more useful than a single isolated writing tool.
- Scope decisions should be evidence-based.
- Ambiguity should be documented, not hidden.
- AI should gather available information before escalating.
- When uncertainty remains, ask the owner rather than guessing.
- Do not automatically respond to a client before verification and the appropriate approval.
- The preferred current direction is a **Client Operations Assistant** containing focused operational skills.

---

## 17. Next Updates

This document should be updated as we complete:

- final Day 3 positioning and market validation;
- Day 4 final skill selection;
- implementation architecture;
- testing standards;
- packaging and pricing lessons;
- real-user feedback;
- post-launch improvements.

The objective is for this file to evolve from a learning notebook into a reusable **skill-building operating standard** for future AI products.

---

## 18. Day 4 — Integrated Operations Partner Lessons

Day 4 buyer exercises materially changed the product hypothesis.

### Owner's buying priorities

1. A system that filters large amounts of available information and intelligently prioritizes what deserves attention.
2. A system that independently handles recurring daily work and saves meaningful owner time.
3. A system that conducts market research and supports market outreach.

### Explainability rule

For important recommendations, the system must explain **why** it made the decision and show the evidence/data that influenced it.

A useful prioritization decision should consider:
- available evidence and authoritative operating standards;
- signal versus noise versus operational-improvement opportunity;
- expected outcome/value;
- consequences of delay and dependencies;
- actual risk;
- uncertainty and missing/conflicting information.

**New principle:** The AI earns authority through evidence, not confidence.

### Autonomy rule

**Autonomy follows consequence.**

Separate authority into:
- Observe;
- Act within explicit reversible guardrails;
- Seek approval for consequential actions until that action class is deliberately delegated.

### Outcome rule

Do not reward the operator for looking busy. Measure qualified opportunities, useful responses, conversions, owner time saved, correct work completed, risk prevented, and progress toward objectives rather than raw message/task volume.

### Self-validation rule

When the buyer is uncertain, do not invent a persona and build blindly.

The integrated AI Operations Partner's first commercial assignment is to use its own market-validation, prioritization, and outreach-preparation capabilities to help identify its market and acquire its first paying customer.

The initial segment order is a hypothesis:
1. solo consultant/coach;
2. creator;
3. tiny agency;
4. small online-business/SaaS founder.

Research should actively seek disconfirming evidence, not merely support the owner's initial ranking.

### Morning operating brief

A useful daily brief should answer:
1. How is the product doing today?
2. What is happening in the market?
3. What changed or was observed that could affect us?
4. What meaningful work happened in the last 24 hours, including outreach outcomes?
5. What should we do today, and why?
6. What genuinely needs owner approval?

### Product architecture lesson

The original small skills can remain useful internal capabilities, but the MVP is tested as one integrated operating product:

**Observe → Gather → Understand → Filter → Prioritize → Explain → Act within authority → Verify → Measure → Report → Learn**

See `product/AI_OPERATIONS_PARTNER_MVP.md` for the current testable specification.
