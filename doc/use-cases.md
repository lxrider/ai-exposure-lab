# Use Cases

These use cases exist to test the method against reality. They are starting points, not universal answers.

For each case, start with the business need, run `quick-review.md`, challenge the use, apply RCCM and prove the countermeasure before turning it into a playbook.

When AI can directly cause an effect, also run the agentic authority checkpoint. A principal's access does not automatically become an agent's task authority.

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
- If AI can update the ATS or trigger workflow decisions, what authority was actually delegated for this candidate and this task?
- Can AI turn a recommendation into a business action without a new human decision?

### Countermeasure hypothesis

If the organization already has an approved ATS, the safer path may be to keep candidate processing inside that environment and use an **approved AI capability or approved integration**, rather than moving candidate data to a personal general-purpose AI account.

This addresses the channel and exposure problem without denying the business need.

It does **not** automatically answer every delegation, authority, HR or Legal/Privacy question.

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

If the use later evolves into an agent that updates the CRM, sends customer emails, changes an opportunity or triggers a workflow, run the agentic authority checkpoint again. The risk has changed from assistance to action.

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

The administrator may have root access. That does not mean an agent acting for the administrator should inherit root-equivalent authority.

```text
USER PERMISSION
Administrator can manage the server.

TASK AUTHORITY
Investigate nginx failure.
Read relevant logs.
Restart nginx if required.
On server-12.
For incident-42.

AGENT TECHNICAL CAPABILITY
Its SSH credential may technically allow much more.
```

> **User permission ≠ task authority ≠ agent technical capability.**

Questions to test:

- Does the agent have more technical access than the task requires?
- Can it execute outside the affected host, service or incident scope?
- Can its authority be revoked while the task is still running?
- Is the final production effect traceable to the task and delegated authority?

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

For an action-taking coding agent, separate developer permissions from task authority:

```text
DEVELOPER PERMISSION
Developer can modify the repository.

TASK AUTHORITY
Fix issue #412.
Work on branch fix/412.
Modify application code and tests.
Open a pull request.

AGENT TECHNICAL CAPABILITY
The repository token may technically permit changes to other branches,
CI configuration or repository settings.
```

Questions to test:

- Does the agent's technical access exceed what this task requires?
- Can it cross repository, branch or CI/CD boundaries that are not part of the task?
- Does authority expand automatically when the agent decides it needs more access?
- Can the resulting changes be traced back to the task and approval path?

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
- If it can act, what authority has actually been delegated to the supplier's AI?
- How is that authority bounded, expired or revoked?
- What do we require contractually?
- How do we obtain evidence rather than relying only on declarations?

This use case links AI governance with third-party and supply-chain risk.
