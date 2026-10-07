# Agentic Authority

This page adds one small checkpoint to the lab when AI can cause an effect.

It is not an IAM framework and does not prescribe a technology.

## Advice and action are different

When AI only advises:

```text
AI → recommendation → human → effect
```

The human remains the execution boundary.

When AI can act:

```text
AI → tool → effect
```

The security question changes. We must understand not only what the agent can technically do, but what it is legitimately allowed to do for the current task.

## Keep three concepts separate

```text
USER / SERVICE PERMISSION
What the principal is allowed to do.

        ≠

AGENT TECHNICAL CAPABILITY
What the agent can technically do through its tools and credentials.

        ≠

DELEGATED TASK AUTHORITY
What the agent is legitimately allowed to exercise for this task.
```

Example:

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
The SSH credential may technically allow much more.
```

The technical capability should not define the task authority.

## Two questions matter

### Derivation

How did the task obtain this authority?

The authority should be traceable to a legitimate source such as explicit human intent, an approved task rule or an explicit approval.

> **Ambiguity must not silently create authority.**

A model may propose what it thinks is needed. That proposal is not authority by itself.

### Continuity

Is the same authority still bounded and valid when the effect occurs?

Execution may cross agents, jobs, queues, workers or tools before the final effect.

```text
Human
  ↓
Task
  ↓
Agent
  ↓
Job
  ↓
Queue
  ↓
Worker
  ↓
Effect
```

The final action should still be inside the task authority, and that authority should still be valid when the effect occurs.

Expiry or revocation must matter even if the work was created earlier.

## Minimal model

```text
INTENT
  ↓
TASK AUTHORITY
  ↓
DELEGATION
  ↓
EXECUTION
  ↓
AUTHORITY CHECK
  ↓
EFFECT
  ↓
EVIDENCE
```

For the AI Exposure Lab, the practical questions are enough:

- Who delegated the authority?
- For which task or purpose?
- Which actions and resources are in scope?
- Does technical access exceed task authority?
- Can authority be reduced, expired or revoked?
- Is authority checked before a significant effect?
- Can the effect be traced back to the task and authority that allowed it?

The lab stops here. How those properties are implemented belongs to a deeper architecture and engineering problem.
