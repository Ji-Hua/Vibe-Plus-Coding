© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.2

# Chapter III | Roles and Mental Models: A War of Software Engineering

In the previous two chapters, we established the structural principles of Vibe + Coding:

- Decision and responsibility are inseparable.
- High-responsibility decisions must be completed by the party bearing the responsibility.
- AI can only act within explicitly authorized responsibility spaces.

But even if the structure itself is correct, engineering can still fail. The reason is often singular:

**Humans have not truly stepped into the position required by this structure.**

The key to understanding Vibe + Coding is not learning "how to use AI better," but completing a **fundamental shift in role perception**.

The most effective way is to understand a software engineering project as a **long-term war**.

---

## 3.1 A War, Not a Conversation

In Vibe + Coding:

- A software engineering project is a long-term war.
- Every complete Design-Execution cycle is a battle.
- Every code modification is a specific tactical action.

The goal of the war is not:

- To write code as quickly as possible.
- To obtain a result that "looks usable."

But rather:

**To continuously maintain the stability of system structure and semantics during the long-term process of countering complexity, uncertainty, and evolutionary pressure.**

If you still understand AI programming as:

- Asking a question.
- Getting a reply.
- Continuing to ask questions.

Then you are actually using the mental model of a "chat system" to attempt to command a war.

The result is almost inevitably a breakdown in command.

---

## 3.2 Your True Role: Supreme Commander, Not Frontline Lead

In this war, you are not:

- A tool user.
- A prompt debugger.
- A direct executor of code.

The position you occupy is:

**Supreme Commander**

This means you are responsible not for "how to write code," but for:

- Whether this war is worth fighting.
- What problem the target system aims to solve.
- Which complexities must be endured.
- Which risks are unacceptable.

What you truly bear are:

**The full consequences of the system over the coming months and even years.**

Therefore, your core responsibility is not "giving smarter instructions," but:

- Clarifying war objectives.
- Freezing irreversible decisions.
- Clarifying which issues are not allowed to be re-discussed during the execution phase.

If a battle fails, the responsibility lies not with the execution unit, but with:

**Whether the strategic level made clear, transmissible, and constrained determinations.**

At the same time, this role positioning does not change with rank or task size; it is naturally recursive.

A General is the Supreme Commander to a Colonel, but he must still obey the strategy of the Army Group; a Squad Leader, though subordinate to a Captain, is the sole Supreme Commander with final say over his small patch of ground.

The same is true in software engineering: whether you are refactoring an entire payment middle-platform or optimizing a string processing function, as long as you bear the consequences within that scope, you are the Supreme Commander of that scope. Power and responsibility are equivalent at every scale.

---

## 3.3 Vibe Agent: The Staff System, Not the Command System

The role of the Vibe Agent in this war is:

**General Staff (The Staff System)**

Its responsibilities are:

- Analyzing problems.
- Projecting plans.
- Revealing implicit assumptions.
- Comparing the consequences of different decision paths.

Its purpose is to enhance your judgment capability, not to replace your judgment responsibility.

Therefore, it never possesses:

- Decision-making power.
- Authorization power.
- Risk-acceptance power.

The Staff can propose ten plans, but even if only one sentence is adopted, the responsibility remains entirely with the Commander.

Once you mentally outsource "judging correctness" to the Vibe Agent, you are effectively allowing the Staff to initiate war on its own.

In any real military system, this is a structural disaster.

---

## 3.4 Design Document: Commander’s Intent

In a real war, the Supreme Commander does not control all troops through endless orders.

He issues a:

**Commander’s Intent**

It clarifies not "how to execute," but:

- The desired end-state of the battle.
- Principles that must not be violated.
- Known risks and boundaries of acceptance.

In Vibe + Coding, the Design Document fulfills this role.

It describes:

**The structural and semantic state the system should present when this round of battle concludes.**

This is why:

- The Design Document is a high-responsibility artifact.
- It must be frozen.
- It must become the sole superior basis for all subsequent judgments.

Once the battle intent is frozen, no execution unit has the right to re-interpret the war objectives.

---

## 3.5 The Staff System’s Second Responsibility: From Battle Intent to Executable Tasks

In a real military system, the Staff's responsibility does not end at "giving suggestions."

Once the battle intent is clear and frozen, the Staff system must also undertake a critical responsibility:

**Translating the Commander's intent into a task structure that the execution system can understand.**

This step is not the decision itself, but the engineering expression of the decision.

In war, this usually manifests as:

- Draft operational plans.
- Division of phase objectives.
- Unit responsibility and boundary descriptions.
- Synergistic interfaces and dependency relationships.

All of this is drafted by the Staff system but, under no circumstances, constitutes an order until formally approved by the Commander.

---

## Correspondences in Vibe + Coding

In Vibe + Coding, this responsibility is borne by the Vibe Agent.

Its job is not to issue instructions directly to the Coding Agent, but to:

**Decompose the frozen Design Document into a set of clear, executable, and non-overreaching Task Specification drafts.**

These Task Specifications serve to clarify:

- What this task solves.
- What it does not solve.
- Which design conclusions are frozen.
- Which judgments are still allowed for free choice at the execution level.

Its core purpose is singular:

**To prevent the tactical execution phase from being forced to re-think strategic issues.**

---

## A Key Principle: Staff Is Responsible for Executability, Not Correctness

When decomposing tasks, the Vibe Agent does not focus on:

- Whether the battle intent is "correct."

But rather:

- Whether it is clear enough.
- Whether there is ambiguity.
- Whether it can be safely delegated.

If a problem is found, the Staff system should not arbitrarily "correct" the intent; instead, it should push the issue back up to the command level to wait for new, explicit authorization.

The Staff does not correct strategy; it only exposes the incompleteness of strategy.

---

## 3.6 Task Specification: Formal Action Authorization Document

In Vibe + Coding:

- The Design Document is the Commander’s Intent.
- The Task Specification is the formal authorization organized by the Staff system.

It explicitly defines:

- What is allowed to happen.
- What is not allowed to happen.
- When it is considered complete.

The Coding Agent receives not "your thoughts," but a formal authorization that is auditable, traceable, and cannot be interpreted at will.

---

## 3.7 Coding Agent: The Constrained Tactical Commander

The Coding Agent is the authorized Tactical Commander.

It can:

- Decide on specific implementation paths.
- Handle technical details.
- Make judgments within a local scope.

But it must never:

- Modify war objectives.
- Re-interpret design semantics.
- Expand the scope of the battle.
- Introduce unauthorized structural changes.

Once you expect the Coding Agent to "help you think about whether the strategy needs adjustment," in a military sense, this is equivalent to:

**Letting the frontline commander decide the direction of the war.**

---

## 3.8 Verification / Audit: Military Discipline and Responsibility Traceability System

No long-term war can rely on self-discipline.

Therefore, there must exist:

**Verification / Audit Agent — The Military Discipline System.**

It does not judge whether something is "smart"; it only judges whether authority was exceeded.

The highest basis for the audit is always the Design Document.

---

## 3.9 The True Meaning of "Overstepping"

Overstepping is not a mistake.

Overstepping is:

**Crossing responsibility levels.**

When overstepping occurs, the problem is not in the code, but in the fact that high-responsibility decisions were not correctly frozen or were erroneously delegated.

---

## 3.10 The Sole Direction of the Command Chain

You (Strategic Commander)
↓
Battle Intent (Design Document)
↓
Staff Decomposition (Vibe Agent)
↓
Action Authorization (Task Specification)
↓
Tactical Execution (Code)

Responsibility can only be authorized from the top down; problems can only be traced from the bottom up.

---

## 3.11 The Essence of the New AI Collaboration Paradigm

In the new AI engineering paradigm, what we truly need is not:

- An AI that makes decisions for you.
- An AI that initiates battles for you.
- A "smart-looking" all-powerful agent.

What we truly need is:

- **An increasingly smart Staff system proficient in analysis and decomposition.**
- **A "one-track-minded" frontline commander who is highly restrained and strictly follows authorization boundaries during the execution phase.**

The Staff can be extremely smart, propose endless possibilities, and constantly challenge your cognitive boundaries.

But once the determination is frozen and orders are issued:

**The execution system must be dull, restrained, and loyal.**

It does not think about whether a strategy is "better"; it does not judge if a goal is "worth it"; it does not arbitrarily escalate the war because something "looks better."

In any high-reliability system:

**Intelligence must be concentrated before the decision, while execution must happen after the decision.**

This is precisely the engineering order that Vibe + Coding seeks to restore.

---

## 3.12 Chapter Summary

In Vibe + Coding:

- Software engineering is a long-term war.
- You are the sole Strategic Commander.
- Vibe Agent is an increasingly smart Staff system.
- Coding Agent is a "one-track-minded" Tactical Commander for the execution phase.
- Design Document is the Battle Intent.
- Task Specification is the Formal Authorization.
- Audit system is responsible for military discipline and responsibility traceability.

When you truly stand in this position, you no longer expect AI to "think everything through" for you.

Instead:

**Command intelligence to serve you within a strictly constrained system.**
