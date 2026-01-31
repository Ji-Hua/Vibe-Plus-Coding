© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.1

# Chapter 6｜Common Errors and Engineering Trade-offs

Vibe + Coding is not a process that guarantees success if followed mechanically.
It is a paradigm that **heavily depends on engineering discipline**.

Once key constraints are violated, the process rarely collapses immediately.
Instead, it degrades subtly and gradually, eventually reverting to old Vibe Coding.

This chapter aims not to list “bad habits,”
but to help you recognize **signals that you are misusing the paradigm or should not be using it at all**,
and to correct course before engineering truly goes out of control.

---

## 1. The Most Dangerous Anti-Pattern: Role Mixing

This is the **most common and most fatal** source of failure.

### Symptoms

- Discussing architecture during Coding
- Letting the Coding Agent “optimize structure”
- Writing code before design is frozen
- Injecting implementation details during Vibe

### Consequences

- Implementation hijacks design
- Documentation loses authority
- Decisions become buried in code
- The system becomes unauditable

### Engineering Meaning

Once role boundaries are broken,
Vibe + Coding no longer exists.

### Correction

- Immediately stop execution
- Return to documentation
- Clarify whether you are in Vibe or Coding
- Restore role and context isolation

---

## 2. Patching Code to Hide Design Problems

This is the second most common and more insidious degradation path.

### Symptoms

- “This is weird; let’s patch it for now”
- “Let it run first; we’ll fix the doc later”
- “The doc isn’t clear, but this code works”

### Root Problem

**Design flaws are converted into implementation complexity.**

Short-term efficiency masks long-term damage:

- Design becomes hollow
- Code becomes heavy
- Eventually, no one dares to touch the system

### Principle

All unexpected behavior must be resolved at the documentation layer.

**Code does not explain design.**
Only documentation owns semantic authority.

---

## 3. Documentation Drift: Saying One Thing, Doing Another

### Symptoms

- Documentation stops being updated
- Implementation clearly exceeds documented scope
- Tests validate “actual behavior” rather than design behavior

### Danger Signals

- New contributors must read code to understand the system
- Documentation becomes historical residue

This means:

> The system has degraded into implicit knowledge.

### Correction

- Pause new development
- Systematically reconcile docs and implementation
- Decide which behaviors are truth and which are obsolete

---

## 4. Overtrusting AI “Intelligence”

This is a psychological anti-pattern.

### Symptoms

- “It should understand what I mean”
- “This doesn’t need documentation”
- “The model is strong; it won’t get this wrong”

### Reality

- Implicit assumptions accumulate
- Small deviations amplify
- Errors become irreproducible and inexplicable

The core premise of Vibe + Coding is:

> **AI is only reliable within constraints.**

Any “intelligence” outside documents and tests is engineering risk, not advantage.

---

## 5. Over-Formalizing Documentation

Anti-patterns are not only about too little, but also too much.

### Symptoms

- Documentation aims for perfect specification
- Attempts to define everything upfront
- Writing docs costs as much as writing code

### Consequences

- Design rigidity
- Drastic slowdown in iteration
- Loss of exploratory space

### Principle

Documentation should be:

> **Clear enough to execute, but not so rigid that it freezes the future.**

Documentation freezes stage consensus, not ultimate truth.

---

## 6. Forcing Exploratory Problems into the Paradigm

A very common misuse scenario.

### Symptoms

- Unproven algorithms
- Unvalidated technical paths
- High-uncertainty exploratory work

Yet attempting to:

- Write full design documents
- Define strict tests
- Freeze implementation paths

### Outcome

- Many useless documents
- Frequent design reversals
- Heavy psychological burden

### Engineering Judgment

When the core question is still:

“Can this be done?”

Rather than:

“How should this be done well?”

Using Vibe + Coding is itself a mistake.

---

## 7. Misapplying the Paradigm to Inappropriate Scenarios

Forcing Vibe + Coding into these scenarios almost guarantees degradation:

- One-off scripts
- Strong UI/UX-driven frontend work
- Highly trial-and-error tuning tasks
- Legacy systems with heavy historical debt

In these cases:

- Documentation cost ≈ implementation cost
- Design freezing lacks realism

**Paradigm failure does not imply method failure, but scenario mismatch.**

---

## 8. Ignoring Integration Risk

### Symptoms

- All module tests pass
- System fails as a whole
- Module interfaces do not compose

### Cause

Design over-focuses on internal modules, ignoring inter-module composition.

### Correct Practice

- Write integration tests for boundaries
- Run minimal viable paths early
- Do not wait until everything is complete to integrate

---

## 9. Silent Refactoring

### Symptoms

- “I just cleaned up the structure a bit”
- “It’s just renaming; logic unchanged”
- No documentation updates

### Risk

- Design semantics change silently
- Historical decisions are lost
- Debugging and tracing costs explode

### Principle

> **Refactoring without documentation does not exist.**

---

## 10. Early Warning Signs of Loss of Control

If you observe:

- Frequently editing code directly
- Documentation no longer updated
- Coding Agent often “guesses” intent
- Repeated explanations of the same thing
- Difficulty explaining why bugs occur

These indicate:

> Engineering is drifting away from Vibe + Coding.

---

## 11. Chapter Summary

Failures of Vibe + Coding almost never stem from insufficient model capability,
but from **relaxed engineering discipline**.

When the process starts deforming, do not try to:

“Use AI harder.”

Instead:

- Return to role separation
- Return to documentation
- Return to tests
- Return to freeze points

Vibe + Coding’s value lies not in flexibility,
but in providing a **path to retreat** when chaos emerges.
