# Problem V1

## The problem

Generative AI makes it extremely easy to send company information to an external service.

An employee may simply want to:

* rewrite an email;
* understand some code;
* summarize a document;
* analyze information;
* save time.

The security question is not:

> **Can employees use AI?**

It is:

> **Can this person provide this information to this AI service for this purpose?**

---

## Access is not disclosure

A user may legitimately have access to company information.

That does not automatically mean they are allowed to send it to an external AI service.

> **Access right ≠ Disclosure authority**

Example:

A developer may need access to source code to do their job.

That does not automatically mean the same code may be sent to ChatGPT, Claude or another external service.

---

## Information matters

Not all information has the same value.

A label such as `Internal` or `Confidential` can help, but the most useful question is:

> **What could happen if this information were disclosed?**

A code fragment may be harmless.

Another may expose:

* credentials;
* internal architecture;
* proprietary logic;
* vulnerabilities.

The same applies to emails, documents, customer data or internal plans.

---

## The destination matters

The same information can create different exposure depending on where it is sent.

```text
Personal AI account
        ≠
Organization-approved AI service
```

The AI service should therefore be considered a recipient of company information.

The network path also matters, but it does not decide whether the use is authorized.

For example:

```text
Corporate laptop
+ Corporate network
+ Personal AI account
```

may still be an unauthorized use.

And:

```text
Home network
+ Approved corporate AI account
```

may still be legitimate.

---

## The decision

For each use case, ask:

```text
What information?
Who can access it?
Who may disclose it?
Why is AI needed?
Which AI service receives it?
How much information is really necessary?
Who decides?
```

Then keep the outcome simple:

```text
ALLOWED
ALLOWED WITH CONDITIONS
NOT ALLOWED
UNKNOWN
```

One principle applies everywhere:

> **Expose only what is necessary for the task.**

---

## Shadow AI

Shadow AI is not always the root problem.

It may be a symptom of:

* unclear rules;
* no useful approved tool;
* slow approval;
* too much friction.

A safe path must also be usable.

---

## MVP

The first MVP focuses on one situation:

> **A human employee intentionally provides company information to an external generative AI service to perform professional work.**

The goal is to test this decision model against a few realistic scenarios.

Not to solve all AI governance.

---

## Out of scope

For now:

* prompt injection;
* RAG;
* MCP;
* autonomous agents;
* model poisoning;
* model training;
* hallucination management;
* AI-generated decisions;
* detailed technical controls;
* full enterprise AI governance.

These topics may come later if the lab shows they are needed.

---

## Working principle

Technology may help enforce a decision.

It cannot make the decision for us.

> **Understand the use. Decide what is acceptable. Make the safe path usable. Review when reality changes.**
