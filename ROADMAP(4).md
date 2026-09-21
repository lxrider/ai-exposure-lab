# Roadmap

This roadmap intentionally starts small.

The goal is not to design a complete AI governance program.

The goal is to understand one narrow security problem by building and testing a simple decision model.

## Phase 0 — Blank page

**Goal:** understand the problem before designing controls.

Done:

- identify the professional-use scenario;
- distinguish personal AI use from professional information exposure;
- identify `Access right ≠ Disclosure authority`;
- identify information sensitivity and disclosure impact;
- recognize the AI service as a recipient;
- challenge the simple controlled/uncontrolled network model;
- define the first MVP boundary.

Output:

- `README.md`
- `docs/problem-v1.md`

## Phase 1 — First real scenarios

**Goal:** test the reasoning against a few concrete situations.

Create 4–6 simple scenarios.

Suggested starting set:

1. Public information → approved AI service.
2. Internal email → personal AI account.
3. Small proprietary code fragment → approved AI service.
4. Source code containing a credential → external AI service.
5. Customer information → personal AI account.
6. Professional information → personal smartphone over 5G.

For each scenario, answer:

```text
What information?
Who has access?
Who may disclose?
Why is AI needed?
Which AI / account?
How much information is necessary?
Who decides?
```

Then classify the result:

```text
ALLOWED
ALLOWED WITH CONDITIONS
NOT ALLOWED
UNKNOWN / NEEDS DECISION
```

Deliverable:

- `docs/scenarios-v1.md`

## Phase 2 — Challenge the decision model

**Goal:** find where the simple model fails.

Questions to test:

- Does the same information produce a different decision with a different AI destination?
- Does account type matter more than network path?
- Can a low-sensitivity fragment become sensitive through aggregation?
- What happens when the organization has no clear disclosure authority?
- Where does user friction appear?
- Which decisions are obvious and which require escalation?

Deliverable:

- `docs/findings-v1.md`

Do not add new framework layers unless the scenarios show a real need.

## Phase 3 — Define the minimum governance response

**Goal:** translate what was learned into a small operating model.

Only after the scenarios are tested, define:

- who can make routine decisions;
- who can approve exceptions;
- which decisions can be standardized;
- which uses require escalation;
- what must be logged as evidence;
- what users need to understand.

Possible deliverable:

- `docs/minimum-governance-v1.md`

## Phase 4 — First technical experiment

**Goal:** test one technical control against one clearly defined governance decision.

Do not start with a product list.

First choose one decision that is already understood.

Example:

> Customer PII must not be sent to an unapproved consumer AI account.

Then ask:

- where could this be observed?
- what could be detected?
- what could be prevented?
- what can still bypass the control?
- what false positives or friction appear?

Only here should technical mechanisms such as browser controls, DLP, proxying, CASB/SSE, or AI gateways be evaluated.

## Phase 5 — Review and expand only if justified

Possible later topics:

- embedded AI in SaaS;
- IDE assistants;
- provider retention and contractual controls;
- output validation;
- prompt injection;
- RAG;
- MCP;
- agents;
- incident response;
- metrics and governance maturity.

These topics are not roadmap commitments.

They are candidates that should be added only if the earlier phases show they are necessary.

## Working principles

### Start from reality

Do not assume how users behave.

Test real or realistic scenarios.

### Keep security understandable

If a rule cannot be explained simply, challenge the rule.

### Prefer impact over labels

Classification helps, but the consequence of disclosure matters more.

### Access is not disclosure

The right to use information internally does not automatically include the right to send it to an external AI service.

### Minimize exposure

Expose only what is necessary for the task.

### Make the safe path usable

A control that users cannot realistically follow will encourage workarounds.

### Build only after the problem is understood

No technology should be introduced simply because it is commonly associated with AI security.
