© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.2

# Chapter VI | Decomposition Phase

## The Sole Legitimate Path from Frozen Decisions to Executable Tasks

In the Vibe + Coding engineering process, **the Decomposition Phase is the only allowed transition zone between decision and execution**.

If the Decision Phase solves:
> **"What we have decided and what we are no longer discussing"**

Then the Decomposition Phase solves only one problem:
> **How to transform frozen design decisions into task descriptions that can be directly understood and executed by the execution entity, without introducing any new high-responsibility judgments.**

The Decomposition Phase is not a continuation of the design phase, nor is it the start of the execution phase.

It is a **translation job**, not a judgment job.

---

## 1. The Engineering Status of the Decomposition Phase

The core engineering goal of the Decomposition Phase can be precisely defined as:

> **Translating frozen high-responsibility design conclusions into structured, unambiguous, and auditable Task Specifications, clarifying which judgments have been completed and which are authorized for the subsequent execution phase.**

In this phase:
- **Do not** re-discuss whether the design is reasonable.
- **Do not** supplement new system-level judgments.
- **Do not** introduce new sources of responsibility through "decisions made along the way."

Failure in the Decomposition Phase often stems not from a lack of execution capability, but because **design judgments are quietly rewritten here**.

---

### Mental Model Analogy | From Battle Determination to Operational Order

In a military system, battle determination itself cannot be directly executed by frontline units.

It must be translated into **structured, verifiable operational orders**:
- Clear task objectives.
- Clear scope of action.
- Clear prohibited items.
- Clear completion conditions.

If this step is missing, so-called "execution flexibility" only evolves into overstepping authority.

The Decomposition Phase corresponds to this role.

---

## 2. Participating Roles and Division of Responsibility

### Participating Roles
- **Vibe Agent**
  The primary executor of the Decomposition Phase, responsible for structural expression and task breakdown.
- **Actor (Human Engineer)**
  The final confirmer of decomposition results, responsible for judging whether the decomposition **faithfully reflects the original decision**.

---

### Responsibility Boundaries
In the Decomposition Phase:
- Vibe Agent **can decide on the form of expression**.
- Vibe Agent **cannot decide on the meaning of the design**.
- Actor **no longer makes design choices**.
- Actor **only judges if a semantic shift has occurred**.

In other words:
> The Decomposition Phase allows for "how things are said," but not for "saying something different."

---

## 3. Inputs and Outputs of the Decomposition Phase

### Legitimate Input
The Decomposition Phase accepts only one type of legitimate input:
- **Frozen design decision artifacts.**

Including but not limited to:
- Design Documents.
- Architectural descriptions.
- Declarations of invariants and constraints.

If the input itself still contains ambiguity, it indicates the problem should be pushed back to the **Decision Phase**, rather than being remediated here.

---

### Legitimate Output
The output of the Decomposition Phase is one or more **Task Specifications**.

Every Task Specification must satisfy:
- Being independently understandable.
- Being independently executable.
- Being independently auditable.

It is not a prompt, nor a temporary instruction, but a **formal engineering artifact**.

---

## 4. Engineering Definition of Task Specifications

In Vibe + Coding, a Task Specification is not an execution instruction or implementation hint; it is an **engineering artifact used to define the responsibility boundary of the execution phase**.

Its core purpose is singular:

**To clarify for the execution phase, once and for all, without introducing new judgments: what to achieve, who has the final say, what cannot be moved, how one is permitted to act, and when it is considered complete.**

To prevent Task Specifications from degrading into mere checklists or casual instructions, they must be clarified from an engineering perspective:
**A qualified Task Specification must simultaneously cover constraints in the following five directions.**

These directions have no sequential order; they jointly constitute the legitimate action space of the execution phase.

---

### 4.1 Goals and Intent (What to complete in this task)

This part serves to clarify:
**The state change the system should undergo relative to the start of the task once the task is complete.**

It focuses on "what the world looks like after completion," rather than "what should be done in the middle."

In this direction, the Task Specification should clarify:
- The core goal of this task.
- The specific problem this change seeks to solve.
- The overall state that should be satisfied upon successful completion.

This part usually **retains implementation freedom**. As long as the final state satisfies the goal, the execution entity can choose the implementation path itself, provided it does not violate other constraints.

**Mental Model Analogy:**
This is equivalent to the **Operational Objective** in combat—such as "hold the position" or "seize the high ground." It defines the direction of the action, not the end-point of completion.

---

### 4.2 Authority and Adjudication (Who has the say when conflict arises)

This part serves to clarify:
**Where the final adjudicatory power lies when inconsistencies arise between different information sources.**

In complex engineering, documentation, tests, existing implementations, and historical experience are often not perfectly consistent. If the Task Specification does not define the source of adjudication, the execution phase will be forced to "choose who to believe" on its own, thereby unintentionally assuming design responsibility.

In this direction, the Task Specification should clarify:
- Which documents or specifications hold supreme authority.
- The status of other materials in this task.
- The order of adjudication to follow when conflicts occur.

The purpose of this part is to **block the possibility of the execution phase re-introducing design judgments through selective interpretation**.

**Mental Model Analogy:**
This is equivalent to the **Battle Objective and Command Attribution** in combat—once determined, frontline units have no right to change the direction of action themselves.

---

### 4.3 Boundaries and Freezing (Which engineering facts must not be touched)

This part serves to clarify:
**Which engineering judgments have already been completed and are not within the discretionary scope of the execution phase for this task.**

It focuses not on "what the system looks like now," but on "what things are explicitly frozen for this task."

In this direction, the Task Specification usually freezes:
- The scope allowed or prohibited for modification.
- Established structural designs and module responsibilities.
- Interface semantics, invariants, or other hard constraints.
- Content explicitly excluded from this task.

If this part is missing, the execution entity will often make substantial modifications to established decisions in the name of "making things easier to implement."

**Mental Model Analogy:**
This is equivalent to the **Strategic Boundaries and Restricted Zones** in combat—the frontline can maneuver but has no right to change the combat zone range or defense positions.

---

### 4.4 Execution Constraints and Work Method (How one is allowed to work)

This part serves to clarify:
**The working method and operational form permitted for the execution phase at the engineering level.**

It does not guide specific operational steps, but rather limits the freedom of the execution phase to prevent the introduction of implicit complexity or unauditable discrepancies.

In this direction, the Task Specification usually constrains:
- Tools and operation modes allowed or required for use.
- Established development methods and work discipline.
- Engineering norms, code quality, and organizational rules.
- Placement principles for artifacts (code, tests, documentation).

These constraints do not decide "where to fight," but rather "In what form to fight."

**Mental Model Analogy:**
This is equivalent to the **Selection of Operational Form and Tactical Means Constraints** in combat—clarifying whether this fight uses armored advancement, paratrooper assault, or position defense, but not deciding specific advancement routes or which unit goes first.

Once the operational form is determined, it must not be switched arbitrarily during execution.

---

### 4.5 Acceptance and Completion Semantics (When it is considered complete)

This part serves to answer an unavoidable question:
**In an engineering sense, how to judge if this task is completed.**

If the Task Specification cannot clarify completion criteria, the execution phase cannot end work autonomously, and the audit phase cannot judge if authority has been exceeded.

In this direction, the Task Specification should clarify:
- Functional semantics and behavioral constraints that must be satisfied.
- Explicitly prohibited behaviors.
- Observable manifestations of success and failure.
- Verifiable completion conditions.
- Necessary audit and summary artifacts.

**Goal and completion criteria are concepts at two different levels.**

**Mental Model Analogy:**
The Operational Objective might be: "Hold the position."
But completion criteria must further clarify: "Hold the position until 10 PM, with the defense line remaining unbroken."

The former defines **what to do**, while the latter defines **to what degree it counts as qualified** so that the action can end. Without completion criteria, action cannot end, and responsibility cannot be traced.

---

### A Crucial Reminder
The five directions above are not a writing order, nor are they independent items.
They jointly define:
**The authorized action space and the insurmountable responsibility boundaries for the execution phase.**

If any of these directions are missing, the Task Specification is incomplete in an engineering sense.

---

### Section Summary
The value of a Task Specification lies not in how detailed it is written, but in whether it once and for all solves the problems the execution phase should no longer think about.

When goals are clear, authority is defined, boundaries are frozen, operational forms are controlled, and completion criteria are verifiable, the execution phase can be safely outsourced without fear of the design being quietly rewritten during implementation.

---

## 5. Qualified Criterion for the Decomposition Phase

Whether a decomposition result is qualified can be judged by a very strict engineering standard:

> **If the Task Specification is handed to an execution entity that did not participate in previous discussions, can it begin work without asking any more design-related questions?**

Questions the execution entity is allowed to raise include:
- Clarifications on implementation details.
- Technical-level choice spaces.

But questions **not allowed** include:
- "Should this module also be responsible for X?"
- "Is this boundary already decided by you, or can I change it?"
- "Is this design confirmed now, or should we see during implementation?"

Once these questions arise, it indicates the Decomposition Phase **failed to fulfill its engineering responsibility**.

In simpler terms: if an Actor, as a human engineer, receives this Task Specification, would they be able to successfully complete the task without overstepping boundaries?

---

## 6. Common Error: Re-designing during the Decomposition Phase

The most common and dangerous error in the Decomposition Phase is:
> **Re-introducing design judgments in the name of "making the task easier to execute."**

Typical manifestations include:
- Supplementing new design assumptions in the Task Specification.
- Weakening original constraints for the sake of "easy implementation."
- Modifying interface meanings without returning to the Decision Phase.

These behaviors appear reasonable in form, but are **completely unacceptable** in terms of engineering responsibility.

---

### Mental Model Analogy | Frontline Rewriting Operational Orders
A frontline commander can choose attack routes but has no right to modify operational objectives.

Any behavior that modifies the order itself based on "site conditions being more suitable" is considered a serious disciplinary violation in a military system.

---

## 7. Decomposition and Backtracking: The Sole Legitimate Path for Correction

If, during the decomposition process, it is discovered that:
- The original design contains ambiguity.
- Decision conclusions are insufficient to support the task definition.

**The only legitimate way to handle this is:**
1.  Suspend current decomposition work.
2.  Explicitly push the problem upward.
3.  Return to the **Decision Phase** to supplement or correct the design.
4.  After re-freezing, re-enter decomposition.

There is no legitimate path for "temporarily patching the design" during the Decomposition Phase.

---

## Chapter Summary

The Decomposition Phase is not a thinking phase, nor is it a prelude to the execution phase.

It is:
- A **responsibility isolation layer** between decision and execution.
- A **structural buffer zone** to prevent the design from being quietly tampered with.
- **One of the sole sources** of legitimacy for the execution phase.

When the Decomposition Phase is strictly enforced:
- The execution phase can be safely and completely outsourced.
- The conclusions of the Decision Phase will not be eroded by the implementation process.
- The Audit Phase can clearly judge if authority has been exceeded.

**This is the engineering significance of the Decomposition Phase in Vibe + Coding that cannot be skipped.**
