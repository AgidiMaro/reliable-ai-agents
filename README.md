# Building Auditable AI Agents for High-Stakes Decisions

Most AI demos focus on what models *can* do.
This portfolio focuses on what AI systems *should* do.

Across this work, I build AI agents that support high-stakes decisions
without delegating judgment to a black box.

## The Core Problem

As AI systems are increasingly used in:
- incident management
- hiring
- financial decisions
- compliance and risk

the biggest failures are not model accuracy problems.
They are **governance failures**.

Common failure modes include:
- AI making decisions it cannot justify
- Overconfidence in ambiguous situations
- No clear accountability when things go wrong
- Inability to audit or replay decisions

This portfolio is a response to those failures.

## My Design Philosophy

Every agent in this portfolio follows the same principles:

1. **AI never makes the final decision**  
   Models extract facts only.

2. **Deterministic code enforces policy**  
   Decision logic is explicit, testable, and reviewable.

3. **Evidence is mandatory**  
   Every extracted fact must point to source text.

4. **Uncertainty triggers escalation**  
   Ambiguous cases are surfaced to humans, not hidden.

5. **Humans retain accountability**  
   Agents advise; people decide.

These principles are implemented consistently across domains.

## Completed Agents

### Incident Severity Classification Agent
**Domain:** IT Operations & Security  
**Decision:** SEV1 · SEV2 · SEV3 · ESCALATE  

This agent classifies operational incidents using AI-assisted fact extraction
and deterministic severity rules. It explicitly escalates cases with missing,
conflicting, or low-confidence signals.

Key risks addressed:
- Outage misclassification
- Overreaction to noisy signals
- Lack of auditability in incident response

https://github.com/AgidiMaro/Incident-Severity-Classification-Agent.git

---

### Hiring Shortlisting Agent
**Domain:** Hiring & Fairness  
**Decision:** SHORTLIST · DO_NOT_SHORTLIST · ESCALATE  

This agent evaluates candidate CVs against role criteria using evidence-linked
fact extraction and deterministic screening logic. Protected characteristics
are explicitly excluded from decision-making, and uncertain cases are escalated.

Key risks addressed:
- Bias and proxy discrimination
- Overconfident AI screening
- Opaque hiring decisions

https://github.com/AgidiMaro/Hiring-Agent.git

## What These Agents Demonstrate

Taken together, these systems show that:

- Reliable AI agents are **designed**, not prompted
- Governance can be embedded directly into system architecture
- Explainability does not require sacrificing usefulness
- Escalation is a feature, not a failure

This pattern is reusable across regulated and high-impact domains.

## What Comes Next

Future work may apply this same blueprint to domains such as:
- credit and loan decisioning
- transaction monitoring
- compliance assessments

The core design philosophy will remain the same.

---

## Why This Portfolio Exists

This work is not about replacing human judgment.

It is about building AI systems that:
- know their limits
- surface uncertainty
- can be audited after the fact
- fit naturally into real-world decision processes
