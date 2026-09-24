# Use Cases

These use cases exist to test the method against reality. They are starting points, not universal answers.

For each case, start with the business need, run `quick-review.md`, challenge the use, apply RCCM and prove the countermeasure before turning it into a playbook.

## 1. HR / Talent Acquisition — AI-assisted candidate screening

A Talent Acquisition team wants to reduce the time spent reviewing applications and preparing shortlists.

A tempting shortcut is to copy CVs into a personal general-purpose AI account.

```text
BUSINESS VALUE
Recruit faster without degrading hiring quality or candidate trust.

CHANNEL
Personal AI account or approved HR environment.

EXPOSURE
CVs, contact details, employment history and other candidate information.

COGNITIVE DELEGATION
Summarize → Compare → Rank.

ACTION DELEGATION
Potentially update the ATS, schedule an interview or influence rejection.
```

Questions to test:

- Why does the recruiter need AI here?
- Is all candidate information necessary for the task?
- Is AI only summarizing, or also scoring and ranking people?
- Who validates the result and owns the hiring decision?
- Can the use stay inside the approved recruitment process?

### Countermeasure hypothesis

If the organization already has an approved ATS, the safer path may be to keep candidate processing inside that environment and use an **approved AI capability or approved integration**, rather than moving candidate data to a personal general-purpose AI account.

This addresses the channel and exposure problem without denying the business need.

It does **not** automatically answer every delegation, HR or Legal/Privacy question.

> **Approved tool ≠ approved use case.**

## 2. Sales — preparing a customer meeting

A salesperson copies a customer email and internal notes into a personal AI account to prepare a meeting faster.

```text
BUSINESS VALUE
Prepare faster and improve the customer interaction.

CHANNEL
Personal / unapproved AI account.

EXPOSURE
Customer context, internal comments, possible pricing or commercial information.

COGNITIVE DELEGATION
Summarize → Analyze → Suggest talking points.

ACTION DELEGATION
None initially.
```

The visible behavior is not necessarily the root cause. The salesperson may simply have a legitimate need with no usable approved alternative.

The review should ask why this channel is being used and whether a safe path can deliver the same result with less exposure.

## 3. SysAdmin — troubleshooting production

A system administrator encounters an error on a server and asks AI to diagnose it. They paste logs, configuration excerpts, hostnames, IP addresses and commands already executed, then ask:

> "Give me the commands to fix this."

```text
BUSINESS VALUE
Restore service quickly and correctly.

EXPOSURE
Logs, architecture, configuration and possibly secrets.

COGNITIVE DELEGATION
Analyze → Diagnose → Reason → Recommend.

ACTION DELEGATION
Human copy/paste into production.
```

Questions to test:

- What information is really required for diagnosis?
- Could credentials, tokens or sensitive architecture leak through the logs?
- Is the administrator reviewing the proposed command or merely executing it?
- What happens if the recommendation is wrong?

With an AI agent, the same use case can evolve into:

```text
SSH → Execute → Modify → Restart
```

That changes the problem from advice to direct action.

## 4. Developer — AI-assisted coding

A developer asks AI to understand a bug, generate a fix and improve tests.

```text
BUSINESS VALUE
Develop and fix software faster.

EXPOSURE
Source code, architecture, business logic and possibly embedded secrets.

COGNITIVE DELEGATION
Understand → Analyze → Generate → Review.

ACTION DELEGATION
With an agent: modify files → run tests → commit → open a pull request.
```

Questions to test:

- Which parts of the codebase can be exposed?
- Are secrets or proprietary business rules included?
- Who reviews generated code?
- What permissions does a coding agent really need?
- Can it modify repositories, CI/CD or production-related configuration?

## 5. Supplier / Third Party — our data in someone else's AI

A supplier receives company information to deliver a service. During support, analysis or content production, the supplier uses its own AI service.

```text
BUSINESS VALUE
Receive an external service efficiently.

CHANNEL
Outside our direct environment.

EXPOSURE
Our data, logs, documents, customer information or business context.

COGNITIVE DELEGATION
Potentially known only partially.

ACTION DELEGATION
Potentially known only partially.

CONTROL
Often contractual and assurance-based rather than directly technical.
```

Questions to test:

- What value does the supplier touch?
- What information may it expose to AI?
- Which AI providers or sub-processors are involved?
- What cognitive work is delegated?
- Can AI act on our systems or data?
- What do we require contractually?
- How do we obtain evidence rather than relying only on declarations?

This use case links AI governance with third-party and supply-chain risk.
