# Building Auditable AI Agents for High-Stakes Decisions

Most AI demos focus on what models *can* do.  
This portfolio focuses on what AI systems *should* do when decisions matter.

Across this work, I build AI agents that support high-stakes decisions
without delegating judgment to a black box, and without sacrificing
auditability, traceability, or human accountability.

---

## The Core Problem

As AI systems are increasingly used in:
- incident management
- hiring
- financial decisions
- compliance and risk

the biggest failures are rarely model accuracy problems.

They are **governance and control failures**.

Common failure modes include:
- AI making decisions it cannot explain or justify
- Overconfidence in ambiguous or incomplete situations
- No clear accountability when outcomes are challenged
- Decisions that cannot be audited, reproduced, or replayed

This portfolio is a response to those risks.

---

## Design Philosophy (Summary)

Every agent in this portfolio follows the same core principles:

1. **AI never makes the final decision**  
   Models extract facts from unstructured inputs; they do not decide outcomes.

2. **Deterministic code enforces policy**  
   Decision logic is explicit, versioned, testable, and reviewable.

3. **Evidence is mandatory**  
   Every fact used in a decision must be traceable to source material.

4. **Uncertainty triggers escalation**  
   Low confidence, missing information, or conflicting signals are surfaced
   for human review rather than hidden.

5. **Humans retain accountability**  
   Agents provide decision support; people remain responsible.

These principles are implemented consistently across domains and agents.

For a deeper explanation of the thinking behind this approach, see
[`philosophy.md`](https://github.com/AgidiMaro/reliable-ai-agents/blob/main/philosophy.md).

---

## Completed Agents

### Incident Severity Classification Agent
**Domain:** IT Operations & Security  
**Decision:** SEV1 · SEV2 · SEV3 · ESCALATE  

This agent classifies operational incidents using AI-assisted fact extraction
and deterministic severity rules. It explicitly escalates cases with missing,
conflicting, or low-confidence signals.

Key risks addressed:
- Outage misclassification
- Overreaction to noisy or partial signals
- Lack of auditability in incident response

Repository: [`Incident severity classification agent`](https://github.com/AgidiMaro/Incident-Severity-Classification-Agent.git).

---

### Hiring Shortlisting Agent
**Domain:** Hiring & Fairness  
**Decision:** SHORTLIST · DO_NOT_SHORTLIST · ESCALATE  

This agent evaluates candidate CVs against defined role criteria using
evidence-linked fact extraction and deterministic screening logic.
Protected characteristics are detected for transparency but explicitly
excluded from decision-making.

Key risks addressed:
- Bias and proxy discrimination
- Overconfident automated screening
- Opaque or non-reviewable hiring decisions

Repository:  [`Hiring agent`](https://github.com/AgidiMaro/Hiring-Agent.git).

---

### Credit & Loan Decisioning Agent
**Domain:** Credit Risk & Responsible Lending  
**Decision:** APPROVE · DECLINE · ESCALATE  

This agent provides advisory decision support for credit and loan applications.
AI is used strictly for fact extraction from financial documents, while all
recommendations are produced by a deterministic, versioned policy engine.

Uncertain or borderline cases are explicitly escalated to human credit officers.

Key risks addressed:
- Opaque or unchallengeable credit decisions
- Overconfidence in automated affordability assessments
- Inability to audit or replay lending outcomes
- Poor handling of uncertainty in credit risk

Repository:  
[`Credit & Loan Decisioning Agent`](https://github.com/AgidiMaro/Credit-Loan-Decisioning-Agent.git)

---
## What These Agents Demonstrate

Taken together, these systems show that:

- Reliable AI agents are **designed**, not prompted
- Auditability and practical usefulness are compatible
- Explainability improves decision quality, not just compliance
- Escalation is a control safeguard, not a failure

This pattern is reusable across regulated and high-impact environments.

---

## What Comes Next

Future work may apply this same blueprint to domains such as:
- transaction monitoring
- regulatory compliance assessments
- third-party and operational risk decisioning

The underlying design philosophy will remain the same.

---

## Why This Portfolio Exists

This work is not about replacing human judgment.

It is about building AI systems that:
- know their limits
- surface uncertainty early
- can be audited and challenged after the fact
- fit naturally into real-world decision and control processes
