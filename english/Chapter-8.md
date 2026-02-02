© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.2

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
