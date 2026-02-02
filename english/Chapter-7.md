© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.2

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
