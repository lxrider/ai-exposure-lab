# AI Exposure Lab

> **Is there a pilot in the plane? ✈️**

Please, take 2 minutes and a blank page.

Generative AI is already being used at work. Employees use ChatGPT, Claude, Gemini and other AI services to write emails, summarize documents, analyze information, understand code or simply work faster.

The problem is simple:

> **Company information can leave the organization through AI without anyone really stopping to ask whether it should.**

A confidential email can be pasted into ChatGPT. Source code can be sent to Claude. A customer document can be uploaded to Gemini. An employee can even bypass the corporate network entirely by using a personal smartphone over 5G.

Depending on the information involved, this can become an unauthorized disclosure and create a real security, privacy, contractual or business risk.

And that is only the first problem.

> **How much cognitive tasks are we starting to delegate to AI?**

Ok... Let's take a cup of coffe :)

---

## Two questions

The first experiments focus on two questions:

> **What are we exposing to AI?**

and:

> **What are we delegating to AI?**

These are different problems, but they meet at the same point:

> **Who is actually in control?**

---

## Information exposure

Having access to company information does not automatically mean being allowed to send it to an external AI service.

> **Access right ≠ Disclosure authority**

A developer may legitimately access source code.

That does not automatically mean the code can be sent to an external AI provider.

The same applies to:

* customer information;
* internal emails;
* architecture;
* financial information;
* security data;
* credentials;
* confidential documents.

The destination matters too.

```text
Personal AI account
        ≠
Organization-approved AI service
```

And the network does not solve everything.

A corporate device can use a personal AI account.

A personal smartphone can bypass corporate controls completely.

---

## Cognitive delegation

There is also a difference between asking AI to:

```text
Rewrite
Summarize
Explain
Suggest
Recommend
Decide
Act
```

This is not a formal scale.

It simply shows that AI can move from assistance toward greater involvement in human judgement.

Rewriting an email is not the same as deciding which security control should be implemented.

So another principle appears:

> **Assistance ≠ Decision**

At some point, somebody must still own the judgement and the consequences.

---

## MVP

The first MVP looks at a human employee using an external generative AI service for professional work.

For each scenario, we ask:

```text
What information is involved?
Why is AI needed?
Which AI receives it?
What are we asking the AI to do?
Who can authorize the disclosure?
Who owns the final decision?
```

Then we try to reach a simple answer:

```text
ALLOWED
ALLOWED WITH CONDITIONS
NOT ALLOWED
UNKNOWN
```

If these questions are not enough, the scenarios should show us why.

---

## For now

We are deliberately not starting with:

* prompt injection;
* RAG;
* MCP;
* autonomous agents;
* model poisoning;
* AI infrastructure security;
* detailed technical controls;
* full enterprise AI governance.

The lab should only grow when the problem requires it.

---

## Approach

```text
UNDERSTAND
   ↓
TEST
   ↓
LEARN
   ↓
BUILD
```

Start with the problem.

Question the assumptions.

Test them against reality.

Then build only what is needed.

**Work in progress.**
