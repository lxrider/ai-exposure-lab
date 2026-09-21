# Scenarios

These scenarios test two simple questions:

> **What are we exposing to AI?**

> **What are we delegating to AI?**

The goal is not to prove that our reasoning works. It is to find where it becomes unclear or breaks.

## Scenario 1 — Public information

A marketing employee asks an external AI service to summarize a press release already published on the company website.

**Exposure:** the information is already public.

**Delegation:** the AI is summarizing existing content, not making a business decision.

**Decision:**

```text
ALLOWED
```

This gives us a useful baseline: using an external AI service is not automatically a security problem.

## Scenario 2 — Internal information, personal AI

A sales employee copies an internal email into a personal ChatGPT account to prepare for a customer meeting. The email contains customer context, internal comments and possible pricing information.

**Exposure:** the employee is allowed to read the email, but that does not automatically mean they can send it to an external personal AI service.

> **Access right ≠ Disclosure authority**

**Delegation:** the AI is mainly being used to summarize and help prepare the meeting. The main issue here is information exposure.

**Decision:**

```text
NOT ALLOWED
```

for the personal AI account.

A different destination, or a minimized version of the information, could lead to another answer.

This scenario shows that a legitimate business need does not automatically make the disclosure acceptable.

## Scenario 3 — Approved AI, unclear responsibility

A security engineer uses an organization-approved AI service. They provide a small extract of an internal architecture and ask:

> **Which security control should we implement first?**

The engineer is authorized to access the architecture. The AI service is approved. No credentials or customer information are included.

**Exposure:** the disclosure may be acceptable.

**Delegation:** the AI is no longer only explaining information. It is recommending a security priority that may influence architecture, budget and risk.

**Decision:**

```text
UNKNOWN
```

The problem is not necessarily the AI service.

Another question has appeared:

> **Who owns the decision?**

Who validates the recommendation? Who accepts the risk? Who remains accountable if it is wrong?

This is the question behind:

> **Is there a pilot in the plane?**

Governance is not only about deciding what information may leave. It is also about understanding how much judgement is being delegated and who remains responsible.

## What we learned so far

The three situations are already different:

```text
Low exposure
+ Limited delegation
= Simple decision
```

```text
Higher exposure
+ Limited delegation
= Information governance problem
```

```text
Acceptable exposure
+ Greater delegation
= Accountability problem
```

That is enough for now.

The next step is not to add more rules. It is to challenge these scenarios and see what we missed.
