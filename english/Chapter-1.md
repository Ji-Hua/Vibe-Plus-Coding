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
