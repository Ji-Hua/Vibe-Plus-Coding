© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.2

# The VPC Principle for AI-native Engineering

Coding **is** decision-making.

Choosing a function name is a decision. Designing a schema is a decision. Defining a system architecture is a decision.
They differ not in kind, but in **weight** and **consequence**.

In any robust system, decision authority must match responsibility.
Anything else is structural negligence.

AI can bear only limited responsibility; therefore, it should be confined to low-impact decisions.
Yet in today’s AI coding paradigm, we routinely outsource high-impact decisions to it.

This is not a capability failure.
It is a **governance failure**—a structural mismatch between decision authority and responsibility.

This problem cannot be solved by “smarter” AI.
On the contrary, more capable models only make it worse: they make **implicit, high-impact decisions** more frequently, more convincingly, and more invisibly.

The solution is not to elevate AI to a “co-pilot.”
The solution is to **bind it**.

AI must be treated as a constrained component, operating under an explicit constitution.

We must state—clearly and non-negotiably—which decisions belong to humans, which decisions may be delegated, and which decisions, once made by humans, **must never be weakened, reinterpreted, or eroded** by AI execution.

Hence, the VPC Principle:

**Verdict. Permission. Boundary Control.**

---

## V (Verdict)

Verdicts are high-level, high-responsibility decisions.
They are the constitutional laws of the system.

Only humans may issue or modify a Verdict.
AI is strictly forbidden from reinterpreting, softening, or overriding it.

---

## P (Permission)

Permission defines the operational envelope.

Humans define the decision space within which AI may operate.
Inside this space, AI may optimize and implement freely.
Outside it, AI has no authority.

---

## C (Boundary Control)

Boundary Control is structural enforcement.

We do not ask whether the AI completed the task.
We ask whether it **stayed within the law**.

---

In engineering terms, this is a **dependency inversion of authority**:
human intent must never depend on AI implementation.
They are decoupled, connected only through Verdict and Permission.

---

## A Minimal Execution Loop

**Decision**
Humans issue the Verdict.
AI may advise, analyze, or challenge—but it does not decide.
The output is a binding blueprint.

**Decomposition**
The Verdict is translated into explicit Permissions.
This step defines not what the AI should do, but what it is **allowed** to do.

**Execution**
This is pure labor.
The agent executes strictly within the granted authority.

**Audit**
A dedicated mechanism verifies whether any Verdict or Permission has been violated.

---

## The Failure Rule

If the Audit fails, the developer must not patch the code.

Only two remedies exist:

1. Rewrite the Verdict—because the constitution was ambiguous.
2. Rewrite the Permission—because the delegation was flawed.

All fixes are forced back to the legislative layer.

Through this pressure, the system converges toward stability, clarity, and human control.

---

The VPC Principle is not about creating a better prompt, a new workflow, or a more capable coding agent.
It asserts something more fundamental:

In the AI era, engineers do not write code.
They write the laws under which code is allowed to exist.
