© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.1

# Chapter 3｜Methodology – Vibe

After establishing design philosophy and mental model, we can finally address a practical question:

**How does Vibe + Coding actually operate?**

This chapter does not cover specific tools, platforms, or prompt-writing techniques.
Those belong to the implementation layer, not methodology.

Instead, this chapter presents a **stable, repeatable, extensible engineering framework**
that answers a more fundamental question:

> **How to turn a vague, complex, long-term engineering problem
> into a sequence of tasks that AI can execute safely and controllably**
In other words, how to **Vibe**.

---

## 1. Why a Methodology Is Necessary

In old Vibe Coding, engineering often advances through continuous conversation:

- Ideas unfold in chat
- Decisions remain implicit in context
- Changes happen through “just saying one more thing”

This feels natural at small scale, but breaks down quickly at engineering scale:

- Decisions are invisible
- Consensus cannot be frozen
- State cannot be restored
- Progress depends on unreliable conversational memory

Vibe + Coding aims to shift engineering from:

**Continuous conversation → Discrete decision structure**

Only when problems are decomposed, structured, and explicitly recorded
can AI execute reliably and engineering remain controllable.

---

## 2. The Four-Stage Model Overview

In the Vibe phase, Vibe + Coding uses a fixed four-stage model to organize all design activities:

**Input → Alignment → Refinement → Freeze**

These four stages form the complete **Vibe lifecycle**.

Important notes:

- They are not strictly linear
- They can loop
- They can recurse
- They can nest

The same model applies to project-level architecture
and to individual feature-level design convergence.

---

## 3. Input: Provide a Starting Point, Not a Solution

The goal of the Input stage is simple:

> **Provide a starting point for thinking.**

You do not need a full solution.
You do not consider implementation details.

Input can be:

- A vague idea
- A goal description
- A problem statement

For example:

- “I want to build a chess program supporting local two-player and AI play.”
- “I want to design a framework to evaluate LLM output quality.”

At this stage:

- Completeness is not required
- Correctness is not required
- Technical choices are deferred

You are only stating one thing:

**This is the problem we are about to seriously discuss.**

---

## 4. Alignment: Align Understanding, Not Design

Alignment is the **most critical and most frequently skipped step** in the Vibe phase.

Many Vibe Coding failures stem not from poor design ability, but from failing to align on:

**What problem is actually being discussed.**

The sole goal of alignment is:

> **Ensure you and the Vibe Agent share the same understanding of the problem itself.**

Typical alignment activities include:

- Asking the Vibe Agent to restate the problem
- Exposing ambiguity and unclear areas
- Clarifying scope, goals, and non-goals

Typical alignment questions:

- Is this a local program or a server system?
- Is it for end users or internal use?
- Does it require long-term extensibility?
- Are there performance or stability constraints?

The output of alignment is not a solution, but:

**A mutually agreed-upon problem definition.**

No design should begin before alignment is complete.

---

## 5. Refinement: Turn the Problem into Structure

The goal of refinement is to gradually construct a **discussable, modifiable, implementable system structure** on top of an aligned problem definition.

This stage typically includes:

- Module decomposition
- Responsibility boundary definition
- Technical path discussion
- Preliminary data and interface structures

During refinement, you may:

- Ask the Vibe Agent to propose multiple design options
- Compare trade-offs
- Narrow the design space

Important constraints:

- No code is written
- Everything remains design-level thinking

You are not building implementation, but:

> **A system model that humans can understand, discuss, and take responsibility for.**

---

## 6. Freeze: Freeze Decisions and Form Engineering Consensus

Freeze is the **most important and most often neglected step** in Vibe + Coding.

Here, you must explicitly do one thing:

> **Fix the design conclusions confirmed so far.**

Freeze can take the form of:

- A design document
- A task specification
- An architecture description
- A module boundary definition

The format does not matter. The semantics do:

- What has been decided
- What is no longer under discussion
- What execution must strictly follow

Once frozen:

- Design becomes read-only
- Execution receives stable input

Any new idea must:

- Explicitly break the freeze
- Modify documentation
- Enter a new iteration

“There is no ‘change code first and see.’”

---

## 7. Fractal Recursion: Same Model, Different Scales

The four stages are not limited to top-level design.

They naturally exhibit **fractal recursion**.

You can apply them to:

- The entire project
- A single module
- A subsystem
- A concrete feature

Repeating:

**Input → Alignment → Refinement → Freeze**

Until you converge to a scale:

> **That a Coding Agent can independently execute as an atomic task.**

At that point, the task should have:

- A clear goal
- Clear inputs and outputs
- Clear constraints
- Clear completion criteria

This marks the end of the Vibe phase and the start of Coding.

---

## 8. Depth-First, Not Breadth-First

In practice, strongly prefer:

**Depth-first (DFS) over breadth-first (BFS)** progression.

That is:

- Fully design one module to execution-ready state
- Complete its implementation and validation
- Only then move to the next module

The reasons are practical:

- AI struggles to maintain multiple unfrozen designs
- More half-finished modules mean more semantic pollution
- Unfrozen designs easily interfere with one another

DFS maximizes design stability.

---

## 9. Chapter Summary

The four-stage model:

**Input → Alignment → Refinement → Freeze**

forms the methodological core of Vibe + Coding.

Its goal is not speed, but to make engineering:

- Controllable
- Traceable
- Executable

Once you can fluently move between these stages
and know when to advance and when to freeze,
you possess the ability to decompose complex engineering problems
into tasks that AI can safely execute.
