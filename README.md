# AI Exposure Lab

A practical cybersecurity lab about the professional use of generative AI and the exposure of company information.

## The idea

Generative AI entered everyday life very quickly.

Employees may already use ChatGPT, Claude, Gemini or other AI tools personally before their organization has defined how they should be used at work.

Then a professional need appears.

```text
Employee
   ↓
Professional task
   ↓
Company information
   ↓
AI service
```

The employee may simply want to rewrite an email, understand some code or summarize a document.

The first security question is not:

> How do we secure AI?

It is:

> **Can this person provide this information to this AI service for this purpose?**

## A first principle

Having access to information does not automatically mean being allowed to share it with an external service.

> **Access right ≠ Disclosure authority**

The same question applies to source code, customer emails, internal documents, architecture diagrams or any other company information.

## The problem

The decision depends on more than the information itself.

We need to understand:

* what information is involved;
* who is using it;
* why AI is needed;
* which AI service receives it;
* how much information is really necessary;
* who has authority to allow the disclosure.

The network is only part of the problem.

A corporate laptop may use a personal AI account.

A personal smartphone may bypass the corporate network completely.

So the real question is:

> **How much control does the organization actually have over the exposure?**

## The approach

Start small.

Take one real use case and ask:

```text
What information?
Who can access it?
Who may disclose it?
Why?
To which AI?
How much is necessary?
Who decides?
```

Then make a simple decision:

```text
ALLOWED
ALLOWED WITH CONDITIONS
NOT ALLOWED
UNKNOWN
```

Learn from real scenarios and improve the model.

## MVP

The first MVP focuses on one situation:

> **A human employee intentionally provides company information to an external generative AI service to perform professional work.**

For now, the project does not cover:

* prompt injection;
* RAG;
* MCP;
* autonomous agents;
* model poisoning;
* AI infrastructure security;
* hallucination management;
* full enterprise AI governance.

These may come later.

## Guiding question

> **Is there a pilot in the plane?**

In other words:

> **Who decides whether company information can be exposed to AI, under which conditions, and who owns that decision?**

## Status

**Work in progress.**

Start with the problem. Test assumptions. Learn from reality. Improve.
