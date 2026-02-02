© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.2

# Chapter IV | The Optimal Engineering Process for Vibe + Coding

This chapter provides the definition of the optimal **engineering process** for Vibe + Coding.

This process is not a "collection of tips on how to use AI," but a **process model based on responsibility as the core, documentation as the interface, and auditing as the constraint**.

It does not answer "what AI can do," but rather:

> **In a project that requires long-term maintenance, how should different agents collaborate under strict constraints, and how can we ensure that decision-making power, execution power, and responsibility never become misaligned?**

In the previous chapter, we established a unified mental model through a military command system. This chapter will strictly describe the process ontology in **engineering language** and provide, at critical structural nodes marked as **[Mental Model Analogy]**, a comparative re-description using the military command system to explain why these engineering constraints cannot be weakened or bypassed.

---

## 1. The Basic Unit of the Process: A Responsibility Closed-Loop

In Vibe + Coding, the basic unit of the process is **not the entire project**, but a single **engineering closed-loop completed within clear responsibility boundaries**.

An engineering closed-loop can correspond to:

- A functional module.
- A subsystem.
- A phase objective.
- Or an independently deliverable responsibility unit.

Therefore, the process described in this chapter does not signify "project completion," but rather means:

> **Within the current scope of responsibility, a legitimate decision, decomposition, execution, and audit have been completed, and the results have been reclaimed by the responsible person.**

Engineering scale is expanded step-by-step through the **recursive combination of multiple responsibility closed-loops**.

---

### Mental Model Analogy | Responsibility Closed-Loop

In a military command system, the smallest unit that can be strictly controlled is not the "entire war," but a single, clearly authorized combat action with a clear goal and the possibility of debriefing. Every action has a clear commander, staff support, execution units, and military discipline constraints, and upon the conclusion of the action, the results must be confirmed by the command level, which then bears the consequences. Without such an action loop, any command system would rapidly spiral out of control.

---

## 2. Process Overview: Four Unmixable Phases

The engineering process of Vibe + Coding is explicitly divided into four phases:

1.  **Decision Phase**
2.  **Decomposition Phase**
3.  **Execution Phase**
4.  **Audit Phase**

These four phases are not simple sequential steps, but rather **engineering zones where responsibility density decreases step-by-step, but constraint intensity increases step-by-step**.

Each phase strictly defines:

- Participating roles.
- Legitimate inputs and outputs.
- Permissible behaviors.
- Explicitly prohibited acts of overreaching authority.

---

## 3. Decision Phase: The Sole Legitimate Place for High-Responsibility Decisions

### Phase Goal

To transform vague, incomplete requirements and objectives into **clear, freezable design decisions that can be executed and audited in subsequent phases**.

### Participating Roles

- **Actor (Human Engineer)**: The sole bearer of responsibility and confirmer of decisions.
- **Vibe Agent**: A collaborator participating in analysis, projection, and expression, who possesses no decision-making power.

### Input

- Vague requirement descriptions.
- Problem background and constraints.
- Business or technical objectives.

### Core Activities

In this phase, the Actor, assisted by the Vibe Agent, completes:

- Clarifying what problem to solve and explicitly what not to solve.
- Defining the responsibility boundaries of the system or module.
- Comparing candidate plans and making trade-offs.
- Clarifying invariants that must hold true long-term.
- Judging which risks are acceptable and which must be avoided.

It must be emphasized that:

> **Any judgment that will affect the long-term form, semantic boundaries, or maintenance cost of the system must be completed and explicitly confirmed in this phase.**

### Output

- A complete, clear, and frozen Design Document.

From this moment on, the Design Document enters a read-only state; subsequent phases are no longer allowed to introduce new high-responsibility judgments.

---

### Mental Model Analogy | Design Decisions and Command Intent

In a military system, the Supreme Commander must clarify battle determination before the action begins, including objectives, the price allowed to be paid, and boundaries that must absolutely not be touched. The Staff can propose various plans, analyze risks, and expose assumptions, but whether to adopt them and to what extent is decided only by the Commander. Once the battle intent is formed, no frontline unit has the right to re-discuss "whether to fight" or "where to fight."

---

## 4. Decomposition Phase: From Decision to Executable Tasks

### Phase Goal

To transform frozen design decisions into **concrete task descriptions that can be directly understood and executed by the execution entity**.

### Participating Roles

- **Vibe Agent**: Primarily responsible for decomposition and structural expression.
- **Actor (Human Engineer)**: Responsible for confirming whether the decomposition results faithfully reflect the original decision.

### Input

- Frozen Design Document.

### Core Activities

In this phase, the Vibe Agent breaks down the Design Document into **one or more Task Specifications**.

Every Task Specification must explicitly answer:

- What specifically needs to be completed in this task.
- Which design conclusions are already frozen and must not be touched.
- Which judgments are explicitly delegated to the execution phase.
- How to objectively judge if the task is completed.

---

### Mental Model Analogy | Staff and Operational Orders

In a military system, the Commander does not issue vague intents directly to the frontline; instead, the Staff translates the battle determination into structured operational orders. These orders clearly define task objectives, range of action, prohibited items, and explicitly state "under what state the task is considered completed." Determination that has not been clearly translated into an order is equivalent to non-existence at the frontline.

---

### The Engineering Status of Task Specifications

 A Task Specification is a **formal engineering artifact**, not a temporary prompt or a casual instruction.

Every Task Specification must contain:

- Clear task objectives.
- Clear authorization boundaries and prohibited items.
- Technical space for free choice.
- **Criteria for task completion (Tests).**

---

### Mental Model Analogy | Mission Orders and Completion Criteria

In an operational order, the criteria for victory or defeat are not questions for post-hoc discussion but are part of the order itself. If the order does not explicitly state "reaching what state allows the action to end," then the action can neither be executed, nor evaluated, let alone be traced for responsibility. The status of tests in engineering is equivalent to the completion criteria in an operational order.

---

## 5. Execution Phase: Implementation Within Authorized Scope

### Phase Goal

To complete the implementation objectives described in the Task Specification without introducing any new decisions.

### Participating Roles

- **Code Agent**: The sole subject of execution.
- Human Engineer: Does not participate.

### Input

- A single Task Specification.

### Core Activities

The Code Agent, according to the Task Specification:

- Chooses specific implementation paths.
- Fills in implementation details.
- Adjusts the implementation to meet the task completion criteria.

The execution phase allows for technical-level free choice but strictly prohibits any form of re-decision.

---

### Mental Model Analogy | Frontline Execution and Overstepping

In a military system, a frontline commander can choose attack routes based on terrain and the situation but has no right to change operational objectives or unilaterally expand the scale of action. Any "more reasonable-looking" temporary decision that exceeds the order's authorization is considered an act of overstepping authority. The "one-track-mindedness" of the execution phase is not a lack of capability, but a prerequisite for system stability.

---

## 6. Audit Phase: Consistency Check and Responsibility Traceability

### Phase Goal

To judge whether implementation results were **completed within the legitimate scope of authorization** and to clarify responsibility attribution for issues (if any).

### Participating Roles

- **Verification Agent**: Performs the audit.
- **Actor (Human Engineer)**: Final adjudication.

### Input

- Execution results.
- Task Specification.
- Original Design Document.

### Core Activities

The audit phase does not judge whether the implementation is "elegant"; it only answers the following questions:

- Does it satisfy the task completion criteria?
- Does it violate the authorization boundaries of the Task Specification?
- Did it implicitly change the original design decisions?

It should be clearly noted: tests are responsible for correctness, while audits are responsible for compliance.

---

### Mental Model Analogy | Discipline System and Responsibility Traceability

In a military system, the discipline system is not responsible for commanding combat, nor for optimizing tactics; it does only one thing: judging whether orders were violated. Once an act of overstepping is discovered, the problem must be pushed up to the command level, where the person who made the decision bears the responsibility for correction or accepts the consequences.

---

## 7. Responsibility Reclaim and Release

After the audit is completed, the process enters the responsibility reclaim point.

Only the Actor, as the bearer of responsibility, possesses the final confirmation and release rights.

Release signifies:

> **Within the current responsibility boundary, one engineering closed-loop has been completed.**

The release result can serve as a stable prerequisite for subsequent processes.

---

## 8. Recursive Structure: How the Process Expands to Engineering Scale

The engineering process of Vibe + Coding is **naturally recursive**:

- Decisions frozen in the previous round
  → Become input constraints for the next round.
- Release results of the next round
  → Become established facts in the higher-level system.

---

## Chapter Summary

The engineering process of Vibe + Coding is a **responsibility closed-loop model centered on four phases**:

- Decisions happen centrally.
- Decomposition handles disambiguation.
- Execution is strictly limited.
- Audit clarifies responsibility attribution.

By introducing clear **mental model analogies** at critical structural nodes, we are not "beautifying" the process, but rather explaining that:
**These engineering constraints are not arbitrary choices, but the inevitable results of long-term evolution in all high-reliability systems.**
