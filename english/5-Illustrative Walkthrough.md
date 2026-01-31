© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.1

# Chapter 5｜Illustrative Walkthrough: A Complete Vibe + Coding Flow

This chapter is **not a real, complete, directly reproducible engineering case**.
It does not aim to cover every detail of a project from zero to one.

Its sole purpose is:

> **To connect every key step of Vibe + Coding through a “hypothetical but sufficiently concrete” example,
> so you can clearly see what you should do at each step—not how to write code.**

Think of this chapter as:

- A process diagram
- A rehearsal-style walkthrough
- A transferable operational skeleton

Not as:

- A full tutorial
- A best-practice implementation
- A real project blueprint

---

## Reading Conventions (Very Important)

- The example is deliberately simplified
- All prompts are illustrative
- Outputs prioritize correctness of direction, not completeness
- The chess project is merely a vehicle, not the focus

Do not attempt to copy this chapter verbatim into a real project.

---

## 0. Example Problem Setup (For Illustration Only)

Assume the following engineering idea:

- Project: Chess
- Goal: Support local two-player matches
- Interface: Command line
- Language: Python
- Non-goals:
  - GUI
  - Network play
  - Performance optimization
  - AI algorithms

This problem has two characteristics:

- Clear rules
- Complex state

It is ideal for **demonstrating process, not technique**.

---

## Step 1 — Input: Declare the Problem Only

### What You Are Doing

You are telling the Vibe Agent:

> “This is what we are about to seriously discuss.”

Not:

> “Design or implement this system for me.”

### Illustrative Vibe Prompt (Input)

- I want to build a chess program in Python.
- Phase one only considers local two-player play via CLI.
- Do not design or write code yet.
- First, record my description.
- After I say “input finished,” do only two things:
  1) Restate your understanding of the requirements;
  2) List what you think is unclear.

Input finished.

### Tip

If the AI starts discussing modules, classes, or implementation,
you failed to prevent it from entering design mode during Input.

---

## Step 2 — Alignment: Confirm We Are Discussing the Same Thing

### What You Are Doing

You are not advancing solutions.
You are eliminating misunderstandings.

Alignment aims for **shared understanding**, not better ideas.

### Illustrative Alignment Actions

- Ask the AI to restate requirements
- Correct deviations
- Resolve key uncertainties
- Explicitly define non-goals

### Tip

“Restate your understanding” works when inputs are already precise;
“List unclear points” works better when inputs are vague.

---

## Step 3 — Refinement: Turn the Problem into Structure

### What You Are Doing

You allow the AI to participate in **structural thinking**, but only about:

- Modules
- Responsibilities
- Data
- Flow

Not implementation.

### Illustrative Vibe Prompt (Refine)

- Based on the aligned requirements:
  - Propose a minimal viable system structure
  - Explain module boundaries and responsibilities
  - Describe core data models
  - Describe minimal execution flow
- Do not write code; output structured design only.

### Tip

Common mistakes in refinement:

- Obsessing over implementation details too early
- Attempting to design the final form in one pass

You only need **a system model suitable for documentation**.

---

## Step 4 — Freeze: Turn Discussion into Documentation

### What You Are Doing

You are performing a critical but often skipped step:

> **Fixing what we currently believe is correct.**

### Illustrative Freeze Actions

- Ask the AI to organize current design into a document
- Explicitly state this is a phase conclusion
- Declare it the authoritative source for execution

### Tip

A simple test:

> If you would hand this document to someone who “executes without thinking,”
> the freeze is sufficient.

---

## Step 5 — From Document to Tasks: Illustrative DFS Decomposition

### What You Are Doing

You are not planning the whole project.
You are asking:

> “Which small piece can be independently completed next?”

### Illustrative Task Decomposition

For example:

- Task 1: Board and coordinate system
- Task 2: Piece abstraction
- Task 3: Move representation
- …

Each task must be:

- Independently implementable
- Testable
- Auditable

---

## Step 6 — Make One Task Executable

### What You Are Doing

You are transforming a task from:

“Engineer-understandable”
into
“Executor-proof.”

### Illustrative Task Document Includes

- Task goal
- Authoritative design source
- Scope and boundaries
- Behavioral constraints
- Completion criteria

### Tip

Self-check:

> **If I were the executor, would I need to guess anything?**

---

## Step 7 — Coding: Switch Session, Execute Only

### What You Are Doing

You deliberately **reduce AI freedom**.

- New session
- No shared context
- Only the task document

### Illustrative Coding Prompt Characteristics

- Explicitly state this is execution
- Declare authoritative sources
- Explicitly forbid design changes
- Require test-first
- Require implementation report

### Tip: Context Health Signal

A practical trick:

- Require the AI to output a fixed marker (e.g., today’s date) at the end of each response
- If the marker disappears across responses, stop and restart the session

This usually indicates context degradation.

---

## Step 8 — Review Loop: Compare Against Documentation

### What You Are Doing

You are not asking:

> “Is the code good?”

But:

> “Did the code faithfully execute the document?”

Any deviation must be attributed to:

- Design issues
- Or execution issues

Never masked with patches.

---

## Chapter Summary

This chapter uses a **deliberately simplified illustrative example**
to demonstrate the full operational skeleton of Vibe + Coding:

- How to start discussion
- How to align
- How to converge
- How to freeze
- How to decompose
- How to execute
- How to review

You do not need to remember chess.
You do not need to remember the prompts.

Remember only one thing:

> **At each step, are you thinking—or executing?**

Once these two mix, the process degrades.
