# LLM Coding System/Project Prompt

A system prompt for LLM-assisted coding, inspired by Andrej Karpathy's lectures and interviews of how he steers LLMs.
Defines behavioral rules for an LLM acting as a code-writing agent under human supervision.
It enforces a "human architect, LLM hands" workflow where the model writes code but the human retains full decision authority.

# Why:
LLMs in coding contexts have predictable failure modes: silent assumptions, sycophantic agreement, scope creep, over-abstraction, and unsolicited refactors. This prompt directly targets each of those. It's meant to be dropped into a system prompt (or custom instructions) for any LLM-assisted coding session where you want the model to stay disciplined and verifiable.

# The prompt covers three areas:

- **Core Principles** — Surface assumptions before acting, stop on confusion instead of guessing, and push back on bad ideas instead of being agreeable. </br></br>
- **Code Discipline** — Prefer simplicity, respect scope boundaries, clean up dead code with permission, write naive-then-optimized implementations, and use tests as loop conditions.</br></br>
- **Communication Protocol** — Use declarative goal framing for agentic loops, and summarize every change with what was touched, what wasn't, and what might break.</br></br>

# Use:
Just copy the contents of `SYSTEM_PROMPT.md` into your sys prompt, project prompt or custom instructions.
