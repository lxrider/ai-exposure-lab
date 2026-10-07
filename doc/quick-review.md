# Quick AI Use Case Review

This review is deliberately short.

Start with one real use case, not a framework or a list of controls.

## 1. Business first

**What are we trying to achieve?**

What result does the team expect?

**Why is AI being used?**

What problem, friction or repetitive task does it solve?

**What has value?**

People, customers, data, knowledge, intellectual property, decisions, operations, reputation, money, availability?

**Why could this use become a problem for the business?**

## 2. Frame the AI use

### Channel

Where does the use happen?

- approved and managed environment;
- approved external service;
- personal / unapproved account;
- supplier or partner environment;
- unknown.

### Exposure

What information reaches AI?

Is all of it necessary?

> **Access right ≠ disclosure authority.**

### Cognitive delegation

What cognitive work are we giving AI?

```text
Summarize → Analyze → Compare → Infer → Reason → Recommend → Plan → Decide
```

### Action delegation

What execution are we delegating to AI?

```text
Read → Search → Create → Send → Modify → Execute → Delete
```

### Agentic authority checkpoint — only if AI can cause an effect

Separate what is technically possible from what has actually been authorized.

```text
USER / SERVICE PERMISSION
What can the principal do?

AGENT TECHNICAL CAPABILITY
What can the agent technically do through its tools or credentials?

DELEGATED TASK AUTHORITY
What may the agent legitimately do for this specific task?
```

Ask:

- Who delegated the authority?
- To which agent or service?
- For which task or purpose?
- Which actions and resources are in scope?
- For how long?
- Can that authority be reduced or revoked?
- Can the resulting effect be traced back to the task and authority that allowed it?

Do not assume that a user's or service's permissions are automatically delegated to AI.

## 3. Break it

Put yourself in an attacker's shoes.

**What value would I target?**

**What could I steal, manipulate, influence, disrupt or abuse?**

**What would be my objective?**

Then remove the attacker.

**What could simply go wrong?**

Consider bad input, wrong reasoning, over-reliance, excessive technical permissions, accidental disclosure, unsafe automated action, authority inferred from ambiguous input, or authority that remains usable after it should have expired or been revoked.

## 4. Define the objective

What must remain true for the business?

Security objectives can remain simple:

```text
CONFIDENTIALITY
The wrong people or AI services must not receive the information.

INTEGRITY
Information, reasoning or decisions must not be improperly altered or influenced.

AVAILABILITY
AI must not unnecessarily disrupt the service or business process.

AUTHORITY
AI must not exercise more authority than was legitimately delegated for the current task.

ACCOUNTABILITY
We must know who remains responsible.

TRACEABILITY
We must be able to reconstruct what happened, who or what caused it, under whose authority and why it was allowed.
```

Not every use case needs all six.

Use only the objectives that matter for the business value at stake.

Examples:

- customer information must not reach an unauthorized service;
- candidate selection must remain reviewable and human-owned;
- an AI-generated command must not be executed blindly in production;
- an agent must not modify production outside the authority delegated for the task;
- significant actions must remain traceable to the task and authority that caused them.

Keep the objective understandable and testable.

## 5. RCCM

### Problem

What is actually wrong?

Do not confuse the problem with the visible symptom.

### Root cause

Why can this situation happen?

Use the Five Whys if useful.

Do not stop at "the user made a mistake".

### Countermeasure

What is the smallest durable response that addresses the cause?

Possible responses include minimizing information, using an approved environment, clarifying disclosure rules, requiring human validation, reducing technical permissions, bounding task authority, requiring approval before authority expands, validating authority before a significant effect, or logging important actions.

## 6. Prove it

Test the countermeasure.

- Can the risky path still happen?
- Can the team achieve the same business result through the safe path?
- Are there obvious bypasses?
- Did we reduce the risk or merely move it?
- Did we create so much friction that people will work around it?

If AI can cause an effect, also test:

- Can it perform an action outside the delegated task authority?
- Can it still act after that authority expires or is revoked?
- Can the resulting effect be traced back to the task and authority that allowed it?

If it fails, learn why and improve it.

## 7. Outcome

Keep the operational decision simple:

```text
OK
OK WITH CONDITIONS
REVIEW NEEDED
STOP
```

Record three things:

**Owner** — who owns the business decision?

**Quick win** — what can we improve now?

**Playbook** — does this use case teach a reusable way of working?
