© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.2

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
