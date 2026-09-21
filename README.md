# AI Exposure Lab

> **Is there a pilot in the plane? ✈️**

Generative AI is already used at work. Employees use ChatGPT, Claude, Gemini and other AI services with emails, documents, source code, customer information or internal data.

Sometimes nobody has clearly decided whether that information should be sent there. This creates a simple governance problem:

> **Who can use what information, with which AI, when, why and under which conditions?**

Another question quickly follows:

> **How much human judgement are we willing to delegate to AI?**

## The problem

A developer may legitimately have access to source code. That answers one question: **who can access it?**

It does not answer another: **can they send it to an external AI service?**

> **Access right ≠ Disclosure authority**

The same applies to customer emails, financial information, architecture, credentials or confidential documents.

To understand an AI use case, we can start with a few simple questions:

```text
WHO?         Who is using the information?
WHAT?        What information is involved?
WHY?         Why is AI needed?
WHEN?        In which business context?
WHERE?       Which AI service receives it?
HOW?         Corporate device, personal account, smartphone over 5G?
HOW MUCH?    How much information is really necessary?
WHO DECIDES? Who can authorize this use?
```

The goal is not to create a huge framework. It is simply to understand the situation well enough to make a sensible decision.

## What are we delegating?

Information exposure is only one side of the problem. There is also a difference between asking AI to:

```text
Rewrite → Summarize → Explain → Suggest → Recommend → Decide → Act
```

This is not a formal scale. It simply shows that AI can move from assistance towards greater involvement in human judgement.

Rewriting an email is not the same as recommending which security control should be implemented. The question therefore becomes:

> **What are we asking the AI to do, and who remains responsible for the result?**

## A simple way in

For now, the model remains deliberately simple:

```text
Understand the use
        ↓
Understand the information
        ↓
Understand the destination
        ↓
Understand the level of delegation
        ↓
Decide what is acceptable
```

The outcome can also remain simple:

```text
ALLOWED
ALLOWED WITH CONDITIONS
NOT ALLOWED
UNKNOWN
```

`UNKNOWN` is not a failure. It means we have found something that requires a decision.

## What this lab should give us

At the end of the journey, we should be able to frame an AI exposure quickly and understand the main questions involved: what information is being used, who can access or disclose it, where it is going, how much judgement is being delegated and who owns the decision.

The objective is also to identify a few practical quick wins and, above all, a simple way to enter the subject without trying to solve everything at once.

This is not about saying **no** to AI or making people feel guilty for using tools that help them work better. The goal is to make AI use safer, clearer and easier to govern.

> **Take the right flight, know where you are going, and enjoy the journey.**

## The lab

Start with simple scenarios, test the questions and learn what works or fails.

**Understand first. Build only what is needed.**
