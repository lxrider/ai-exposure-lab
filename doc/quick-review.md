# Quick AI Use Case Review

This review is deliberately short. Start with one real use case, not a framework or a list of controls.

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

What can AI actually do?

```text
Read → Search → Create → Send → Modify → Execute → Delete
```

## 3. Break it

Put yourself in an attacker's shoes.

**What value would I target?**  
**What could I steal, manipulate, influence, disrupt or abuse?**  
**What would be my objective?**

Then remove the attacker.

**What could simply go wrong?**

Consider bad input, wrong reasoning, over-reliance, excessive permissions, accidental disclosure or an unsafe automated action.

## 4. Define the objective

What must remain true for the business?

Examples:

- customer information must not reach an unauthorized service;
- candidate selection must remain reviewable and human-owned;
- an AI-generated command must not be executed blindly in production;
- an agent must not modify production without the required authorization;
- significant actions must remain traceable.

Keep the objective understandable and testable.

## 5. RCCM

### Problem

What is actually wrong?

Do not confuse the problem with the visible symptom.

### Root cause

Why can this situation happen?

Use the Five Whys if useful. Do not stop at "the user made a mistake".

### Countermeasure

What is the smallest durable response that addresses the cause?

Possible responses include minimizing information, using an approved environment, clarifying disclosure rules, requiring human validation, reducing agent permissions, adding an approval step or logging important actions.

## 6. Prove it

Test the countermeasure.

- Can the risky path still happen?
- Can the team achieve the same business result through the safe path?
- Are there obvious bypasses?
- Did we reduce the risk or merely move it?
- Did we create so much friction that people will work around it?

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
