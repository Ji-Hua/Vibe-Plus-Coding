© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.1

# Chapter 2｜Mental Model

Before any process, template, or concrete practice can be discussed, a correct mental model must be established.
If the mental model is wrong, no matter how complete the steps or how refined the templates, the process will inevitably collapse back into old Vibe Coding:
a single conversation, chatting while coding, with design driven by implementation.

**The key to Vibe + Coding is not “how to use AI,”
but how you view yourself, and how you view AI.**

---

## 1. A Fundamental Shift: You Are No Longer a “User”

In old Vibe Coding, the engineering relationship is often implicit:

- You provide requirements
- You describe ideas
- You wait for AI to produce results

AI is implicitly treated as a black box that:

- Understands requirements
- Designs solutions
- Implements them
- And maybe debugs along the way

The essence of this relationship is:

> **Humans request, AI substitutes.**

In Vibe + Coding, this relationship must be completely dismantled.

You are no longer:

- A tool user
- A prompt engineer
- A person waiting for output

You play the role of:

**Staff Engineer / Tech Lead.**

This means:

- You are responsible for the entire system
- You are responsible for architectural quality
- You are responsible for long-term maintainability
- You hold final authority over all key design decisions

AI is no longer “the one who gets things done for you,”
but an **engineering resource you organize, constrain, and allocate**.

---

## 2. Not One AI, but Three Engineering Roles

Vibe + Coding is not about “using AI more cleverly.”
It compresses the division of labor of a real engineering team into a **personally controllable collaboration model**.

In this model, there are always three clearly defined roles.

---

### 2.1 You: The Sole System Owner

You are the owner of the entire system.

Your responsibility is not to write the most code, but to make the most important decisions:

- What problem the system actually solves
- Which problems it explicitly does not solve
- Where system boundaries lie
- Which abstractions are worth preserving long-term
- Which design conclusions must be frozen

You are responsible for:

- Design trade-offs
- Architectural judgment
- Responsibility ownership

Not for:

- Repetitive implementation
- Framework boilerplate
- Mechanical labor

Your core output is not code, but **decisions**.

---

### 2.2 The Vibe Agent: Design Collaborator

The Vibe Agent participates in only one thing:

**The thinking phase.**

Its role is to help you:

- Clarify unclear ideas
- Decompose complex problems
- Expose implicit assumptions
- Propose structured candidate solutions
- Externalize thinking into documentation

It is more like:

- A design discussion partner
- A thinking amplifier
- A highly intelligent rubber duck

The Vibe Agent’s value is not in “providing correct answers,”
but in:

> **Helping you turn unformed judgments in your mind into discussable, freezable structures.**

One point must be made absolutely clear:

- The Vibe Agent has no decision authority
- All design conclusions must be confirmed by you
- Everything it produces is a candidate, never a fact

---

### 2.3 The Coding Agent: A Constrained Executor

The Coding Agent has a very narrow role.

Its responsibility is only one thing:

> **Correctly executing according to documentation and tests.**

It may:

- Implement features based on documents
- Fix implementations based on tests
- Report execution results

It must not:

- Participate in architectural discussions
- Redesign interfaces
- Modify abstraction boundaries
- Introduce undocumented behavior

There is a critical discipline in Vibe + Coding:

> **The Coding Agent is not allowed to make decisions that “seem better.”**

If a behavior is not explicitly allowed by documentation, it must not occur.

Once the Coding Agent starts “self-optimizing,” the process has already failed.

---

## 3. Documentation: Frozen Consensus, Not Explanation Material

In Vibe + Coding, documentation is fundamentally redefined.

It is not:

- A tutorial
- A usage guide
- An external presentation artifact

It is:

**The frozen form of design consensus.**

You can think of the Vibe phase as an ongoing technical meeting:

- You and the Vibe Agent continuously discuss
- Continuously refine understanding
- Continuously narrow the design space

Documentation is the meeting minutes of that process.

Its purpose is to:

- Clearly record what has been decided
- Prevent later stages from repeatedly overturning design
- Provide the sole authoritative input to the Coding Agent
- Preserve decision context for your future self

Once documentation is frozen:

- The design phase temporarily ends
- The execution phase officially begins

In this paradigm, “change code first and see” does not exist.

---

## 4. Tests: The Executable Form of Design

In Vibe + Coding, tests are not merely a quality assurance tool.

Their true role is:

**The executable contract of the design document.**

Design documents describe semantic constraints:

- What should happen
- What must not happen

Tests translate these constraints into:

- Verifiable behavior
- Automatically checkable rules

Thus, in the hierarchy:

- Documents define semantics
- Tests define behavior
- Code merely implements behavior

The Coding Agent’s goal is not “to write code,” but:

> **To make the implementation satisfy the design constraints represented by tests.**

When tests conflict with implementation, the issue can only be:

- The design was not clearly written
- Or the implementation is wrong

Never that the test is “too strict.”

---

## 5. A Clear Engineering Responsibility Chain

Putting all roles together yields a clear responsibility chain:

You
↓
Design judgment
↓
Documentation
↓
Tests
↓
Code

The value of this chain is:

- When issues arise, you know where to trace responsibility
- Each layer has a clearly defined authority

Code always sits at the bottom.
It never owns semantic authority.

---

## 6. Failure Almost Always Starts with Role Confusion

Nearly all Vibe + Coding failures stem from the same root cause:

**Role boundaries are violated.**

Common symptoms include:

- Discussing design during the Coding phase
- Obsessing over implementation details during the Vibe phase
- Allowing the Coding Agent to modify APIs
- Masking design flaws with patch code

Once roles blur:

- Implementation hijacks design
- Documentation loses authority
- The system evolves uncontrollably

This mirrors failure modes in human engineering teams exactly.

---

## 7. Correct Psychological Expectations

In a healthy Vibe + Coding workflow, you should feel:

- The Vibe phase progresses slowly but with high focus
- The Coding phase progresses quickly and mechanically
- Cognitive load shifts forward
- Implementation cost drops significantly

This is normal.

If you feel that:

- Writing code is harder than designing
- Implementation repeatedly forces you to “patch design”

It usually means:

> The design phase was never truly completed.

---

## 8. Chapter Summary

In Vibe + Coding:

- You are the sole system owner
- The Vibe Agent is a design collaborator
- The Coding Agent is a constrained executor
- Documentation freezes consensus and preserves memory
- Tests are the behavioral contract of design

When these roles are clearly separated and respected,
AI can transform from an unstable generator into:

**A reliable, auditable, reusable engineering execution unit.**

Understanding this mental model is a prerequisite for the methodology and practice chapters that follow.
