# Playbooks

A playbook is a short, practical answer learned from a real AI use case.

Do not write it before the problem has been understood, the root cause identified and the countermeasure tested.

A useful playbook should be short enough for the people doing the work to actually use it.

## Playbook template

```text
USE CASE
What are people trying to do?

BUSINESS VALUE
Why does it matter?

RISK
Why can this use hurt the value?

SAFE PATH
How can the team achieve the same result more safely?

RULES
What must / must not happen?

AUTHORITY — if AI can act
What may AI legitimately do for this task,
and what remains outside its authority?

HUMAN ROLE
Who validates, decides or remains accountable?

PROOF
How do we know the playbook works?
```

## First example — AI-assisted candidate review

**Use case**

A recruiter wants AI assistance to review candidate information more quickly.

**Business value**

Reduce screening time while preserving recruitment quality, candidate trust and appropriate handling of candidate information.

**Risk**

Candidate information may contain personal data.

Using a personal or unapproved AI service may result in unauthorized disclosure or transfer of personal data outside the approved recruitment process.

AI may also move from summarization into comparison or ranking without clear human ownership of the hiring decision.

If AI is later allowed to update the ATS, schedule interviews or trigger workflow decisions, the use also becomes an authority problem: the recruiter's access must not silently become broad agent authority.

**Safe path**

Keep candidate processing inside the organization's approved recruitment environment.

If the organization already has an approved ATS, the safer path may be to use an approved AI capability or integration within that environment rather than moving candidate data to a personal general-purpose AI account.

This addresses the channel and exposure problem without denying the business need.

It does not automatically answer every delegation, authority, HR or Legal/Privacy question.

> **Approved tool ≠ approved use case.**

**Rules**

- expose only the candidate information required for the task;
- do not move candidate personal data outside the approved recruitment environment without authorized conditions;
- distinguish summarization from comparison, scoring or ranking;
- keep the hiring decision human-owned and reviewable;
- use only AI capabilities or integrations approved for the use case;
- if AI can cause an effect, do not infer broad agent authority from the recruiter's access rights.

**Authority — if AI can act**

For the assistance-only path, no direct action authority is required.

If AI can update the ATS or trigger a workflow, define the permitted action, candidate or resource, duration and approval conditions for that task. Anything outside that scope remains out of authority.

**Human role**

The recruiter remains responsible for reviewing the result and the hiring process.

HR, Legal/Privacy and Security review the conditions when AI use goes beyond simple assistance.

**Proof**

- Can the recruiter achieve the time-saving objective through the approved path?
- Can candidate data still be copied to an unapproved AI service?
- Does the approved solution expose only what is necessary?
- Is AI-generated comparison or ranking visible and reviewable?
- If AI can act, is an action outside its delegated task authority blocked?
- If AI can act, can a significant effect be traced back to the task and authority that allowed it?
- Is the approved path simple enough that people will actually use it?

## From playbooks to policy

When the same validated rule appears across several playbooks, it becomes a candidate for organizational policy.

Do not promote a rule because it sounds good.

Promote it because multiple real use cases show that it is necessary, understandable and workable.
