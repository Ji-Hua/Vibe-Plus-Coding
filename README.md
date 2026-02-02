© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0

# Vibe + Coding  
**Vibe Plus Coding (VPC) = verdict frozen, permission explicit, context isolated**

## The Real Problem with AI Coding at Scale

Most large-scale failures of AI Coding are **not caused by insufficient model capability**.

They are caused by a **systematic violation of the Dependency Inversion Principle (DIP)**.

In healthy software engineering:

> **High-level abstractions must not depend on low-level implementations.**  
> Implementations exist to realize decisions — not to make them.

However, in today’s *common AI coding usage patterns*, this dependency is quietly reversed.

---

## How Dependency Inversion Gets Broken

In typical AI-assisted workflows:

- Architectural decisions are **implicitly made during implementation**
- AI “helpfully” resolves structural questions while writing code
- High-level abstractions are **shaped by local implementation convenience**

This means:

> **Low-level implementation is deciding high-level design.**

That is a direct, structural violation of DIP.

This is not a usage mistake by individual engineers.  
It is a **default outcome** of allowing design judgment to occur during execution.

The more capable the AI becomes, the faster this inversion happens.

---

## Why This Cannot Be Fixed by “Better Prompts”

Prompting, code review, specs, and tests all operate **after** the dependency has already been inverted.

Once implementation feedback is allowed to reshape abstraction:
- design authority is lost,
- decisions become implicit,
- and responsibility becomes untraceable.

No amount of intelligence can fix a broken dependency direction.

---

## What Vibe + Coding Actually Does

**Vibe + Coding is not about using AI more carefully.**  
It is about **putting AI back into a dependency-legal position**.

### 1. Vibe Writing (Decision Phase)

AI is used *before implementation* to:
- explore architecture,
- surface trade-offs,
- challenge assumptions.

AI has **advisory power only**.  
Humans make the final decisions.

The output is a **design document** that explicitly freezes high-level abstractions.

At this point, dependency direction is locked.

---

### 2. Task Specifications (Authorization Interface)

Frozen design decisions are translated into **task specifications**.

These documents define:
- what may be implemented,
- what must not change,
- and what completion means.

They are not suggestions.  
They are **execution authorizations**.

---

### 3. AI Coding (Execution Phase)

The Coding Agent operates only within the task specification.

It is free to:
- choose implementation details,
- resolve local technical decisions.

It is not allowed to:
- reinterpret architecture,
- expand scope,
- or revise abstractions.

Implementation depends on abstraction — never the other way around.

---

### 4. Audit (Dependency Enforcement)

An independent Audit Agent compares:
- what was implemented,
- against what was authorized.

It answers one question only:

> **Did implementation violate the frozen abstraction?**

Audit exists because **DIP enforcement cannot rely on trust or intent**.

---

## Not a Linear Workflow

This structure is recursive and composable:
- one design round can feed the next,
- tasks can be grouped or delayed,
- audits can occur at module boundaries.

What never changes is **direction**:
- abstraction flows downward,
- implementation flows upward,
- responsibility remains traceable.

---

## One-Line Definition

> **Vibe + Coding is a structural correction to AI Coding:  
> it restores the Dependency Inversion Principle by moving design decisions out of implementation and enforcing them through explicit documentation and audit.**

Or, more bluntly:

> **Vibe + Coding = Vibe Writing + AI Coding —  
> with dependency direction enforced.**
