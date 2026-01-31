© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.1

# Chapter 1｜Design Philosophy

In the introduction, I explained that Vibe + Coding is not an accidental trick, but the result of repeated failures and corrections in real engineering practice.
The purpose of this chapter is to further clarify the **engineering stance and design assumptions** behind this paradigm.

---

## 0. What Is Vibe + Coding (A Clear and Executable Definition)

**Vibe + Coding is not a “smarter form of Vibe Coding.”
It is a forced decomposition of traditional Vibe Coding into two strictly separated stages.**

These two stages are:

- **Vibe (Design Phase)**
- **Coding (Implementation Phase)**

Their relationship is not collaborative mixing, but **responsibility isolation**.

### The Vibe Phase (Design Phase)

The Vibe phase is responsible for only one thing:

> **Transforming the human engineer’s design intent into executable external structure.**

Its outputs include, but are not limited to:

- Design documents
- Architecture descriptions
- API specifications
- Data structure definitions
- Task specifications
- Behavioral constraints
- Test designs (or test intent)

In this phase:

- No implementation is pursued
- Syntax details are ignored
- “Writing a bit of code just to see” is not allowed

The sole goal of the Vibe phase is to **freeze decisions and externalize them as documentation**.

---

### The Coding Phase (Implementation Phase)

The Coding phase is likewise responsible for only one thing:

> **Strictly implementing under existing documentation and tests.**

In this phase:

- Design is not re-discussed
- No new implicit assumptions are introduced
- No “structural optimizations” are made
- No undocumented behavior is added

The input to the Coding phase is documentation.
The output is code.

---

### A Critical Constraint: No Shared Context

**Vibe and Coding must not share context.**

This is not a recommendation—it is a **necessary condition** for the paradigm to hold.

This means:

- All information from the Vibe phase must be transmitted through documents
- The Coding phase must not rely on “previous conversations”
- There is no implicit communication channel beyond documents and tests

At the tooling level, this isolation can be enforced in multiple ways:

- Using different tools (e.g., ChatGPT for Vibe, Cursor or Copilot for Coding)
- Using different sessions within the same tool
- Using different agent instances with shared history explicitly disabled

**If context is shared, Vibe + Coding degenerates back into old Vibe Coding.**

---

### One-Sentence Definition

> **Vibe + Coding =
> Forcibly splitting Vibe Coding into two stages—
> “design generates documents” and “code is implemented from documents”—
> with strict responsibility separation and context isolation,
> communicating only through documentation and tests.**

If you cannot do this, you are still practicing old Vibe Coding.

---

## 1. Two Fundamentally Different Programming Paradigms

### Vibe Coding (The Old Paradigm)

In this guide, **Vibe Coding** refers to the most common AI-assisted programming approach today:

- Continuous interaction with AI in a single conversation
- Design, implementation, and debugging mixed together
- AI simultaneously “understands the problem” and “writes the code”
- Engineering continuity depends on implicit memory within the context window

This approach works well for:

- Prototyping
- One-off scripts
- Small tools
- Exploratory experiments

But in medium- to large-scale systems, it systematically fails:

- Design intent drifts over time
- Implementation details reverse-drive structure
- Decisions are buried in code and become untraceable
- When issues arise, it becomes hard to explain “why it is this way”

This is not due to user carelessness or model weakness.
It is because this mode **lacks engineering-grade stability**.

Unless otherwise stated, “Vibe Coding” in this guide always refers to this old paradigm.

---

### Vibe + Coding (The New Paradigm)

**Vibe + Coding is not an enhanced version of Vibe Coding.
It is a structural decomposition of it.**

It forcibly separates the previously entangled process into two stages:

- **Vibe: design phase, producing documentation**
- **Coding: implementation phase, executing against documentation**

Responsibilities are separated, context is isolated,
and communication happens only through documents and tests.

Vibe + Coding does not focus on making AI smarter.
Instead, it focuses on:

- Who is responsible for thinking
- Who is responsible for execution
- How decisions are frozen
- How system semantics are preserved

In this paradigm:

- The human engineer is always the project owner
- AI does not participate in design judgment
- AI exists purely as a **constrained execution role**

Once this separation is broken, the process inevitably collapses back into old Vibe Coding.

---

## 2. The Real Problem This Paradigm Solves

In real-world software development, engineers rarely spend most of their energy on the truly hard parts.

Instead, time is consumed by:

- Glue code
- Repetitive structures
- Boilerplate logic
- Framework-driven scaffolding
- Engineering noise unrelated to core design

Meanwhile, the aspects that truly determine system quality and longevity—

- Architecture
- Abstraction modeling
- Interface boundaries
- Invariant definitions
- Long-term maintainability judgments

—are often rushed through in fragmented time.

Vibe + Coding is not about “letting one person write more code.”
It addresses a more realistic question:

> **How can engineers spend their limited cognitive resources on what is truly irreplaceable?**

Thus, its goal is not efficiency maximization, but:

> **Integrity of engineering responsibility.**

### No Silver Bullet

**Vibe + Coding was never meant to make programming easy.**

Programming is inherently difficult.
Any narrative claiming that complex engineering can be solved simply by “writing better prompts” or “letting AI handle everything” is a misreading of engineering reality.

Vibe + Coding does not attempt to reduce thinking.
It does one thing only:

> **Redistribute where, how, and by whom thinking occurs.**

---

## 3. A Reality That Must Be Faced: Context Is Fragile

At the current stage, all large language models share an unavoidable limitation:

**Context windows are finite and unstable.**

As task scale grows, this limitation systematically surfaces:

- Early design decisions are gradually forgotten
- Implicit constraints between modules disappear
- Implementations become “locally correct, globally wrong”
- Root causes are hard to trace once problems appear

Relying on “continuous conversational memory” for complex engineering is itself a high-risk assumption.

This is not a model problem.
It is an **engineering assumption problem**.

---

## 4. The Core Assumption of Vibe + Coding

Vibe + Coding is built on a clear and restrained assumption:

> **AI is not suited to holding the full semantics of complex systems over long periods.**

Therefore, instead of asking AI to “remember the entire project,” we should change how engineering work is organized:

- Decompose complexity into independent subtasks
- Provide each subtask with complete, closed, understandable specifications
- Execute within controlled contexts
- Preserve decisions through documentation and tests

Under this structure, AI instability is confined locally,
while global system semantics remain under human control.

---

## 5. The Redefined Role of Documentation

In Vibe + Coding, documentation is not an after-the-fact record.
It is part of the system structure.

Documentation serves as:

- A carrier of design consensus
- A boundary for frozen decisions
- A semantic source for auditability

It serves three audiences simultaneously:

- Providing execution constraints for the Coding phase
- Acting as a stable memory anchor for the Vibe phase
- Preserving context for your future self

Engineering thus shifts from “continuous conversation” to:

**Discrete, versionable, traceable decision sequences.**

---

## 6. Thinking Is Shifted Forward, Not Reduced

One thing must be made clear:

Vibe + Coding does not reduce thinking.

On the contrary, it demands more intensive upfront thinking.

Many decisions that were previously made “while coding” must now be explicitly considered, written down, and frozen during the Vibe phase.

This is a deliberate engineering trade-off:

- More upfront design investment
- Less low-level implementation labor
- Higher long-term maintainability

If you are accustomed to coding first and thinking later, this paradigm may feel uncomfortable.

But if you value design-first and test-driven engineering, it often brings a stronger sense of control.

---

## 7. Principles on Scope of Applicability

Vibe + Coding is not a universal solution.

It is best suited for **design-driven problems**, not implementation-driven ones.

When a project’s core difficulty lies in:

- System decomposition
- Abstraction stability
- Boundary clarity
- Long-term invariants

Design quality matters far more than implementation speed.

In such problems, Vibe + Coding provides the greatest value.

Conversely, when the core questions are still:

- Can this be built at all?
- Can performance meet requirements?
- Is this approach viable?

Freezing design early is often inappropriate.

Specific misuse cases and failure modes will be discussed in later chapters.

---

## 8. Chapter Summary

Vibe + Coding is not a shortcut, nor a bag of tricks.
It is a deliberate engineering stance:

- Trade structure for stability
- Trade documentation for memory
- Trade design for scale
- Trade upfront thinking for long-term returns

When engineers focus on “what to do and why,”
and AI focuses on “how to correctly execute under constraints,”
true collaboration becomes possible.

This is the core design philosophy this guide aims to establish.
