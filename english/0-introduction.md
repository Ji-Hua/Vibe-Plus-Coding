© 2026 Ji Hua.
This repository documents the Vibe + Coding methodology.
Licensed under CC BY-NC-ND 4.0.

Vibe + Coding — Version 0.1

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
