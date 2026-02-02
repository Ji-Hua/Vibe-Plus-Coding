© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.2

# Chapter I | The True Problem with AI Coding: When Decision and Responsibility Are Misaligned

Before discussing any processes, templates, or "best practices," we must first establish an **engineering axiom** that does not change with technological progress:

**In any real software engineering, decision-making and responsibility are inseparable.**
Whoever makes a critical judgment must bear the long-term consequences of that judgment across the dimension of time.

This does not depend on how advanced the tools are, nor on how efficient the execution is. It is the prerequisite for an engineering system to exist long-term.

---

## Starting from an Axiom

Once we acknowledge that "responsibility cannot be outsourced," we must face a direct and uncomfortable corollary:

> **Any role that does not bear the engineering consequences lacks the legitimacy to hold final decision-making power in high-responsibility judgments.**

This is precisely the core contradiction of current AI Coding—
**AI cannot bear engineering responsibility, yet it is involved in engineering decisions by default.**

Or simply:
**AI is "with great power but zero responsibility".**

The instability of most AI Coding in real engineering stems not from a lack of model capability, but from this structural mismatch.

---

## Why Improved Capability Cannot Solve This Problem

Current discussions regarding AI programming focus almost entirely on the capability level:

- Is the model smart enough?
- Is the context window long enough?
- Is the prompt sophisticated enough?

But even if we assume an idealized premise—that AI has infinite context, fully understands requirements, and can generate near-perfect code—it still fails to solve a fundamental problem:

**AI cannot bear responsibility for engineering outcomes.**

In real engineering, the consequences of architectural errors, technical debt, maintenance costs, and collaboration failures are ultimately borne by humans. As long as responsibility cannot be outsourced, final decision-making power cannot be fully outsourced.

Capability can be outsourced,
Judgment can be assisted,
But responsibility can never be transferred.

---

## 0 → 1 vs. 1 → 100: The Fracture in Responsibility Structure

The reason this contradiction is often ignored in practice is that people confuse two stages with completely different responsibility structures.

Current mainstream AI Coding performs exceptionally well in **0 → 1** scenarios: quickly turning an idea into a running demo, a small tool, or a one-off script.

At this stage:

- Decision consequences are short-lived.
- Things can be torn down and rebuilt.
- There are almost no long-term maintenance obligations.

Therefore, even if AI implicitly makes certain judgments during implementation, it does not immediately trigger structural problems.

But real software engineering does not stop there. What is truly difficult—and truly important—is **1 → 100**:

- Will the code still be readable months later?
- Can the abstractions withstand change?
- Can the system be handed over to others?
- Are historical judgments traceable?
- Are errors localizable and repairable?

At this stage, every critical judgment continuously generates consequences across time. This is not just an increase in engineering "complexity," but a **qualitative change in the responsibility structure**.

---

## It Is the Collaboration Paradigm That Fails, Not the AI

This is precisely why many senior engineers maintain a cautious attitude toward AI Coding.

They do not deny the capability of AI, but rather naturally guard against the quiet destruction of the responsibility system.

Current mainstream AI Coding carries an assumption that has almost never been systematically scrutinized:

> **Humans are responsible for raising requirements; AI is responsible for completing them on their behalf.**

The result is—
Humans make requests, while AI **makes substitutive judgments** during the implementation process.

In high-responsibility engineering, this mode inevitably leads to:

- Judgments occurring quietly during the implementation phase.
- Design trade-offs not being explicitly expressed.
- Original intent being backward-molded by code details.
- Systems evolving continuously without clear frozen points.

Ultimately, what spins out of control is not whether the code "runs," but the fact that the system is being reshaped by an execution body that bears no responsibility, without anyone noticing.

To make matters worse, under the mainstream AI collaboration model, while humans gain the "relaxed experience of chatting," they fall into the trap of frequent mental role-switching:

One moment you must be a Product Manager proposing requirements, the next you switch to a Senior Engineer deciding on architecture, and then you must act as a Quality Assurance Engineer rigorously auditing code.

Human engineers are forced to make high-frequency decisions across completely different cognitive scales. This type of collaboration, lacking structural constraints, not only fails to precipitate effective engineering judgments but instead leaves engineers exhausted in the process of being "backward-molded by code."

---

## Stronger AI Will Only Amplify This Problem

What is even more alarming is that smarter AI does not solve this problem; it may amplify the risks.

The stronger the AI,
The easier it is for it to choose structures that "look better" during implementation.
The easier it is for it to make unconfirmed trade-offs locally.
The easier it is for it to make implicit balances between short-term efficiency and long-term responsibility on your behalf.

These behaviors may increase output speed in the short term, but they simultaneously blur judgment boundaries, hide responsibility attribution, and make the system's evolution path uncontrollable.

And AI can never bear the long-term consequences of these judgments.

---

## This Is a Governance Problem, Not a Technical One

This misalignment of responsibility is not unique to AI programming. It almost perfectly replicates the governance failure models that have been repeatedly verified in human organizations.

In any mature organization,
The distribution of decision-making power is never based on the ceiling of capability, but on **whether the consequences of failure still fall within the boundary of responsibility.**

A role that does not bear long-term consequences, even if it is "more likely to be correct" in a statistical sense, should not be granted final discretionary power over high-responsibility judgments.

The world of engineering is not special, and AI is no exception.

---

## The Essence of the Problem and the Way Out

Therefore, the instability of AI Coding today is not because AI is not strong enough, but because we allow an execution body that bears no responsibility to **participate in high-responsibility judgments in 1 → 100 engineering**.

This is an error at the level of collaboration structure, not a problem that can be solved with a better model.

The direction for a solution thus becomes clear:

> **It is not about limiting the capability of AI, but about re-aligning the attribution of decision-making power and responsibility.**

As long as AI does not bear engineering consequences, its power of judgment must be restricted to a range matching its responsibility; whereas judgments that truly affect the long-term evolution of the system must be made by the party capable of bearing the consequences.

---

# Chapter II | From Problem to Solution: A Collaborative Structure Converging Under Engineering Constraints

In Chapter I, we accomplished one critical thing:

We stopped discussing "whether AI can write good code" and instead repositioned the issue as a more fundamental and stable engineering problem—

Under the premise of AI participating in software engineering, how can a responsibility system be structurally sound?

If the engineering axiom that "decision and responsibility are inseparable" holds true, then the question is no longer "whether to use AI," but necessarily:

Under what collaborative structure can AI be used so that the engineering does not spin out of control on a 1 → 100 time scale?

This means any viable solution must first satisfy a set of unavoidable engineering constraints.

---

## 1. Engineering the Problem: Three Questions Every Solution Must Answer

In any engineering system, the so-called "responsibility problem" is not an abstract moral discussion; it can be reduced to three specific, verifiable questions:

- Who owns the decision-making power?
- At what stage does the decision occur?
- Who bears the consequences of a failed decision?

If these three questions cannot be explicitly answered, then so-called "collaborative processes" and "best practices" can only rely on individual self-discipline and cannot form stable, reproducible engineering constraints.

This is precisely the core issue with traditional AI Coding:

These three questions are never explicitly answered, yet they are implicitly resolved, repeatedly modified, and mutually overwritten during the implementation process.

---

## 2. Additional Engineering Constraints: Not All "Correct" Solutions Are Viable

Up to this point, we have merely confirmed one thing:

High-responsibility decisions cannot occur at the wrong stage by the wrong entity.

However, this conclusion alone is not enough to constitute a usable engineering solution.

In real engineering, even if a solution is logically correct, it cannot stand long-term if it violates engineering reality or human ways of working. Therefore, before proceeding with the derivation, we must introduce a set of additional engineering constraints to limit the viable solution space.

These constraints are not idealized goals, but prerequisites that any implementable plan must satisfy simultaneously.

---

### Constraint 1: AI Must Be Included

We are not discussing a regression to traditional development methods.

The solution must be predicated on built-in AI collaboration, rather than evading the problem by not using AI. Any plan that requires engineers to re-assume all implementation, analysis, and execution work is outside the scope of discussion.

---

### Constraint 2: Humans Must Be Relaxed

The solution cannot achieve stability by shifting the mental burden back onto the human engineer.

If a plan requires engineers to remain in a long-term state of highly formalized, process-heavy, and document-heavy work, it will be equally unsustainable in reality.

In other words, engineering stability cannot come at the cost of sacrificing the engineer's convenience. If introducing this solution does not significantly reduce the engineer's mental burden during the implementation phase, then the solution itself does not hold.

---

### Constraint 3: Important Decisions Must Be Made by Humans

All high-responsibility judgments that could lead to long-term structural consequences must be completed by the human engineer who bears those consequences.

No AI should be allowed to make such judgments without constraints.

---

### Constraint 4: AI Is Allowed to Make Decisions, But Cannot Overrule Human Decisions

The solution cannot gain safety by prohibiting AI decisions.

AI should be allowed to make a large number of decisions within low-responsibility spaces to liberate human engineers; however, the decisions already made by human engineers must not be influenced, modified, or implicitly overturned by the subsequent actions of the AI.

---

### Constraint 5: AI Decision Risks Must Be Controllable

The discretionary freedom possessed by AI during the execution process must be explicitly limited within an auditable and traceable range.

Any decision-making behavior where the discretionary boundary cannot be defined and where it cannot be determined if it has exceeded its authority is unacceptable.

---

### Constraint 6: The Solution Must Be Domain-Agnostic

This collaborative structure should not apply only to a specific class of problem domains or technology types.

As long as a problem contains judgments that require long-term consequences to be borne, this structure should be applicable.

Whether to enable this solution is determined by the human engineer based on the nature of the problem; however, once enabled, the logic of responsibility division, decision freezing, and authorization auditing should not change with the problem domain, technology stack, or form of implementation.

---

## 3. From Constraints to Solution

Under the constraints above, we can gradually converge the space of viable solutions.

First, any programming method without AI participation is directly excluded.

Second, according to Constraint 4—that AI decisions cannot backwardly influence human decisions—we can find that this requirement is structurally consistent with the **Dependency Inversion Principle** in software engineering:

High-level decisions should not depend on low-level implementations; they must be isolated through stable interfaces, with both parties depending on that interface.

Here, this interface cannot be code, nor can it be a dialogue state; it must be an explicit, freezable, and auditable engineering artifact.

---

### Externalization of the Decision Interface

A natural and necessary choice is:

**Externalize critical decisions made by human engineers into documentation, and use that documentation as the sole decision interface between humans and AI.**

Dialogue is naturally low-entropy and diffuse. In a long conversation, early engineering constraints are often submerged by later implementation details. The essence of externalized documentation is "decision freezing"—by solidifying fluid dialogue into static documents, we artificially create a process of entropy reduction, ensuring the system's evolution path is always anchored to the initial engineering design. Using documentation prevents the Coding Agent from accessing the decision context, protecting it from noise pollution during the discussion process.

In engineering, documentation here is not a single form but two types of constraint carriers with a clear hierarchical relationship:

**1. Design Document**
Used to constrain the human engineer themselves, answering:
*What do I want, and what will I not allow to happen?*

This document carries all high-responsibility judgments and long-term structural decisions; it is the human engineer's commitment to the system's future.

**2. Task Specification**
Used to constrain the Coding Agent, answering:
*What should you do, and what must you absolutely not do?*

This document is derived from the Design Document and is a specific authorization of execution behavior.

Between these two types of documents, there is a clear and irreversible hierarchy of authority:

**The authority of the Design Document is higher than that of the Task Specification.**

- The Task Specification can only refine and decompose decisions already frozen in the Design Document.
- It must not introduce new design judgments.
- It must not weaken or modify the constraints already clarified in the Design Document.

When any inconsistency arises between the two, the Design Document always prevails.

The Coding Agent can only execute based on the Task Specification; any behavior not explicitly authorized by the Task Specification, even if it could be inferred from the Design Document, is considered an unauthorized action during the execution phase.

Through this layered structure, human decisions, execution authorizations, and AI behavior boundaries are explicitly distinguished and permanently locked.

---

### Vibe Writing: Completing Decision Freezing Without Increasing Burden

In the stages involving human engineers, we still allow AI to exist as a cognitive amplifier.

Human engineers can clarify requirements, explore plans, and compare trade-offs through natural language discussions with AI. This process maintains the ease of "Vibe Coding."

**However, the output of this stage is no longer code, but documentation.**

This process can be called **Vibe Writing**.

It must be emphasized that the documentation here is not a specification that exhausts every implementation detail, but rather the minimal externalized set of human high-responsibility judgments.

---

### Execution and Audit: Efficient Implementation Under Restricted Freedom

After the Design Document is frozen, the Vibe Agent decomposes it into a set of standardized Task Specifications.

Each Task Specification must clarify:

- Task goals.
- Task scope (including explicit prohibitions).
- Allowed discretionary space.
- Completion criteria and acceptance conditions.

The Coding Agent executes the implementation within the authorized space defined by the Task Specification:

- Possessing discretionary power within the scope.
- Maintaining necessary ignorance of anything outside the scope.
- Stopping execution and returning results immediately upon meeting acceptance criteria.

**Necessary ignorance of the global context is the core protection mechanism of this structure.** If the Coding Agent has permission to modify the global state, it will destroy global consistency for the sake of "convenience" while implementing local functions. The Task Specification is not just an authorization; it is an isolation wall.

The implementation results of the Coding Agent will be submitted to an independent **Audit Agent** for verification.

The responsibility of the Audit Agent is strictly limited to:

- Verifying if the implementation complies with the Task Specification.
- Judging if there are any boundary-crossing behaviors.
- Marking the locations of discrepancies and reasons for failure.

The Audit Agent must not introduce new implementation or design judgments, nor should it repair the code.

---

### Recursive Structure and Sole Return Path

When an audit fails, only the following return paths are allowed:

- If the task description is unclear or self-contradictory, return to the **Design Phase**, where the human engineer revises the documentation.
- If the task is clear but implementation failed, return to the **Coding Agent** for re-execution.

There are no paths for cross-layer patching or "fixing things along the way."

The entire process proceeds recursively in this manner.

---

## 4. The Inevitable Form of the Solution

Based on the derivation above, we arrive at an inevitable form of the solution:

- Human engineers complete high-responsibility decisions through discussion with AI (Vibe Agent).
- Decisions are externalized as Design Documents and frozen.
- Design Documents are decomposed into Task Specifications as the sole authorization for execution.
- AI (Coding Agent) executes implementation within the authorized space.
- Execution results are verified through independent auditing of boundaries.
- All failures can only return to their respective responsibility levels.

This set of solutions is called **Vibe + Coding**.

Its core shift lies in:

**Turning Vibe Coding into Vibe Writing + AI Coding.**

- In the **Vibe phase**, the output consists of decisions and constraints, not code.
- In the **Coding phase**, code is merely the result of the Task Specification being executed.

In this structure:

- Human engineers bear high-responsibility judgments and are responsible for long-term consequences.
- AI executes efficiently within explicitly authorized spaces.
- There is no backward pollution path between decision-making and execution.

---

## 5. Conclusion

Vibe + Coding is not a smarter way to use AI, but a collaborative structure derived under established engineering axioms and realistic constraints.

Its goal is not to make AI more powerful, but to ensure:

**High-level decisions are always made only by those who can bear the consequences, and are never backward-molded by low-level execution during the implementation phase.**

---

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

---

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

---

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

---

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

---

# Chapter VII | Execution Phase

## Consuming Frozen Semantics Under Established Authorization

After the Decomposition Phase ends, the engineering system already possesses a critical prerequisite:

**All high-responsibility judgments required for the execution phase have been completed and frozen.**

The execution phase no longer cares about:
- Whether the design is reasonable.
- Whether the decision is optimal.
- Whether the goal should be adjusted.

It cares only about one thing:

**How to transform established semantics into verifiable engineering reality without breaking authorization boundaries.**

The execution phase is not a continuation of design, nor a supplement to decision.

It is a **restricted, traceable, and fully auditable process of semantic consumption**.

Please note that in the Vibe + Coding paradigm, the Coding Agent and Vibe Agent are two different Agents; the sole path for communication between the two is documentation: Design Documents and Task Specifications. These two are not required to be in a specific form of isolation—it could be ChatGPT + Cursor, or different conversations within Copilot—but they must not share context. This method physically prevents noise from the design phase from penetrating the "veil of ignorance" and entering the execution phase.

---

## 1. The Engineering Status of the Execution Phase

In Vibe + Coding, the Execution Phase is strictly defined as:

**Completing a minimal, atomic, and verifiable engineering implementation within the authorization space defined by the Task Specification.**

In this phase:
- Introducing new design judgments is no longer allowed.
- Re-interpreting frozen semantics is no longer allowed.
- Modifying established boundaries in the name of "more reasonable implementation" is no longer allowed.

The legitimacy of the execution phase depends entirely on the artifacts of the Decomposition Phase. Once the execution entity begins work, it accepts by default the following facts:
- The goal is determined.
- Authority is assigned.
- Boundaries are frozen.
- Completion criteria are defined.

The execution phase has no right to question these premises.

---

### Mental Model Analogy | Orders Issued, Action Authorized

In a military system, once an operational order is issued and takes effect:
- Frontline units no longer discuss whether the strategy is correct.
- They no longer re-evaluate political goals.
- They no longer adjust operational purposes on their own.

Their sole responsibility is:
**To complete the action in the most reliable way within the range allowed by the order.**

The Execution Phase occupies this position.

---

## 2. The Sole Input for the Execution Phase

The execution phase accepts only one legitimate input:

**A confirmed, frozen, and auditable Task Specification.**

The execution entity must not:
- Trace the discussion process of the design phase.
- Rely on oral explanations or implicit background.
- Self-complete semantics based on historical implementations.

In the execution phase:
- Design Documents serve only as cited sources of authority.
- Task Specifications are the sole artifacts directly constraining execution behavior.

Any behavior not explicitly authorized in the Task Specification is defaulted as not permitted in engineering semantics.

---

## 3. The Restricted Action Loop of the Execution Entity

In Vibe + Coding, the work of the execution entity (including the Coding Agent) is limited to a clear, closed execution loop:

1.  Read and confirm the Task Specification.
2.  Based on the acceptance semantics defined in the Task Specification, prepare verification artifacts (usually tests).
3.  Run the verification artifacts and confirm their initial failure state.
4.  Write the minimal implementation to satisfy constraints.
5.  Re-run verification.
6.  Correct the implementation until all constraints are satisfied.

In this loop, the execution entity:
- Can choose specific implementation paths.
- Can make technical trade-offs within the allowed range.
- Can adjust code organization to satisfy established norms.

But is not allowed to:
- Modify Design Documents.
- Expand task scope.
- Introduce undeclared behaviors.
- Perform structural refactoring to "improve overall quality."

The success standard for the execution phase is singular:
**The implementation behavior fully satisfies the verifiable constraints defined in the Task Specification.**

---

## 4. Minimal Principle: The Sole Legitimate Strategy for Document Gray Zones

Even if the Decomposition Phase has tried its best to eliminate ambiguity, in real engineering, the execution entity may still encounter situations not explicitly covered by the Task Specification.

In the execution phase, these situations are collectively referred to as:

**Document Gray Zones.**

Facing a document gray zone, the execution phase is not allowed to introduce new design judgments. The only legitimate handling principle is:

**The Minimal Principle.**

The Minimal Principle means:
- Do not expand existing semantics.
- Do not introduce new long-term commitments.
- Do not increase irreversible structural complexity.
- Choose implementation methods with the smallest impact, which are replaceable and reversible.

The Minimal Principle is not "smart implementation"; it is a deliberate engineering posture of restraint.

---

### Mental Model Analogy | Maneuvering at Boundaries, Not Rewriting Orders

Frontline troops, during execution, **may enter areas not explicitly authorized by original orders under unavoidable circumstances**, for example, if original positions can no longer be deployed or advancement continued due to changes in weather, terrain, or environment.

In such cases, frontline troops can retreat, bypass, or temporarily occupy alternative positions to maintain continuity of action and complete established missions.

However, such behavior must simultaneously satisfy the following premises:
- The overreaching behavior must have the completion of the established mission as its sole purpose.
- The range of overreaching should be kept to the degree of smallest impact.
- All overreaching behaviors and their triggering reasons must be fully recorded for subsequent audit and responsibility adjudication.

What the Minimal Principle corresponds to is precisely this **restricted maneuvering that allows limited overreaching to prevent action interruption, but rejects implicit expansion of power**.

---

## 5. Overreaching Is a Reality, Not an Exception

Vibe + Coding does not assume that the execution phase is always correct.

On the contrary, it explicitly acknowledges:
**The occurrence of overreaching by the execution entity in document gray zones is an expected engineering reality.**

Therefore, the safety of the system does not depend on:
- The execution entity being cautious enough.
- The Agent being smart enough.
- The Prompt being perfect enough.

Rather, it depends on a more fundamental fact:
**Whether overreaching can be identified, and whether a clear return and adjudication mechanism exists.**

The execution phase itself is not responsible for adjudicating whether overreaching is legitimate; it is only responsible for leaving sufficiently clear traces for the subsequent audit phase to judge.

---

## 6. Implementation Report: Artifacts the Execution Phase Must Leave

After every execution task is completed, the execution entity must output an Implementation Report.

The Implementation Report is not summary text, but a record of execution that can be audited, explaining at least:
- Which task goals were covered by this implementation.
- How the implementation corresponds to constraints in the Task Specification.
- Whether document gray zones were encountered.
- Whether trade-offs under the Minimal Principle were made.

The existence of the Implementation Report ensures the execution phase:
- Is no longer a black box.
- Does not rely on the memory of the executor.
- Does not lose context due to changes in personnel or Agents.

---

## Execution Suspend Condition: An Implementation-Level Defense Mechanism

*This section provides implementation-level suggestions and does not constitute a necessary condition for the validity of the methodology.*

In some high-risk or highly uncertain engineering environments, a set of Execution Suspend Conditions can be introduced for the execution entity to expose problems early.

Typical suspension triggering scenarios include:
- Constraints in the Task Specification are mutually conflicting in engineering.
- Multiple implementation paths involve obvious design-related trade-offs.
- Verification artifacts cannot express critical frozen semantics.

When a suspend condition is triggered, the execution entity should:
- Stop further implementation.
- Explicitly record the reason for triggering.
- Toss the problem upward for handling in subsequent phases.

It must be emphasized that:
**Execution suspension is not for protecting the execution entity, but to avoid implicitly assuming design responsibility during the execution phase.**

---

## 7. Conditions for Ending the Execution Phase

The end of the execution phase is not marked by the code being finished.

It must simultaneously satisfy:
- All verification artifacts have passed.
- An Implementation Report has been generated.
- All execution behaviors can be traced back to authorized items in the Task Specification.

Once these conditions hold, the execution phase ends, and the system enters the next phase.

---

## Chapter Summary

The Execution Phase is not a space for exercising creativity, but a phase for restricted action, controlled consumption, and waiting for audit.

In this phase:
- Decisions are complete.
- Authorization is clear.
- Actions are strictly constrained.
- Overreaching is allowed to occur but must not be concealed.

Through this design:
- Execution can be safely outsourced.
- Design sovereignty remains in the hands of the human engineer.
- The engineering system can maintain structural stability during long-term evolution.

**The value of execution lies not in being smart, but in being controllable.**

---

# Chapter VIII | Audit Phase

## Re-introducing Judgment After Execution Ends

In Vibe + Coding, **the Audit Phase is the only phase authorized to re-introduce high-responsibility judgment after the execution phase.**

Before entering the Audit Phase, one prerequisite must be clarified:

> **Execution has ended; the execution entity no longer possesses any right to act.**

The Audit Phase no longer modifies code, no longer supplements implementations, and no longer continues "getting things done."

It does only one thing:

**Judging whether the execution behaviors that have already occurred fall within the established authorization boundaries.**

---

## 1. The Engineering Status of the Audit Phase

The position of the Audit Phase in the engineering process is clear and irreplaceable.

It is not an extension of the execution phase, nor the start of the next execution loop, but a **phase for responsibility recovery and boundary calibration**.

In this phase:
- Adjudicatory power returns to the high-responsibility role.
- The execution entity's right of interpretation is strictly limited.
- Whether a result is "good" or "bad" does not constitute a basis for legitimacy.

The core question of the Audit Phase is not:
"Is this right?"
But rather:
> **"Was this authorized?"**

---

### Mental Model Analogy | Post-War Evaluation, Not On-Site Command

### Mental Model Analogy | Military Discipline Review, Not Battlefield Command

In a military system, the end of combat does not mean everything is automatically legitimate.

What truly determines whether an action is recognized is not the judgment of the frontline, but the **military discipline and order review** that follows.

In this phase:
- No new operational orders are issued.
- No tactical deployments are adjusted.
- There is no discussion of whether things were "more reasonable" at the time.

The review is based on only three things:
- Established operational orders.
- Authorization boundaries clarified beforehand.
- Action records left during combat.

The core question of the evaluation is not:
"Would it have been better to use a different tactic then?"
But rather:
**"Were these actions performed within the established orders and authorizations?"**

The Audit Phase corresponds to this role: it is not about continuing to command actions, but about adjudicating whether actions complied with the established discipline and command system.

---

## 2. The Sole Goal of the Audit Phase

The goal of the Audit Phase can be precisely expressed as:

> **Making a clear adjudication on the legitimacy of execution behaviors based on established authorization documents and execution records.**

It does not pursue the "optimal engineering solution," nor is it responsible for "making the system better."

It is responsible for only three things:
- Confirming which behaviors are legitimate.
- Identifying which behaviors touched gray zones.
- Clarifying which behaviors constitute overreaching.

And providing a **clear, unambiguous adjudication result** for subsequent processes.

---

## 3. Audit Input Artifacts: The Sole Factual Basis for Adjudication

The Audit Phase does not "understand the system," nor does it "reconstruct the execution process."

It does only one thing:

**Judging whether execution behaviors were authorized based on a set of explicitly permitted engineering artifacts.**

Therefore, in Vibe + Coding, **the first principle of the Audit Phase is not how to judge, but: what things can be used for judgment.**

Any material not included in the scope of audit input artifacts, regardless of how reasonable it seems or how much it "helps understand the background," must be treated as non-existent in engineering semantics.

---

### 3.1 The Freezing Principle for Audit Inputs

The Audit Phase accepts only artifacts that already existed at the end of the execution phase.

During the audit process:
- Supplementing new explanatory materials is not permitted.
- Introducing post-hoc "understandings" is not permitted.
- Backward-inferring execution intent based on results is not permitted.

Audit judgment is based only on factual records left at the time, not on post-hoc narratives.

If a behavior did not leave an auditable trace during the execution phase, it is unprovable in audit semantics.

---

### 3.2 Core Audit Input Artifact List

The Audit Phase must, and is only permitted to, use the following artifacts as a basis for judgment.

#### 3.2.1 Frozen Design Documents
The frozen Design Document defines:
- The semantic boundaries of the system.
- Module responsibilities and invariants.
- Completed and frozen high-responsibility judgments.

In the audit phase:
- Design Documents are the highest semantic authority.
- They are used to judge whether a certain class of behavior is permitted to exist in principle.

The audit does not evaluate whether the design is reasonable; it only evaluates if the design was followed.

---

#### 3.2.2 Corresponding Version of Task Specifications
The Task Specification is the direct authorization for the execution phase.

It defines:
- The scope permitted to be touched for this task.
- Engineering facts explicitly frozen.
- Acceptance and completion criteria.

In the audit phase, the Task Specification is used to judge:
- Whether a specific behavior was explicitly authorized.
- Whether a trade-off still falls within the authorization space.

Any behavior that is neither authorized nor classifiable as a necessary trade-off under the Minimal Principle will be treated as a candidate for overreaching.

---

#### 3.2.3 Implementation Code and Verification Results
Implementation code and test results serve to answer:
**What the execution entity actually did.**

They are not sources of authority, nor do they hold adjudicatory status.

Whether code is elegant or if tests all passed does not itself constitute proof of legitimacy; they are merely evidence of behaviors that occurred.

---

#### 3.2.4 Implementation Report (Execution Report)
The Implementation Report is an explanatory artifact that the execution phase must leave behind.

It is used to:
- Mark the correspondence between implementation behaviors and authorized items.
- Clarify if document gray zones were touched.
- Explain if trade-offs under the Minimal Principle were adopted.

In the audit phase, the Implementation Report is not a defense plea, but a structural labeling of the execution entity's own behaviors.

---

#### 3.2.5 Records and Labels Generated during the Execution Phase
Including but not limited to:
- Gray zone trigger records.
- Execution suspension labels.
- Explicitly declared overreaching behaviors and their reasons.

The value of these records lies not in whether the explanation is sufficient, but in whether the occurrence of overreaching was acknowledged and explicitly exposed.

Overreaching that was not recorded is treated as implicit expansion of power in audit semantics.

---

### 3.3 Explicitly Excluded Non-Audit Inputs

The following content is explicitly prohibited from serving as a basis for audit:
- Subjective intent of the execution entity.
- Oral or temporary explanations.
- Result-oriented defenses of reasonableness.
- Post-hoc design understandings.
- Unfrozen drafts or intermediate documents.

These contents may be "helpful" in engineering, but are unacceptable in the responsibility structure.

---

### 3.4 Default Adjudication Stance when Input Artifacts are Incomplete

When audit input artifacts are missing, vague, or cannot be aligned, the Audit Phase adopts:

**The Principle of Interpretation Against the Execution Entity.**

This is not a punishment, but a structural constraint used to encourage leaving sufficient traces during the execution phase and to prevent evading adjudication through post-hoc explanations.

---

## 4. Adjudication Questions Addressed by Audit

The Audit Phase focuses not on whether the task was completed, but on the following questions:
- Did implementation behaviors fall within authorization boundaries?
- Were there Minimal Principle executions under gray zones?
- Was there unrecorded or undeclared implicit expansion of power?

Audit conclusions must be explicitly categorized as:
- Legitimate execution.
- Gray zone but acceptable.
- Explicit overreaching.

There is no legitimate state of "not processing for now."

---

## 5. Sole Legitimate Handling Paths after Adjudication

When an audit discovers an issue, only two handling results are permitted:

**1. Tightening Authorization**
- Judging the behavior as unauthorized.
- Requiring backtracking or rewriting implementation.

**2. Explicit Delegation of Power**
- Confirming the behavior is acceptable.
- Writing the originally implicit freedom into documentation.
- Re-freezing authorization boundaries.

The Audit Phase does not assign blame; it only performs demarcation.

---

### Mental Model Analogy | Not Punishment, but Boundary Correction
Auditing is not meant to negate execution, but to prevent the system from expanding power unconsciously.

---

## 6. Audit Results as Engineering Artifacts

The Audit Phase must produce formal Audit Result artifacts, explicitly recording:
- Adjudication conclusions.
- Input artifacts relied upon.
- Whether document revision was triggered.
- Impact on subsequent processes.

Audit results will directly affect:
- Whether subsequent decomposition is legitimate.
- Whether execution needs to be rolled back.
- Whether the system authorization boundary has changed.

---

## Chapter Summary

The Audit Phase is not meant to make the system "smarter," but to keep the system **from spinning out of control**.

By freezing audit inputs, limiting adjudication basis, and forcing overreaching to be made explicit:
- Execution no longer relies on trust.
- Judgment no longer relies on memory.
- System evolution no longer relies on fluke.

**The power of auditing comes from its refusal to understand any reasonableness that was not recorded.**
