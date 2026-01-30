# Vibe + Coding: A new AI coding workflow

# Introduction

Vibe Coding is a powerful tool.  
As an engineer who has spent many years working on system design and long-term maintenance, I am always eager to adopt any technology that can reduce implementation effort—and AI is undoubtedly one of the most promising.

However, after nearly a year of practical use, I gradually came to realize a fundamental problem:  
**AI cannot independently handle the implementation of medium- to large-scale systems.**  
Even in projects that are only moderately complex, it easily leads to structural breakdown, semantic drift, and long-term unmaintainability.

These problems rarely manifest as “the code doesn’t run.”  
Instead, they surface in the quality of the engineering itself, for example:

- Writing code unrelated to the design goals  
- Hardcoding behavior that should be passed through parameters or configuration  
- Randomly adding meaningless logs or debug output  
- Chaotic function interfaces with unclear responsibilities  
- Arbitrary extension of inheritance hierarchies without clear abstraction boundaries  
- Uncontrolled modification of project directory structures  
- Installing dependencies without constraints, introducing hidden complexity  

I tried more elaborate prompts, stricter instructions, and even step-by-step decomposition of agent behavior, but the results remained limited.  
Under this mode, AI is at best capable of simple, local, low-risk implementations; once task complexity increases, the entire project quickly spirals out of control.

The real turning point came during what seemed like an ordinary personal project.

At the time, I wanted to implement a board game as a web app. Unlike before, I first wrote a rule specification, then designed test cases based on those rules, and only afterward began implementation.  
At that moment, I suddenly realized something critical:  
**The problem was not that AI was insufficiently capable, but that I had been using it in the wrong way.**

As an engineer with more than a decade of experience, I cannot guarantee that every line of my own code is inherently correct.  
I also rely on documentation to clarify semantics, tests to constrain behavior, and structure to prevent system decay.  
So why should I expect AI to independently complete complex engineering tasks without any of these constraints?

AI’s strength does not lie in designing systems, but in precisely executing decisions that have already been made.  
Design, trade-offs, judgment, and ownership are precisely the core value of human engineers.  
In other words, project ownership must belong to humans, and decisions should not be outsourced to models.

Different engineers naturally write very different code—and AI is no exception.

After recognizing this, I consciously adjusted my workflow:  
First, I worked with AI to complete design documentation and then froze decisions;  
Next, I wrote tests based on those documents;  
Finally, I let AI perform constrained implementation, execution, fixes, and refactoring.

I applied this workflow to two projects of different scales, and both achieved my engineering expectations.  
At that point, I was confident that this was not an accidental success, but a reusable engineering paradigm.

I named this workflow **Vibe + Coding**.  
The design phase is Vibe, the implementation phase is Coding, and the two interact only through documentation.

This guide is a systematic organization and summary of that paradigm.

---

# Chapter 1｜Design Philosophy

In the introduction, I explained that Vibe + Coding is not an accidental trick, but the result of repeated failures and corrections in real engineering practice.  
The purpose of this chapter is to further clarify the **engineering stance and design assumptions** behind this paradigm.

---

## 0. What Is Vibe + Coding (A Clear and Executable Definition)

**Vibe + Coding is not a “smarter form of Vibe Coding.”  
It is a forced decomposition of traditional Vibe Coding into two strictly separated stages.**

These two stages are:

- **Vibe (Design Phase)**  
- **Coding (Implementation Phase)**  

Their relationship is not collaborative mixing, but **responsibility isolation**.

### The Vibe Phase (Design Phase)

The Vibe phase is responsible for only one thing:

> **Transforming the human engineer’s design intent into executable external structure.**

Its outputs include, but are not limited to:

- Design documents  
- Architecture descriptions  
- API specifications  
- Data structure definitions  
- Task specifications  
- Behavioral constraints  
- Test designs (or test intent)

In this phase:

- No implementation is pursued  
- Syntax details are ignored  
- “Writing a bit of code just to see” is not allowed  

The sole goal of the Vibe phase is to **freeze decisions and externalize them as documentation**.

---

### The Coding Phase (Implementation Phase)

The Coding phase is likewise responsible for only one thing:

> **Strictly implementing under existing documentation and tests.**

In this phase:

- Design is not re-discussed  
- No new implicit assumptions are introduced  
- No “structural optimizations” are made  
- No undocumented behavior is added  

The input to the Coding phase is documentation.  
The output is code.

---

### A Critical Constraint: No Shared Context

**Vibe and Coding must not share context.**

This is not a recommendation—it is a **necessary condition** for the paradigm to hold.

This means:

- All information from the Vibe phase must be transmitted through documents  
- The Coding phase must not rely on “previous conversations”  
- There is no implicit communication channel beyond documents and tests  

At the tooling level, this isolation can be enforced in multiple ways:

- Using different tools (e.g., ChatGPT for Vibe, Cursor or Copilot for Coding)  
- Using different sessions within the same tool  
- Using different agent instances with shared history explicitly disabled  

**If context is shared, Vibe + Coding degenerates back into old Vibe Coding.**

---

### One-Sentence Definition

> **Vibe + Coding =  
> Forcibly splitting Vibe Coding into two stages—  
> “design generates documents” and “code is implemented from documents”—  
> with strict responsibility separation and context isolation,  
> communicating only through documentation and tests.**

If you cannot do this, you are still practicing old Vibe Coding.

---

## 1. Two Fundamentally Different Programming Paradigms

### Vibe Coding (The Old Paradigm)

In this guide, **Vibe Coding** refers to the most common AI-assisted programming approach today:

- Continuous interaction with AI in a single conversation  
- Design, implementation, and debugging mixed together  
- AI simultaneously “understands the problem” and “writes the code”  
- Engineering continuity depends on implicit memory within the context window  

This approach works well for:

- Prototyping  
- One-off scripts  
- Small tools  
- Exploratory experiments  

But in medium- to large-scale systems, it systematically fails:

- Design intent drifts over time  
- Implementation details reverse-drive structure  
- Decisions are buried in code and become untraceable  
- When issues arise, it becomes hard to explain “why it is this way”  

This is not due to user carelessness or model weakness.  
It is because this mode **lacks engineering-grade stability**.

Unless otherwise stated, “Vibe Coding” in this guide always refers to this old paradigm.

---

### Vibe + Coding (The New Paradigm)

**Vibe + Coding is not an enhanced version of Vibe Coding.  
It is a structural decomposition of it.**

It forcibly separates the previously entangled process into two stages:

- **Vibe: design phase, producing documentation**  
- **Coding: implementation phase, executing against documentation**

Responsibilities are separated, context is isolated,  
and communication happens only through documents and tests.

Vibe + Coding does not focus on making AI smarter.  
Instead, it focuses on:

- Who is responsible for thinking  
- Who is responsible for execution  
- How decisions are frozen  
- How system semantics are preserved  

In this paradigm:

- The human engineer is always the project owner  
- AI does not participate in design judgment  
- AI exists purely as a **constrained execution role**

Once this separation is broken, the process inevitably collapses back into old Vibe Coding.

---

## 2. The Real Problem This Paradigm Solves

In real-world software development, engineers rarely spend most of their energy on the truly hard parts.

Instead, time is consumed by:

- Glue code  
- Repetitive structures  
- Boilerplate logic  
- Framework-driven scaffolding  
- Engineering noise unrelated to core design  

Meanwhile, the aspects that truly determine system quality and longevity—

- Architecture  
- Abstraction modeling  
- Interface boundaries  
- Invariant definitions  
- Long-term maintainability judgments  

—are often rushed through in fragmented time.

Vibe + Coding is not about “letting one person write more code.”  
It addresses a more realistic question:

> **How can engineers spend their limited cognitive resources on what is truly irreplaceable?**

Thus, its goal is not efficiency maximization, but:

> **Integrity of engineering responsibility.**

### No Silver Bullet

**Vibe + Coding was never meant to make programming easy.**

Programming is inherently difficult.  
Any narrative claiming that complex engineering can be solved simply by “writing better prompts” or “letting AI handle everything” is a misreading of engineering reality.

Vibe + Coding does not attempt to reduce thinking.  
It does one thing only:

> **Redistribute where, how, and by whom thinking occurs.**

---

## 3. A Reality That Must Be Faced: Context Is Fragile

At the current stage, all large language models share an unavoidable limitation:

**Context windows are finite and unstable.**

As task scale grows, this limitation systematically surfaces:

- Early design decisions are gradually forgotten  
- Implicit constraints between modules disappear  
- Implementations become “locally correct, globally wrong”  
- Root causes are hard to trace once problems appear  

Relying on “continuous conversational memory” for complex engineering is itself a high-risk assumption.

This is not a model problem.  
It is an **engineering assumption problem**.

---

## 4. The Core Assumption of Vibe + Coding

Vibe + Coding is built on a clear and restrained assumption:

> **AI is not suited to holding the full semantics of complex systems over long periods.**

Therefore, instead of asking AI to “remember the entire project,” we should change how engineering work is organized:

- Decompose complexity into independent subtasks  
- Provide each subtask with complete, closed, understandable specifications  
- Execute within controlled contexts  
- Preserve decisions through documentation and tests  

Under this structure, AI instability is confined locally,  
while global system semantics remain under human control.

---

## 5. The Redefined Role of Documentation

In Vibe + Coding, documentation is not an after-the-fact record.  
It is part of the system structure.

Documentation serves as:

- A carrier of design consensus  
- A boundary for frozen decisions  
- A semantic source for auditability  

It serves three audiences simultaneously:

- Providing execution constraints for the Coding phase  
- Acting as a stable memory anchor for the Vibe phase  
- Preserving context for your future self  

Engineering thus shifts from “continuous conversation” to:

**Discrete, versionable, traceable decision sequences.**

---

## 6. Thinking Is Shifted Forward, Not Reduced

One thing must be made clear:

Vibe + Coding does not reduce thinking.

On the contrary, it demands more intensive upfront thinking.

Many decisions that were previously made “while coding” must now be explicitly considered, written down, and frozen during the Vibe phase.

This is a deliberate engineering trade-off:

- More upfront design investment  
- Less low-level implementation labor  
- Higher long-term maintainability  

If you are accustomed to coding first and thinking later, this paradigm may feel uncomfortable.

But if you value design-first and test-driven engineering, it often brings a stronger sense of control.

---

## 7. Principles on Scope of Applicability

Vibe + Coding is not a universal solution.

It is best suited for **design-driven problems**, not implementation-driven ones.

When a project’s core difficulty lies in:

- System decomposition  
- Abstraction stability  
- Boundary clarity  
- Long-term invariants  

Design quality matters far more than implementation speed.

In such problems, Vibe + Coding provides the greatest value.

Conversely, when the core questions are still:

- Can this be built at all?  
- Can performance meet requirements?  
- Is this approach viable?  

Freezing design early is often inappropriate.

Specific misuse cases and failure modes will be discussed in later chapters.

---

## 8. Chapter Summary

Vibe + Coding is not a shortcut, nor a bag of tricks.  
It is a deliberate engineering stance:

- Trade structure for stability  
- Trade documentation for memory  
- Trade design for scale  
- Trade upfront thinking for long-term returns  

When engineers focus on “what to do and why,”  
and AI focuses on “how to correctly execute under constraints,”  
true collaboration becomes possible.

This is the core design philosophy this guide aims to establish.

---

# Chapter 2｜Mental Model

Before any process, template, or concrete practice can be discussed, a correct mental model must be established.  
If the mental model is wrong, no matter how complete the steps or how refined the templates, the process will inevitably collapse back into old Vibe Coding:  
a single conversation, chatting while coding, with design driven by implementation.

**The key to Vibe + Coding is not “how to use AI,”  
but how you view yourself, and how you view AI.**

---

## 1. A Fundamental Shift: You Are No Longer a “User”

In old Vibe Coding, the engineering relationship is often implicit:

- You provide requirements  
- You describe ideas  
- You wait for AI to produce results  

AI is implicitly treated as a black box that:

- Understands requirements  
- Designs solutions  
- Implements them  
- And maybe debugs along the way  

The essence of this relationship is:

> **Humans request, AI substitutes.**

In Vibe + Coding, this relationship must be completely dismantled.

You are no longer:

- A tool user  
- A prompt engineer  
- A person waiting for output  

You play the role of:

**Staff Engineer / Tech Lead.**

This means:

- You are responsible for the entire system  
- You are responsible for architectural quality  
- You are responsible for long-term maintainability  
- You hold final authority over all key design decisions  

AI is no longer “the one who gets things done for you,”  
but an **engineering resource you organize, constrain, and allocate**.

---

## 2. Not One AI, but Three Engineering Roles

Vibe + Coding is not about “using AI more cleverly.”  
It compresses the division of labor of a real engineering team into a **personally controllable collaboration model**.

In this model, there are always three clearly defined roles.

---

### 2.1 You: The Sole System Owner

You are the owner of the entire system.

Your responsibility is not to write the most code, but to make the most important decisions:

- What problem the system actually solves  
- Which problems it explicitly does not solve  
- Where system boundaries lie  
- Which abstractions are worth preserving long-term  
- Which design conclusions must be frozen  

You are responsible for:

- Design trade-offs  
- Architectural judgment  
- Responsibility ownership  

Not for:

- Repetitive implementation  
- Framework boilerplate  
- Mechanical labor  

Your core output is not code, but **decisions**.

---

### 2.2 The Vibe Agent: Design Collaborator

The Vibe Agent participates in only one thing:

**The thinking phase.**

Its role is to help you:

- Clarify unclear ideas  
- Decompose complex problems  
- Expose implicit assumptions  
- Propose structured candidate solutions  
- Externalize thinking into documentation  

It is more like:

- A design discussion partner  
- A thinking amplifier  
- A highly intelligent rubber duck  

The Vibe Agent’s value is not in “providing correct answers,”  
but in:

> **Helping you turn unformed judgments in your mind into discussable, freezable structures.**

One point must be made absolutely clear:

- The Vibe Agent has no decision authority  
- All design conclusions must be confirmed by you  
- Everything it produces is a candidate, never a fact  

---

### 2.3 The Coding Agent: A Constrained Executor

The Coding Agent has a very narrow role.

Its responsibility is only one thing:

> **Correctly executing according to documentation and tests.**

It may:

- Implement features based on documents  
- Fix implementations based on tests  
- Report execution results  

It must not:

- Participate in architectural discussions  
- Redesign interfaces  
- Modify abstraction boundaries  
- Introduce undocumented behavior  

There is a critical discipline in Vibe + Coding:

> **The Coding Agent is not allowed to make decisions that “seem better.”**

If a behavior is not explicitly allowed by documentation, it must not occur.

Once the Coding Agent starts “self-optimizing,” the process has already failed.

---

## 3. Documentation: Frozen Consensus, Not Explanation Material

In Vibe + Coding, documentation is fundamentally redefined.

It is not:

- A tutorial  
- A usage guide  
- An external presentation artifact  

It is:

**The frozen form of design consensus.**

You can think of the Vibe phase as an ongoing technical meeting:

- You and the Vibe Agent continuously discuss  
- Continuously refine understanding  
- Continuously narrow the design space  

Documentation is the meeting minutes of that process.

Its purpose is to:

- Clearly record what has been decided  
- Prevent later stages from repeatedly overturning design  
- Provide the sole authoritative input to the Coding Agent  
- Preserve decision context for your future self  

Once documentation is frozen:

- The design phase temporarily ends  
- The execution phase officially begins  

In this paradigm, “change code first and see” does not exist.

---

## 4. Tests: The Executable Form of Design

In Vibe + Coding, tests are not merely a quality assurance tool.

Their true role is:

**The executable contract of the design document.**

Design documents describe semantic constraints:

- What should happen  
- What must not happen  

Tests translate these constraints into:

- Verifiable behavior  
- Automatically checkable rules  

Thus, in the hierarchy:

- Documents define semantics  
- Tests define behavior  
- Code merely implements behavior  

The Coding Agent’s goal is not “to write code,” but:

> **To make the implementation satisfy the design constraints represented by tests.**

When tests conflict with implementation, the issue can only be:

- The design was not clearly written  
- Or the implementation is wrong  

Never that the test is “too strict.”

---

## 5. A Clear Engineering Responsibility Chain

Putting all roles together yields a clear responsibility chain:

You  
↓  
Design judgment  
↓  
Documentation  
↓  
Tests  
↓  
Code  

The value of this chain is:

- When issues arise, you know where to trace responsibility  
- Each layer has a clearly defined authority  

Code always sits at the bottom.  
It never owns semantic authority.

---

## 6. Failure Almost Always Starts with Role Confusion

Nearly all Vibe + Coding failures stem from the same root cause:

**Role boundaries are violated.**

Common symptoms include:

- Discussing design during the Coding phase  
- Obsessing over implementation details during the Vibe phase  
- Allowing the Coding Agent to modify APIs  
- Masking design flaws with patch code  

Once roles blur:

- Implementation hijacks design  
- Documentation loses authority  
- The system evolves uncontrollably  

This mirrors failure modes in human engineering teams exactly.

---

## 7. Correct Psychological Expectations

In a healthy Vibe + Coding workflow, you should feel:

- The Vibe phase progresses slowly but with high focus  
- The Coding phase progresses quickly and mechanically  
- Cognitive load shifts forward  
- Implementation cost drops significantly  

This is normal.

If you feel that:

- Writing code is harder than designing  
- Implementation repeatedly forces you to “patch design”  

It usually means:

> The design phase was never truly completed.

---

## 8. Chapter Summary

In Vibe + Coding:

- You are the sole system owner  
- The Vibe Agent is a design collaborator  
- The Coding Agent is a constrained executor  
- Documentation freezes consensus and preserves memory  
- Tests are the behavioral contract of design  

When these roles are clearly separated and respected,  
AI can transform from an unstable generator into:

**A reliable, auditable, reusable engineering execution unit.**

Understanding this mental model is a prerequisite for the methodology and practice chapters that follow.

---

# Chapter 3｜Methodology – Vibe

After establishing design philosophy and mental model, we can finally address a practical question:

**How does Vibe + Coding actually operate?**

This chapter does not cover specific tools, platforms, or prompt-writing techniques.  
Those belong to the implementation layer, not methodology.

Instead, this chapter presents a **stable, repeatable, extensible engineering framework**  
that answers a more fundamental question:

> **How to turn a vague, complex, long-term engineering problem  
> into a sequence of tasks that AI can execute safely and controllably**  
In other words, how to **Vibe**.

---

## 1. Why a Methodology Is Necessary

In old Vibe Coding, engineering often advances through continuous conversation:

- Ideas unfold in chat  
- Decisions remain implicit in context  
- Changes happen through “just saying one more thing”  

This feels natural at small scale, but breaks down quickly at engineering scale:

- Decisions are invisible  
- Consensus cannot be frozen  
- State cannot be restored  
- Progress depends on unreliable conversational memory  

Vibe + Coding aims to shift engineering from:

**Continuous conversation → Discrete decision structure**

Only when problems are decomposed, structured, and explicitly recorded  
can AI execute reliably and engineering remain controllable.

---

## 2. The Four-Stage Model Overview

In the Vibe phase, Vibe + Coding uses a fixed four-stage model to organize all design activities:

**Input → Alignment → Refinement → Freeze**

These four stages form the complete **Vibe lifecycle**.

Important notes:

- They are not strictly linear  
- They can loop  
- They can recurse  
- They can nest  

The same model applies to project-level architecture  
and to individual feature-level design convergence.

---

## 3. Input: Provide a Starting Point, Not a Solution

The goal of the Input stage is simple:

> **Provide a starting point for thinking.**

You do not need a full solution.  
You do not consider implementation details.

Input can be:

- A vague idea  
- A goal description  
- A problem statement  

For example:

- “I want to build a chess program supporting local two-player and AI play.”  
- “I want to design a framework to evaluate LLM output quality.”  

At this stage:

- Completeness is not required  
- Correctness is not required  
- Technical choices are deferred  

You are only stating one thing:

**This is the problem we are about to seriously discuss.**

---

## 4. Alignment: Align Understanding, Not Design

Alignment is the **most critical and most frequently skipped step** in the Vibe phase.

Many Vibe Coding failures stem not from poor design ability, but from failing to align on:

**What problem is actually being discussed.**

The sole goal of alignment is:

> **Ensure you and the Vibe Agent share the same understanding of the problem itself.**

Typical alignment activities include:

- Asking the Vibe Agent to restate the problem  
- Exposing ambiguity and unclear areas  
- Clarifying scope, goals, and non-goals  

Typical alignment questions:

- Is this a local program or a server system?  
- Is it for end users or internal use?  
- Does it require long-term extensibility?  
- Are there performance or stability constraints?  

The output of alignment is not a solution, but:

**A mutually agreed-upon problem definition.**

No design should begin before alignment is complete.

---

## 5. Refinement: Turn the Problem into Structure

The goal of refinement is to gradually construct a **discussable, modifiable, implementable system structure** on top of an aligned problem definition.

This stage typically includes:

- Module decomposition  
- Responsibility boundary definition  
- Technical path discussion  
- Preliminary data and interface structures  

During refinement, you may:

- Ask the Vibe Agent to propose multiple design options  
- Compare trade-offs  
- Narrow the design space  

Important constraints:

- No code is written  
- Everything remains design-level thinking  

You are not building implementation, but:

> **A system model that humans can understand, discuss, and take responsibility for.**

---

## 6. Freeze: Freeze Decisions and Form Engineering Consensus

Freeze is the **most important and most often neglected step** in Vibe + Coding.

Here, you must explicitly do one thing:

> **Fix the design conclusions confirmed so far.**

Freeze can take the form of:

- A design document  
- A task specification  
- An architecture description  
- A module boundary definition  

The format does not matter. The semantics do:

- What has been decided  
- What is no longer under discussion  
- What execution must strictly follow  

Once frozen:

- Design becomes read-only  
- Execution receives stable input  

Any new idea must:

- Explicitly break the freeze  
- Modify documentation  
- Enter a new iteration  

“There is no ‘change code first and see.’”

---

## 7. Fractal Recursion: Same Model, Different Scales

The four stages are not limited to top-level design.

They naturally exhibit **fractal recursion**.

You can apply them to:

- The entire project  
- A single module  
- A subsystem  
- A concrete feature  

Repeating:

**Input → Alignment → Refinement → Freeze**

Until you converge to a scale:

> **That a Coding Agent can independently execute as an atomic task.**

At that point, the task should have:

- A clear goal  
- Clear inputs and outputs  
- Clear constraints  
- Clear completion criteria  

This marks the end of the Vibe phase and the start of Coding.

---

## 8. Depth-First, Not Breadth-First

In practice, strongly prefer:

**Depth-first (DFS) over breadth-first (BFS)** progression.

That is:

- Fully design one module to execution-ready state  
- Complete its implementation and validation  
- Only then move to the next module  

The reasons are practical:

- AI struggles to maintain multiple unfrozen designs  
- More half-finished modules mean more semantic pollution  
- Unfrozen designs easily interfere with one another  

DFS maximizes design stability.

---

## 9. Chapter Summary

The four-stage model:

**Input → Alignment → Refinement → Freeze**

forms the methodological core of Vibe + Coding.

Its goal is not speed, but to make engineering:

- Controllable  
- Traceable  
- Executable  

Once you can fluently move between these stages  
and know when to advance and when to freeze,  
you possess the ability to decompose complex engineering problems  
into tasks that AI can safely execute.

---

# Chapter 4｜Execution Workflow – Coding

After completing design philosophy, mental model, and methodology, we now enter the **execution layer of Vibe + Coding**.

This chapter answers a single question:

> **In the Vibe + Coding paradigm, how does a task move from “design frozen” to “code reliably merged”?**

This chapter no longer discusses thinking.  
It defines a **standard engineering closed loop** from frozen design to committed code.

---

## 1. From Design Freeze to Execution: A Necessary Engineering Transition

At the end of the Vibe phase, you typically have design artifacts such as:

- Architecture or module design documents  
- Feature specifications  
- API contracts  
- Rules and invariants  

But one fact must be recognized clearly:

**These are still “human-readable” design languages.**

Coding Agents cannot—and should not—fill in engineering details from vague semantics.

Therefore, before implementation, a crucial transition must occur:

> **Transform design conclusions into a strictly executable engineering task.**

This is not a formatting step, but the establishment of an engineering safety boundary.

---

## 2. What Counts as an “Executable Task”

A task that can be handed to a Coding Agent must satisfy:

- Clear boundaries  
- Explicit behavior scope  
- Enumerated inputs and outputs  
- Determinable completion criteria  

In other words:

> **If you cannot clearly decide whether the task is complete,  
> it is not yet an engineering task.**

In Vibe + Coding, task descriptions are not “please implement this feature,”  
but **engineering tickets**.

The Coding Agent executes tickets.  
It does not infer intent or background.

A simple self-check is whether you, as the task owner, could implement your own design strictly from the description without deviating from intent.

---

## 3. Mandatory Decomposition from Design to Tasks

Design documents usually cover:

- A module  
- A subsystem  
- Or a milestone  

But a Coding Agent can only safely handle:

> **One atomic task at a time.**

Therefore, you must explicitly:

- Decompose design documents into atomic tasks  
- Ensure each task is independently implementable, testable, auditable  
- Minimize implicit dependencies between tasks  

A healthy task has:

- A clear goal  
- An authoritative design source  
- Explicit constraints and invariants  
- Clear completion standards  

If this step is insufficient, all downstream problems will surface during implementation.

---

## 4. Test First: The True Start of Execution

In Vibe + Coding, the Coding phase **does not start by writing implementation**.

It must start with:

> **Tests.**

The reason is simple:

- Documents define semantics  
- Tests define behavior  
- Code implements behavior  

In a healthy execution flow, the Coding Agent’s first steps are:

- Write tests  
- Run tests  
- Observe failures  

This is a positive signal—it means tests are actually constraining behavior.

If tests pass immediately, they likely do not express real design constraints.

---

## 5. The Constrained Execution Loop of the Coding Agent

The Coding Agent must operate strictly within the following loop:

1. Read the task description  
2. Write or extend tests  
3. Run tests (fail)  
4. Write minimal implementation  
5. Run tests again  
6. Fix implementation  
7. Repeat until all tests pass  

The Coding Agent **must not**:

- Modify design documents  
- Expand task scope  
- Introduce undocumented behavior  
- Refactor structure “for aesthetics”  

Its sole objective is:

> **Make the implementation satisfy the tests that represent design constraints.**

---

## 6. Implementation Report: Required Execution Trace

After task completion, the process is not finished.

The Coding Agent must produce an **implementation report** answering at least:

- What functionality was implemented  
- Which implementations correspond to which design constraints  
- Any assumptions or ambiguities encountered  
- Any items requiring human confirmation  

This report is not a summary, but:

> **An auditable execution record.**

Code without an implementation report should not be merged.

---

## 7. Review Loop: Reconciling Design and Implementation

After completion, you must bring the following back to the Vibe phase:

- Implementation code  
- Tests  
- Implementation report  

Review focuses on:

- Does the implementation strictly follow documentation?  
- Are there ambiguities in documentation?  
- Did undocumented behavior appear?  

Issues must be classified as:

- **Design issues** → modify documentation and re-freeze  
- **Implementation issues** → fix tests or code  

A key principle:

> **Never patch code to hide design problems.**

---

## 8. Commit and Stage Confirmation

Once a task passes review:

- Perform local code review  
- Run unit and integration tests  
- Commit to version control  

Recommended practice:

> **One frozen document version corresponds to one commit.**

This ensures:

- Design decisions are traceable  
- Issues can be mapped to design context  

Code history gains engineering meaning.

---

## 9. Integration Awareness

In real systems, serious issues often arise not within modules, but between them.

Therefore, after multiple tasks:

- Run integration tests  
- Verify minimal end-to-end paths  
- Check upstream/downstream interactions  

**Do not wait until all modules are done to integrate.**

This is one of the most expensive mistakes in practice.

---

## 10. The Correct Approach to Refactoring

Refactoring is inevitable in long-term projects, but in Vibe + Coding it must follow the paradigm:

- Update documentation first  
- Adjust tests  
- Then implement changes  

**Silent refactoring is not allowed.**

Any structural change without corresponding design documentation breaks auditability.

---

## 11. Chapter Summary

This chapter defines a complete, executable engineering loop:

Freeze documentation (Vibe Agent)  
→ Atomic task (Vibe Agent)  
→ Test design (Vibe Agent)  
→ Test implementation (Coding Agent)  
→ Code writing (Coding Agent)  
→ Implementation report (Coding Agent)  
→ Review loop (Vibe Agent)  
→ Commit confirmation (Human)

Through this loop:

- Execution is strictly constrained  
- Design retains interpretive authority  
- AI is confined to safe engineering roles  

---

# Chapter 5｜Illustrative Walkthrough: A Complete Vibe + Coding Flow

This chapter is **not a real, complete, directly reproducible engineering case**.  
It does not aim to cover every detail of a project from zero to one.

Its sole purpose is:

> **To connect every key step of Vibe + Coding through a “hypothetical but sufficiently concrete” example,  
> so you can clearly see what you should do at each step—not how to write code.**

Think of this chapter as:

- A process diagram  
- A rehearsal-style walkthrough  
- A transferable operational skeleton  

Not as:

- A full tutorial  
- A best-practice implementation  
- A real project blueprint  

---

## Reading Conventions (Very Important)

- The example is deliberately simplified  
- All prompts are illustrative  
- Outputs prioritize correctness of direction, not completeness  
- The chess project is merely a vehicle, not the focus  

Do not attempt to copy this chapter verbatim into a real project.

---

## 0. Example Problem Setup (For Illustration Only)

Assume the following engineering idea:

- Project: Chess  
- Goal: Support local two-player matches  
- Interface: Command line  
- Language: Python  
- Non-goals:  
  - GUI  
  - Network play  
  - Performance optimization  
  - AI algorithms  

This problem has two characteristics:

- Clear rules  
- Complex state  

It is ideal for **demonstrating process, not technique**.

---

## Step 1 — Input: Declare the Problem Only

### What You Are Doing

You are telling the Vibe Agent:

> “This is what we are about to seriously discuss.”

Not:

> “Design or implement this system for me.”

### Illustrative Vibe Prompt (Input)

- I want to build a chess program in Python.  
- Phase one only considers local two-player play via CLI.  
- Do not design or write code yet.  
- First, record my description.  
- After I say “input finished,” do only two things:  
  1) Restate your understanding of the requirements;  
  2) List what you think is unclear.  

Input finished.

### Tip

If the AI starts discussing modules, classes, or implementation,  
you failed to prevent it from entering design mode during Input.

---

## Step 2 — Alignment: Confirm We Are Discussing the Same Thing

### What You Are Doing

You are not advancing solutions.  
You are eliminating misunderstandings.

Alignment aims for **shared understanding**, not better ideas.

### Illustrative Alignment Actions

- Ask the AI to restate requirements  
- Correct deviations  
- Resolve key uncertainties  
- Explicitly define non-goals  

### Tip

“Restate your understanding” works when inputs are already precise;  
“List unclear points” works better when inputs are vague.

---

## Step 3 — Refinement: Turn the Problem into Structure

### What You Are Doing

You allow the AI to participate in **structural thinking**, but only about:

- Modules  
- Responsibilities  
- Data  
- Flow  

Not implementation.

### Illustrative Vibe Prompt (Refine)

- Based on the aligned requirements:  
  - Propose a minimal viable system structure  
  - Explain module boundaries and responsibilities  
  - Describe core data models  
  - Describe minimal execution flow  
- Do not write code; output structured design only.  

### Tip

Common mistakes in refinement:

- Obsessing over implementation details too early  
- Attempting to design the final form in one pass  

You only need **a system model suitable for documentation**.

---

## Step 4 — Freeze: Turn Discussion into Documentation

### What You Are Doing

You are performing a critical but often skipped step:

> **Fixing what we currently believe is correct.**

### Illustrative Freeze Actions

- Ask the AI to organize current design into a document  
- Explicitly state this is a phase conclusion  
- Declare it the authoritative source for execution  

### Tip

A simple test:

> If you would hand this document to someone who “executes without thinking,”  
> the freeze is sufficient.

---

## Step 5 — From Document to Tasks: Illustrative DFS Decomposition

### What You Are Doing

You are not planning the whole project.  
You are asking:

> “Which small piece can be independently completed next?”

### Illustrative Task Decomposition

For example:

- Task 1: Board and coordinate system  
- Task 2: Piece abstraction  
- Task 3: Move representation  
- …

Each task must be:

- Independently implementable  
- Testable  
- Auditable  

---

## Step 6 — Make One Task Executable

### What You Are Doing

You are transforming a task from:

“Engineer-understandable”  
into  
“Executor-proof.”

### Illustrative Task Document Includes

- Task goal  
- Authoritative design source  
- Scope and boundaries  
- Behavioral constraints  
- Completion criteria  

### Tip

Self-check:

> **If I were the executor, would I need to guess anything?**

---

## Step 7 — Coding: Switch Session, Execute Only

### What You Are Doing

You deliberately **reduce AI freedom**.

- New session  
- No shared context  
- Only the task document  

### Illustrative Coding Prompt Characteristics

- Explicitly state this is execution  
- Declare authoritative sources  
- Explicitly forbid design changes  
- Require test-first  
- Require implementation report  

### Tip: Context Health Signal

A practical trick:

- Require the AI to output a fixed marker (e.g., today’s date) at the end of each response  
- If the marker disappears across responses, stop and restart the session  

This usually indicates context degradation.

---

## Step 8 — Review Loop: Compare Against Documentation

### What You Are Doing

You are not asking:

> “Is the code good?”

But:

> “Did the code faithfully execute the document?”

Any deviation must be attributed to:

- Design issues  
- Or execution issues  

Never masked with patches.

---

## Chapter Summary

This chapter uses a **deliberately simplified illustrative example**  
to demonstrate the full operational skeleton of Vibe + Coding:

- How to start discussion  
- How to align  
- How to converge  
- How to freeze  
- How to decompose  
- How to execute  
- How to review  

You do not need to remember chess.  
You do not need to remember the prompts.

Remember only one thing:

> **At each step, are you thinking—or executing?**

Once these two mix, the process degrades.

---

# Chapter 6｜Common Errors and Engineering Trade-offs

Vibe + Coding is not a process that guarantees success if followed mechanically.  
It is a paradigm that **heavily depends on engineering discipline**.

Once key constraints are violated, the process rarely collapses immediately.  
Instead, it degrades subtly and gradually, eventually reverting to old Vibe Coding.

This chapter aims not to list “bad habits,”  
but to help you recognize **signals that you are misusing the paradigm or should not be using it at all**,  
and to correct course before engineering truly goes out of control.

---

## 1. The Most Dangerous Anti-Pattern: Role Mixing

This is the **most common and most fatal** source of failure.

### Symptoms

- Discussing architecture during Coding  
- Letting the Coding Agent “optimize structure”  
- Writing code before design is frozen  
- Injecting implementation details during Vibe  

### Consequences

- Implementation hijacks design  
- Documentation loses authority  
- Decisions become buried in code  
- The system becomes unauditable  

### Engineering Meaning

Once role boundaries are broken,  
Vibe + Coding no longer exists.

### Correction

- Immediately stop execution  
- Return to documentation  
- Clarify whether you are in Vibe or Coding  
- Restore role and context isolation  

---

## 2. Patching Code to Hide Design Problems

This is the second most common and more insidious degradation path.

### Symptoms

- “This is weird; let’s patch it for now”  
- “Let it run first; we’ll fix the doc later”  
- “The doc isn’t clear, but this code works”  

### Root Problem

**Design flaws are converted into implementation complexity.**

Short-term efficiency masks long-term damage:

- Design becomes hollow  
- Code becomes heavy  
- Eventually, no one dares to touch the system  

### Principle

All unexpected behavior must be resolved at the documentation layer.

**Code does not explain design.**  
Only documentation owns semantic authority.

---

## 3. Documentation Drift: Saying One Thing, Doing Another

### Symptoms

- Documentation stops being updated  
- Implementation clearly exceeds documented scope  
- Tests validate “actual behavior” rather than design behavior  

### Danger Signals

- New contributors must read code to understand the system  
- Documentation becomes historical residue  

This means:

> The system has degraded into implicit knowledge.

### Correction

- Pause new development  
- Systematically reconcile docs and implementation  
- Decide which behaviors are truth and which are obsolete  

---

## 4. Overtrusting AI “Intelligence”

This is a psychological anti-pattern.

### Symptoms

- “It should understand what I mean”  
- “This doesn’t need documentation”  
- “The model is strong; it won’t get this wrong”  

### Reality

- Implicit assumptions accumulate  
- Small deviations amplify  
- Errors become irreproducible and inexplicable  

The core premise of Vibe + Coding is:

> **AI is only reliable within constraints.**

Any “intelligence” outside documents and tests is engineering risk, not advantage.

---

## 5. Over-Formalizing Documentation

Anti-patterns are not only about too little, but also too much.

### Symptoms

- Documentation aims for perfect specification  
- Attempts to define everything upfront  
- Writing docs costs as much as writing code  

### Consequences

- Design rigidity  
- Drastic slowdown in iteration  
- Loss of exploratory space  

### Principle

Documentation should be:

> **Clear enough to execute, but not so rigid that it freezes the future.**

Documentation freezes stage consensus, not ultimate truth.

---

## 6. Forcing Exploratory Problems into the Paradigm

A very common misuse scenario.

### Symptoms

- Unproven algorithms  
- Unvalidated technical paths  
- High-uncertainty exploratory work  

Yet attempting to:

- Write full design documents  
- Define strict tests  
- Freeze implementation paths  

### Outcome

- Many useless documents 
- Frequent design reversals  
- Heavy psychological burden  

### Engineering Judgment

When the core question is still:

“Can this be done?”

Rather than:

“How should this be done well?”

Using Vibe + Coding is itself a mistake.

---

## 7. Misapplying the Paradigm to Inappropriate Scenarios

Forcing Vibe + Coding into these scenarios almost guarantees degradation:

- One-off scripts  
- Strong UI/UX-driven frontend work  
- Highly trial-and-error tuning tasks  
- Legacy systems with heavy historical debt  

In these cases:

- Documentation cost ≈ implementation cost  
- Design freezing lacks realism  

**Paradigm failure does not imply method failure, but scenario mismatch.**

---

## 8. Ignoring Integration Risk

### Symptoms

- All module tests pass  
- System fails as a whole  
- Module interfaces do not compose  

### Cause

Design over-focuses on internal modules, ignoring inter-module composition.

### Correct Practice

- Write integration tests for boundaries  
- Run minimal viable paths early  
- Do not wait until everything is complete to integrate  

---

## 9. Silent Refactoring

### Symptoms

- “I just cleaned up the structure a bit”  
- “It’s just renaming; logic unchanged”  
- No documentation updates  

### Risk

- Design semantics change silently  
- Historical decisions are lost  
- Debugging and tracing costs explode  

### Principle

> **Refactoring without documentation does not exist.**

---

## 10. Early Warning Signs of Loss of Control

If you observe:

- Frequently editing code directly  
- Documentation no longer updated  
- Coding Agent often “guesses” intent  
- Repeated explanations of the same thing  
- Difficulty explaining why bugs occur  

These indicate:

> Engineering is drifting away from Vibe + Coding.

---

## 11. Chapter Summary

Failures of Vibe + Coding almost never stem from insufficient model capability,  
but from **relaxed engineering discipline**.

When the process starts deforming, do not try to:

“Use AI harder.”

Instead:

- Return to role separation  
- Return to documentation  
- Return to tests  
- Return to freeze points  

Vibe + Coding’s value lies not in flexibility,  
but in providing a **path to retreat** when chaos emerges.

---

# Chapter 7｜Conclusion

This guide proposes an engineering paradigm called **Vibe + Coding**.  
It does not aim to make programming “easy,”  
but to leverage the power of Vibe Coding to **increase stability and controllability in engineering practice**.

---

## 1. What Vibe + Coding Does

At its core, Vibe + Coding explicitly decomposes traditional Vibe Coding into two completely separate agent modules:

- **Vibe Agent**: responsible for design, thinking, modeling, and documentation  
- **Coding Agent**: responsible for executing implementations under explicit constraints  

They **share no context whatsoever**.  
Their only communication channels are **documentation and tests**.

A complete cycle looks like:

Human + Vibe Agent design  
→ Task documentation generated  
→ Coding Agent executes  
→ Execution results audited  
→ Documentation or code updated  
→ Next iteration  

Repeated continuously.

---

## 2. Why the Separation Must Be So Strict

The key value of this paradigm lies in **completely separating design from implementation**:

- Design is no longer polluted by implementation details  
- Decisions are no longer silently altered by “convenient code”  
- Engineering semantics are no longer hidden in implementation details  

It moves critical engineering thinking from:

> “thinking while coding”  
> to “thinking before coding”

The act of “writing” is then fully and explicitly delegated to the Coding Agent.

---

## 3. Not a Shortcut, but an Engineering Stance

**Vibe + Coding is not a shortcut, nor a set of tricks.**

It is an engineering stance:

- Trade structure for stability  
- Trade documentation for memory  
- Trade design for scale  
- Trade upfront thinking for long-term returns  

You are choosing not “faster,”  
but “more controllable.”

---

## 4. The Required Mental Shift

To truly use Vibe + Coding, you must accept the following role restructuring:

- **You are the sole system owner**  
  Your core output is not code, but **decisions**.

- **The Vibe Agent is a design collaborator**  
  Its value lies not in correctness, but in:  
  **helping transform unformed judgment into discussable, freezable structure.**

- **The Coding Agent is a constrained executor**  
  More like a junior engineer turning tickets into code,  
  without participating in judgment.

- **Documentation is frozen consensus and engineering memory**  

- **Tests are the behavioral contract of design**

---

## 5. The Vibe Phase: Organizing Design Work

In the Vibe phase, Vibe + Coding uses a fixed four-stage model:

**Input → Alignment → Refinement → Freeze**

These stages exhibit **fractal recursion**.

You can apply them to:

- Entire projects  
- Individual modules  
- Subsystems  
- Concrete features  

Repeating until you reach a scale:

> **That a Coding Agent can independently execute as an atomic task.**

---

## 6. The Coding Phase: From Freeze to Commit

In the Coding phase, a complete controlled execution chain is:

Freeze documentation (Vibe Agent)  
→ Atomic task (Vibe Agent)  
→ Test design (Vibe Agent)  
→ Test implementation (Coding Agent)  
→ Code writing (Coding Agent)  
→ Implementation report (Coding Agent)  
→ Review loop (Vibe Agent)  
→ Commit confirmation (Human)

In this chain:

- Semantics flow top-down  
- Responsibility traces bottom-up  
- Each layer has clear interpretive authority  

---

## 7. The Real Cause of Failure

When Vibe + Coding fails, it is **almost never due to insufficient model capability**,  
but rather:

> **Relaxed engineering discipline.**

When the process starts deforming, do not try to:

“Use AI harder.”

Instead:

- Return to role separation  
- Return to documentation  
- Return to tests  
- Return to freeze points  

---

## 8. Final Conclusion

The value of Vibe + Coding lies not in flexibility,  
but in providing, amid chaos, a:

> **Reversible engineering path.**

When engineering no longer depends on implicit memory or improvisation,  
when decisions are structured, frozen, and auditable,  
AI can finally become a reliable engineering execution unit.

That is the goal Vibe + Coding seeks to achieve.
