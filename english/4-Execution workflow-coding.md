© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.1

# Chapter 4｜Execution Workflow – Coding

After completing design philosophy, mental model, and methodology, we now enter the **execution layer of Vibe + Coding**.

This chapter answers a single question:

> **In the Vibe + Coding paradigm, how does a task move from “design frozen” to “code reliably merged”?**

This chapter no longer discusses thinking.
It defines a **standard engineering closed loop** from frozen design to committed code.

---

## 1. From Design Freeze to Execution: A Necessary Engineering Transition

At the end of the Vibe phase, you typically have design artifacts such as:

- Architecture or module design documents
- Feature specifications
- API contracts
- Rules and invariants

But one fact must be recognized clearly:

**These are still “human-readable” design languages.**

Coding Agents cannot—and should not—fill in engineering details from vague semantics.

Therefore, before implementation, a crucial transition must occur:

> **Transform design conclusions into a strictly executable engineering task.**

This is not a formatting step, but the establishment of an engineering safety boundary.

---

## 2. What Counts as an “Executable Task”

A task that can be handed to a Coding Agent must satisfy:

- Clear boundaries
- Explicit behavior scope
- Enumerated inputs and outputs
- Determinable completion criteria

In other words:

> **If you cannot clearly decide whether the task is complete,
> it is not yet an engineering task.**

In Vibe + Coding, task descriptions are not “please implement this feature,”
but **engineering tickets**.

The Coding Agent executes tickets.
It does not infer intent or background.

A simple self-check is whether you, as the task owner, could implement your own design strictly from the description without deviating from intent.

---

## 3. Mandatory Decomposition from Design to Tasks

Design documents usually cover:

- A module
- A subsystem
- Or a milestone

But a Coding Agent can only safely handle:

> **One atomic task at a time.**

Therefore, you must explicitly:

- Decompose design documents into atomic tasks
- Ensure each task is independently implementable, testable, auditable
- Minimize implicit dependencies between tasks

A healthy task has:

- A clear goal
- An authoritative design source
- Explicit constraints and invariants
- Clear completion standards

If this step is insufficient, all downstream problems will surface during implementation.

---

## 4. Test First: The True Start of Execution

In Vibe + Coding, the Coding phase **does not start by writing implementation**.

It must start with:

> **Tests.**

The reason is simple:

- Documents define semantics
- Tests define behavior
- Code implements behavior

In a healthy execution flow, the Coding Agent’s first steps are:

- Write tests
- Run tests
- Observe failures

This is a positive signal—it means tests are actually constraining behavior.

If tests pass immediately, they likely do not express real design constraints.

---

## 5. The Constrained Execution Loop of the Coding Agent

The Coding Agent must operate strictly within the following loop:

1. Read the task description
2. Write or extend tests
3. Run tests (fail)
4. Write minimal implementation
5. Run tests again
6. Fix implementation
7. Repeat until all tests pass

The Coding Agent **must not**:

- Modify design documents
- Expand task scope
- Introduce undocumented behavior
- Refactor structure “for aesthetics”

Its sole objective is:

> **Make the implementation satisfy the tests that represent design constraints.**

---

## 6. Implementation Report: Required Execution Trace

After task completion, the process is not finished.

The Coding Agent must produce an **implementation report** answering at least:

- What functionality was implemented
- Which implementations correspond to which design constraints
- Any assumptions or ambiguities encountered
- Any items requiring human confirmation

This report is not a summary, but:

> **An auditable execution record.**

Code without an implementation report should not be merged.

---

## 7. Review Loop: Reconciling Design and Implementation

After completion, you must bring the following back to the Vibe phase:

- Implementation code
- Tests
- Implementation report

Review focuses on:

- Does the implementation strictly follow documentation?
- Are there ambiguities in documentation?
- Did undocumented behavior appear?

Issues must be classified as:

- **Design issues** → modify documentation and re-freeze
- **Implementation issues** → fix tests or code

A key principle:

> **Never patch code to hide design problems.**

---

## 8. Commit and Stage Confirmation

Once a task passes review:

- Perform local code review
- Run unit and integration tests
- Commit to version control

Recommended practice:

> **One frozen document version corresponds to one commit.**

This ensures:

- Design decisions are traceable
- Issues can be mapped to design context

Code history gains engineering meaning.

---

## 9. Integration Awareness

In real systems, serious issues often arise not within modules, but between them.

Therefore, after multiple tasks:

- Run integration tests
- Verify minimal end-to-end paths
- Check upstream/downstream interactions

**Do not wait until all modules are done to integrate.**

This is one of the most expensive mistakes in practice.

---

## 10. The Correct Approach to Refactoring

Refactoring is inevitable in long-term projects, but in Vibe + Coding it must follow the paradigm:

- Update documentation first
- Adjust tests
- Then implement changes

**Silent refactoring is not allowed.**

Any structural change without corresponding design documentation breaks auditability.

---

## 11. Chapter Summary

This chapter defines a complete, executable engineering loop:

Freeze documentation (Vibe Agent)
→ Atomic task (Vibe Agent)
→ Test design (Vibe Agent)
→ Test implementation (Coding Agent)
→ Code writing (Coding Agent)
→ Implementation report (Coding Agent)
→ Review loop (Vibe Agent)
→ Commit confirmation (Human)

Through this loop:

- Execution is strictly constrained
- Design retains interpretive authority
- AI is confined to safe engineering roles
