© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.2

# Chapter V | Decision Phase

## The Sole Legitimate Place for High-Responsibility Judgments

In the Vibe + Coding engineering process, **the Decision Phase is the only phase where high-responsibility judgments are allowed to occur**.

This chapter does not discuss the overall process, nor does it re-explain role relationships; these have been explicitly frozen in previous chapters.

This chapter answers only one question:

> In an engineering project that requires long-term maintenance, audibility, and recursive expansion, how should all judgments that affect the long-term form, semantic boundaries, and maintenance costs of the system be legitimately generated, made explicit, and frozen?

---

## 1. The Engineering Status of the Decision Phase

The Decision Phase is not "thinking things over," nor is it "preparation before implementation."

It is an **institutionalized engineering activity** with a highly clear and irreplaceable goal:

> To complete all high-responsibility judgments in a state where they can be discussed and traced, and to freeze them as the sole legitimate basis for subsequent decomposition, execution, and audit.

What is completed in this phase is not the "optimal solution," but rather:

- Confirmation of problem boundaries.
- Delineation of system responsibility.
- Trade-off records of candidate plans.
- Explicit declarations of invariants and constraints.
- Informed acceptance of risks and costs.

Once these judgments are frozen, subsequent phases must not re-discuss their validity; they **only choose whether to comply**.

---

### Mental Model Analogy | Formation of Battle Determination

In a military command system, the Supreme Command must clarify battle determination before action begins:

- What objectives to achieve.
- What price is allowed to be paid.
- Which boundaries must absolutely not be touched.

The Staff system can provide analysis, plans, and projections, but whether to adopt them and to what extent is decided only by the Commander.

Once battle determination is formed, no frontline unit has the right to re-discuss "whether to fight" or "where to fight."

The Decision Phase in engineering corresponds exactly to this position.

---

## 2. A Basic Premise: The Decision Phase Does Not Generate Decisions Through Implementation

In the Decision Phase, **the introduction of engineering constraints is permitted and often necessary**, including but not limited to:

- Performance goals.
- Feasibility requirements.
- Resource and cost limits.

For example:
- "The system must run stably under the specified throughput."
- "If this module cannot meet real-time requirements, the overall plan is unacceptable."

These constraints **are themselves part of high-responsibility decisions** and must be **explicitly proposed, discussed, and frozen** in the Decision Phase.

---

However, in the Decision Phase, **it is not permitted to generate or solidify high-responsibility judgments through the implementation process itself**, for example:

- Deciding on system structure by "writing a version first to see how it looks."
- Defaulting to a certain design path as reasonable due to the accidental success of a demo.
- Implicitly establishing interfaces, boundaries, or divisions of responsibility in the code.

The issue is not one of efficiency, but of **responsibility legitimacy**.

Any judgment "naturally formed" through the implementation process inevitably introduces:

- Structural decisions that were never explicitly discussed.
- Trade-off paths that are difficult to trace.
- Design origins that cannot be clearly attributed for responsibility.

Once these judgments "happen secretly" through code, subsequent freezing, authorization, and auditing lose their basis for legitimacy.

---

### Special Clarification: Permitted Exploratory Behaviors and Their Engineering Status

In practice, the Decision Phase **allows for certain forms of exploratory activity**, including:

- Experimental code used to verify if an engineering prerequisite holds.
- Exploratory implementations used to measure performance ceilings or bottlenecks.
- Side-verification tasks with no direct dependency on the final engineering.

However, the prerequisite is that the Actor **must be clearly aware in their mental model**:

> These behaviors belong to the necessary reconnaissance before the decision and are not the battle determination itself.

These types of attempts have clear engineering status:

- Their results can only serve as material for discussion.
- They themselves do not constitute design decisions.
- They must not be directly incorporated into the long-term engineering structure.

Any conclusion derived from an attempt **must return to the decision discussion to be explicitly expressed, evaluated, and frozen**; otherwise, it lacks engineering legitimacy.

---

### Mental Model Analogy | Reconnaissance and Battle Determination

In a military system, reconnaissance is used to judge enemy situation and terrain, but it **cannot replace battle determination**.

If a commander defaults to changing operational objectives or advancement routes because a reconnaissance mission "went smoothly," that is not flexibility—it is loss of control.

Exploratory behaviors in engineering only possess institutional validity once they have been explicitly included in decision discussions and frozen.

---

## 3. Internal Structure of the Decision Phase: Four Unskippable Steps

To ensure high-responsibility judgments are fully made explicit before freezing, the Decision Phase must be organized through a fixed internal structure:

**Input → Alignment → Refinement → Freezing**

This is not a process control mechanism, but a **responsibility explicitization model**.

Before entering freezing, free back-and-forth and restarts are allowed between these four steps; once freezing is completed, any backtrack must explicitly break the frozen state.

---

## 4. Input: Defining the Subject of Discussion, Not Proposing Solutions

### Step Goal

The goal of the Input step is singular:

> To clarify what problem is currently being seriously discussed.

Input can be:
- A vague idea.
- A goal statement.
- A requirement that has not yet taken shape.

At this step:
- Completeness is not required.
- Correctness is not required.
- Technical selection is not performed.

The only judgment needed is:
> Is this problem worth entering into a high-responsibility design discussion?

Input should be **relatively clear narrative content**, rather than a question that directly hands the judgment power to AI.

---

### Examples (Illustrative)

**Legitimate Input Examples:**
- "We need a long-term maintainable evaluation system for comparing the performance of different LLM models."
- "The current system spins out of control when expanding to multiple data sources; we need to redefine boundaries."

**Illegitimate Input Examples:**
- "Python or Rust?"
- "Should we use a specific framework?"

---

### Mental Model Analogy | Defining the Operational Agenda

In a military system, the first step is not discussing tactics, but clarifying:
> Is this meeting about discussing attack, retreat, or supplies?

If even the subject of discussion is unclear, any subsequent projection is merely noise.

---

## 5. Alignment: Eliminating Ambiguity in Problem Definition

### Step Goal

The goal of the Alignment step is:
> To ensure the Actor and the collaborative agent reach a unified understanding of "what problem is being solved."

This step does not generate design plans; it only produces a **clearly written problem definition**.

---

### Legitimate Behaviors

- Requiring the collaborative agent to restate their understanding of the problem.
- Proactively exposing implicit assumptions.
- Clarifying goals, boundaries, and non-goals.

---

### Examples (Illustrative)

**Legitimate ways to ask during Alignment:**
- "Please restate your understanding of the system goals and what specifically we are not solving."
- "Please describe from an engineer's perspective what my goal is."

The sign of completed alignment is not that it "sounds about right," but that the **problem definition has been explicitly written and confirmed/accepted by the Actor**.

---

### Mental Model Analogy | Unified Operational Language

In an operational meeting, if different departments have different understandings of the "main direction of attack," then even the most ingenious tactical discussion is meaningless.

The value of the Alignment step lies in **eliminating such ambiguity in advance**.

---

## 6. Refinement: Constructing an Engineering Structure Capable of Bearing Responsibility

### Step Goal

The goal of the Refinement step is:
> Based on the aligned problem definition, transform the vague problem into a structural foundation for execution and, at the end of this step, explicitly provide a **viable plan capable of bearing responsibility**.

A "viable plan" here does not refer to a specific implementation path, but to a system structure that is already closed in terms of responsibility, boundaries, and authorization.

In this step, the Vibe Agent is the primary auxiliary role: proposing reference plans, exposing risks, filling loopholes, and challenging assumptions—but all critical judgments must be completed explicitly by the Actor.

---

### Legitimate Activities

- Division of modules and responsibility boundaries.
- Comparison of candidate plans.
- Extraction of invariants and constraints.
- Preliminary definition of interfaces and data forms.

The collaborative agent can propose multiple plans, but **all judgments must be completed explicitly by the Actor, who then bears the responsibility**.

---

### Examples (Illustrative)

**Legitimate Refinement input examples:**
- "What premises do you think are implicit in this problem? Which ones would lead to overall failure if incorrect?"

**Legitimate Refinement output examples:**
- "The system must strictly distinguish between Input, Evaluation Core, and Output."
- "This interface only accepts POST methods, not GET."

**Illegitimate Refinement behaviors:**
- "Let's write a version first to see if the structure is reasonable."
  —— Introducing a demo into long-term engineering is tactical reconnaissance, not battle determination.
- "Decide these boundaries during implementation."
  —— Instructions are vague; either explicitly exclude it from this discussion or define it clearly now, otherwise it constitutes an overreaching authorization.

---

### Mental Model Analogy | Staff Plans and Command Responsibility

The Staff can propose various operational plans, but once failure occurs, the responsibility is always borne by the commander who made the choice.

The Refinement step in engineering is the process where the explicit落点 (focal point) of responsibility gradually forms.

---

## 7. Freezing: Forming the Sole Legitimate Basis for Design

Freezing is the **only step in the Decision Phase with institutional validity**.

At this node, the Actor must explicitly complete:

- Confirmation of design conclusions.
- Acceptance of trade-offs and exclusions.
- Informed recognition of risks and limitations.

The form of freezing can be:
- Design Documents.
- Architectural descriptions.
- Explicit declarations of invariants.

Form is not important; semantics are:
- Which judgments have been accepted.
- Which trade-offs are no longer discussed.
- All subsequent behaviors must follow this.

The freezing result will serve as:
> The sole legitimate basis for judging "whether authority has been exceeded" in the Decomposition, Execution, and Audit phases.

---

### Mental Model Analogy | Signing Operational Orders

In a military system, once an operational order is signed, it gains institutional validity.

Any temporary judgment that "looks more reasonable on-site" constitutes overreaching if it exceeds the order's authorization.

---

## 8. Freezing and Backtracking: The Sole Legitimate Path for Modification

Freezing does not mean "never modify."

However, any modification must satisfy the following conditions:
1.  Explicitly break the frozen state.
2.  Return to the Decision Phase.
3.  Update documentation and constraints.
4.  Re-complete freezing.

There is no legitimate path for bypassing freezing by modifying code or adjusting implementation details.

---

## Chapter Summary

The Decision Phase is not an inspiration phase, nor is it a warm-up before implementation.

It is:
- The sole legitimate place for high-responsibility judgments.
- The semantic source for subsequent decomposition, execution, and audit.
- The generation point for "facts that can be recursively referenced" in engineering.

When the Decision Phase is strictly enforced:
- Subsequent tasks can be safely delegated.
- The Execution Phase can be strictly constrained.
- The Audit Phase can perform effective responsibility attribution.

**This is the engineering significance of the Decision Phase in Vibe + Coding that cannot be weakened.**
