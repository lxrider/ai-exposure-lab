# Notes

This lab did not start from a framework.

It started from a question:

> **Is there a pilot in the plane?**

The problem is primarily human and organizational. Technology changes the scale, speed and capability of AI use, but people still need to understand why a rule exists, what business value it protects and how to achieve their goal safely.

The aim is not to blame users for adopting tools that help them work. It is to observe reality, explain the risk in understandable terms and make the safer path usable.

A few ideas shape the lab. They are influences, not requirements.

## CNIL / GDPR thinking

Useful principles include understanding purpose, minimizing what is necessary, considering impact, making responsibilities clear and reviewing decisions when context changes.

For this lab, one lesson is especially useful:

> **Do not expose more information than the task actually requires.**

This is not a GDPR project, and not every AI use case requires a DPIA.

## Agile thinking

AI tools, capabilities and habits change quickly. A static answer will have limits.

```text
UNDERSTAND
   ↓
TEST
   ↓
LEARN
   ↓
BUILD
   ↺
```

This is not about Scrum. It is about starting from reality, testing assumptions and changing the response when reality proves us wrong.

## RCCM

The Root Cause Countermeasure approach comes from industrial problem solving.

The useful principle here is simple:

> **Fix the cause, not the symptom.**

If employees use unapproved AI, blocking a website may address only the visible behavior. The root cause may be a legitimate business need with no usable approved alternative.

Understanding that difference changes the response.

## Attacker mindset

After understanding the business value and the use case, change perspective:

> **If I wanted to damage this value for my own benefit, what would I try to achieve?**

Then remove the attacker and ask what could simply fail or go wrong.

The result should be a clear security objective, not an endless list of theoretical threats.

## When AI can act

Giving AI access to a tool does not answer whether it is legitimate for AI to use that tool for every task.

Three things must remain distinct:

```text
USER / SERVICE PERMISSION
What the principal is allowed to do.

AGENT TECHNICAL CAPABILITY
What the agent can technically do.

DELEGATED TASK AUTHORITY
What the agent is legitimately allowed to exercise for the current task.
```

A principal's broad permission should not silently become an agent's authority.

Two working principles follow:

> **Ambiguity must not silently create authority.**

> **Model output may propose an action; it does not create authority to perform it.**

For this lab, these are practical security principles rather than a complete technical architecture. The lab asks whether the distinction is understood, bounded and testable. It does not prescribe OAuth, policy engines, MCP, capability systems or any other implementation.

The deeper technical questions are:

```text
DERIVATION
How did this task obtain this authority?

CONTINUITY
Is that authority still bounded and valid when the effect occurs?
```

Those questions are deliberately kept at the edge of this lab. They become a separate architecture problem when deeper implementation work is required.

## Sun Tzu

Some ideas from *The Art of War* also resonate with the approach.

**Know yourself.** Understand your business value, information, people, processes, exposure and existing controls.

**Know the environment.** Understand how AI is actually being used, not how the organization assumes it is being used.

**Adapt.** Trying to block every possible AI use may simply move the behavior somewhere less visible.

## What stays constant

Start with the problem, not the framework. Start with business value. Understand why people use AI. Minimize unnecessary exposure. Keep responsibility and authority explicit. Fix root causes. Prove countermeasures in reality. Learn and improve.

> **Build. Break. Understand. Rebuild better.**
