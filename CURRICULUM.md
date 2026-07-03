# The Harness Engineering Workshop by Vizuara

**Format:** 5-day live workshop · 7:00–9:00 AM IST daily · ₹60,000
**Instructor:** Raj Dandekar (Vizuara)
**Premise:** Claude Code is not a model. It is a harness — the loop, tools, context
machinery, and recovery systems wrapped around a model. In five mornings you build
that layer from scratch: a working, minimal agentic harness in the spirit of
**pi** (pi.dev), studying **Claude Code** and **Hermes** (Nous Research) as
production case studies along the way.

**What you leave with:** your own working coding-agent harness (loop → tools →
context engine → recovery → orchestration), and a precise mental model of the
difference between prompt engineering, context engineering, and harness engineering.

---

## Module 1 — The Anatomy of a Harness (Day 1)

The thesis of the whole workshop: models are commodities, harnesses are the product.

- Why "just call the API" fails: transactional inference vs. a real agent
- Dissecting three harnesses live: Claude Code, pi, Hermes — what each layer does
- Prompt engineering vs. context engineering vs. harness engineering — precise boundaries
- The agent loop from first principles: messages, turns, stop conditions, streaming
- **Build:** a bare harness — model client + message array + hand-rolled loop that runs until the model stops asking for work

## Module 2 — Tools & the Execution Environment (Day 2)

A harness is only as good as what it lets the model *do* — and what it refuses to let it do.

- Tool schemas as contracts: read, write, edit, bash, search
- Streaming tool calls and partial results to the terminal UI
- Permission gates and approval modes (why Claude Code asks before `rm`)
- Sandboxing and the blast-radius problem; code-mode vs. tool-mode
- **Build:** wire real file and shell tools into your loop — your harness edits actual code on your machine, safely

## Module 3 — Context Engineering Inside the Harness (Day 3)

The context window is the scarcest resource in the system. The harness is its allocator.

- Context budgets: what goes in every turn, what gets evicted
- Compaction and summarization: surviving long sessions without losing the plot
- Memory systems: session state, persistent memory files, the CLAUDE.md pattern
- System prompts as infrastructure, not prose
- **Build:** compaction + a persistent memory layer, so your harness survives a 200-turn session

## Module 4 — Durability, Recovery & Orchestration (Day 4)

Demos die on the first crash. Harnesses recover.

- Durable execution: checkpointing every model turn and tool call, replay on restart
- Self-healing loops: retries, failure classification, resumable sessions
- Sub-agents and handoffs: when one context can't hold the job
- Supervision and human-in-the-loop: plans, approvals, escalation
- **Build:** checkpointed execution + a sub-agent dispatcher with an approval gate

## Module 5 — Production Harnesses & Capstone (Day 5)

Read the masters, then ship your own.

- pi internals: extensions, models.json, the minimal-surface philosophy
- Hermes internals: Nous Research's harness design choices
- Claude Code internals: skills, hooks, MCP, sub-agent types
- Evaluating a harness: how you know yours actually works
- **Capstone:** assemble everything into your own pi-style harness and demo it — loop, tools, context engine, recovery, orchestration

---

## Firestore lesson placeholders (per module)

Each module (topic) gets 3 placeholder lessons for draft mode:
1. "Live Session Recording — Day N" (VIDEO LECTURE, embedUrl empty)
2. "Lecture Notes & Visual Walkthroughs" (TEXT)
3. "Code Checkpoint — Day N" (TEXT, will hold the GitHub branch link)
