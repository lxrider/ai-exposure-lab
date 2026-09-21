# Roadmap

This roadmap explains how the lab will progress from a simple question to practical experiments.

The objective is not to give the reader a ready-made AI governance framework.

The objective is to show, step by step, how the problem is understood, tested, challenged, and eventually translated into useful controls.

At each stage, the reader should be able to follow the reasoning and understand why the next step exists.

---

## Phase 0 — Define the problem

### What we are trying to understand

The starting question is:

> **Can this person provide this information to this AI service for this purpose?**

Before discussing tools or controls, the lab defines the basic concepts needed to answer that question:

* information sensitivity;
* access rights;
* disclosure authority;
* AI destination;
* business purpose;
* level of organizational control.

### What we produce

* `README.md`
* `docs/problem-v1.md`

### What the reader should understand

By the end of this phase, the reader should understand:

* why AI use is also an information-disclosure problem;
* why access does not automatically mean disclosure;
* why the destination matters;
* why the network alone does not define whether an AI use is acceptable.

---

## Phase 1 — Test the model with real scenarios

### What we are trying to learn

A model is only useful if it works on realistic situations.

The lab will test it against simple cases such as:

* public information sent to an approved AI;
* an internal email sent to a personal AI account;
* proprietary code sent to an approved AI;
* code containing credentials sent to an external AI;
* customer information sent to a personal AI;
* company information sent from a personal phone over 5G.

For each case, we will ask:

```text
What information?
Who can access it?
Who may disclose it?
Why is AI needed?
Which AI receives it?
How much is necessary?
Who decides?
```

Then we will try to reach one of four decisions:

```text
ALLOWED
ALLOWED WITH CONDITIONS
NOT ALLOWED
UNKNOWN
```

### What we produce

* `docs/scenarios-v1.md`

### What the reader should understand

By the end of this phase, the reader should be able to see how the same decision model behaves across different real-world situations.

The goal is not to prove the model is correct.

The goal is to find where it works and where it starts to fail.

---

## Phase 2 — Challenge what does not work

### What we are trying to learn

The scenarios should reveal weaknesses in the first model.

We will look for situations where:

* the answer is unclear;
* the AI destination changes the decision;
* the account matters more than the network;
* several low-sensitivity fragments become sensitive together;
* nobody knows who can authorize the disclosure;
* the safe path creates too much friction.

### What we produce

* `docs/findings-v1.md`

### What the reader should understand

By the end of this phase, the reader should understand:

* which assumptions were wrong;
* which questions were useful;
* which questions were missing;
* where the model needs to change.

If the model breaks, that is useful.

This is a lab.

---

## Phase 3 — Define the minimum useful response

### What we are trying to learn

Only after the problem has been tested do we ask:

> **What is the minimum the organization needs to do?**

This may include:

* simple disclosure rules;
* clear decision ownership;
* an exception path;
* a usable approved AI option;
* basic evidence of decisions.

### What we produce

Possible deliverable:

* `docs/minimum-governance-v1.md`

### What the reader should understand

By the end of this phase, the reader should understand what minimum governance is actually needed to support safe AI use without turning the response into a large compliance program.

---

## Phase 4 — Test one technical control

### What we are trying to learn

Only now do we introduce technology.

The lab will take one rule that is already understood and test whether a technical control can actually support it.

Example:

> Customer PII must not be sent to an unapproved consumer AI service.

Then we ask:

* can the control see it?
* can it detect it?
* can it stop it?
* what can bypass it?
* what friction does it create?

### What we produce

A first technical experiment.

### What the reader should understand

By the end of this phase, the reader should be able to distinguish:

> **What governance decides**

from:

> **What technology can actually enforce**

---

## Later

Only if the lab naturally reaches them:

* DLP;
* proxies;
* AI gateways;
* SaaS AI;
* IDE assistants;
* provider retention;
* prompt injection;
* RAG;
* MCP;
* agents;
* incident response.

These are not part of the initial plan.

They are future questions.

---

## How to read this project

This repository is meant to be followed as an experiment.

The reader is not expected to accept the model as a finished answer.

The reader should be able to:

1. follow the reasoning;
2. challenge the assumptions;
3. reproduce the scenarios;
4. compare the decisions with their own environment;
5. see how the model evolves when reality contradicts it.

The project should remain simple enough that every step can be explained and tested.
