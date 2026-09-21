# Roadmap

The project starts from a simple idea:

> **Understand the problem before building the solution.**

No framework first.
No product first.
No technical control first.

---

## Phase 0 — Understand the problem

Define the first problem clearly.

Current focus:

> **Can this person provide this information to this AI service for this purpose?**

Main ideas:

* information sensitivity matters;
* access does not mean disclosure;
* the AI service is a recipient;
* the network is only part of the problem;
* Shadow AI may be a symptom of unclear or unusable rules.

Deliverables:

* `README.md`
* `docs/problem-v1.md`

---

## Phase 1 — Test real scenarios

Take a few simple situations and apply the model.

Examples:

* public information → approved AI;
* internal email → personal AI account;
* proprietary code → approved AI;
* code containing credentials → external AI;
* customer information → personal AI;
* company information → personal phone over 5G.

For each scenario, ask:

```text
What information?
Who can access it?
Who may disclose it?
Why is AI needed?
Which AI receives it?
How much is necessary?
Who decides?
```

Then decide:

```text
ALLOWED
ALLOWED WITH CONDITIONS
NOT ALLOWED
UNKNOWN
```

Deliverable:

* `docs/scenarios-v1.md`

---

## Phase 2 — Learn from what breaks

Challenge the model.

Look for cases where:

* the answer is unclear;
* the destination changes the decision;
* the account matters more than the network;
* small pieces of information become sensitive together;
* nobody knows who can approve the disclosure;
* the safe path creates too much friction.

Do not add complexity unless the scenarios show a real need.

Deliverable:

* `docs/findings-v1.md`

---

## Phase 3 — Build only what is needed

Only after the problem has been tested:

* define the minimum governance rules;
* identify who decides;
* define simple exceptions;
* choose one technical control to test;
* measure what it can and cannot actually solve.

Possible later deliverables:

* `docs/minimum-governance-v1.md`
* first technical experiment

---

## Later, maybe

Only if the lab naturally reaches these topics:

* DLP / proxy / AI gateway;
* provider retention and contractual controls;
* embedded AI in SaaS;
* IDE assistants;
* prompt injection;
* RAG;
* MCP;
* agents;
* incident response.

These are not commitments.

They are future questions.

---

## Working principles

> **Start small.**

> **Test assumptions.**

> **Keep security understandable.**

> **Expose only what is necessary.**

> **Make the safe path usable.**

> **Build only after the problem is understood.**
