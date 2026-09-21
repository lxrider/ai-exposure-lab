# AI Exposure Lab

> **Is there a pilot in the plane? ✈️**

Generative AI is already used at work.

Employees use ChatGPT, Claude, Gemini and other AI services with emails, documents, source code, customer information or internal data.

Sometimes nobody has clearly decided whether that information should be sent there.

That creates a simple governance problem:

> **Who can use what information, with which AI, when, why, and under which conditions?**

And another question follows:

> **How much human judgement are we willing to delegate to AI?**

## The problem

A developer may legitimately have access to source code.

That answers:

> **Who can access it?**

It does not answer:

> **Can they send it to an external AI service?**

So:

> **Access right ≠ Disclosure authority**

The same applies to customer emails, financial information, architecture, credentials or confidential documents.

To understand an AI use case, start with a few simple questions:

```text
WHO?
Who is using the information?

WHAT?
What information is involved?

WHY?
Why is AI needed?

WHEN?
In which business context?

WHERE?
Which AI service receives it?

HOW?
Corporate device?
Personal account?
Smartphone over 5G?

HOW MUCH?
How much information is really necessary?

WHO DECIDES?
Who can authorize this use?
```

The goal is not to create a huge framework.

It is to understand the situation well enough to make a sensible decision.

## Another question: what are we delegating?

Information exposure is only one side of the problem.

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

The further we go, the more human judgement may be involved.

So we also need to ask:

> **What are we asking the AI to do, and who remains responsible for the result?**

## A simple way in

For now, keep the model simple:

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

Possible answers:

```text
ALLOWED
ALLOWED WITH CONDITIONS
NOT ALLOWED
UNKNOWN
```

`UNKNOWN` is not a failure.

It means we found something that needs a decision.

## What this lab should give us

At the end of the journey, we should be able to:

* frame an AI exposure quickly;
* understand what information is involved;
* identify who can access and disclose it;
* understand where the information is going;
* identify how much judgement is being delegated;
* spot a few obvious quick wins;
* know where to start without trying to solve everything at once.

This is not about saying **no** to AI.

It is not about making people feel guilty for using tools that help them work better.

The goal is to make AI use safer, clearer and easier to govern.

> **Take the right flight, know where you are going, and enjoy the journey.**

## The lab

Start with simple scenarios.

Test the questions.

Learn what works, what fails, and what needs to be built.

Understand first. Build only what is needed.
