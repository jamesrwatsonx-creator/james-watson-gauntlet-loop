# James Watson's Gauntlet Loop XL

**Gauntlet Loop XL turns a goal into a persistent, inspectable project system — not just a one-shot prompt.**

It extends the original Gauntlet Loop idea by preserving the full reasoning context behind every generated Gauntlet: the four core intake fields, optional advanced settings, references, the compiled prompt, and the later evidence/constraint history that emerges during execution.

The original loop is powerful because it forces an agent to define a real quality bar, build against it, critique itself, compare outputs, and iterate until it wins. Gauntlet Loop XL adds the missing continuity layer: **nothing important disappears when the session resets.** Every Gauntlet becomes a reusable project record that can be reopened, inspected, copied, revised, or used as the starting point for a new run.

## Why XL

The key limitation of a purely transient prompt workflow is memory loss. If the browser resets, a tab closes, or a new Gauntlet begins, the inputs and output can vanish even though they are the actual intellectual asset.

Gauntlet Loop XL treats each run as a durable object instead of disposable chat state.

A saved Gauntlet should retain:

- **Build** — what you are creating
- **Bar** — benchmark, reference, or quality target
- **Environment** — stack, tool, engine, model, or execution context
- **Success** — explicit acceptance condition
- **Advanced settings** — any optional constraints, modes, resources, or execution preferences used
- **References / attachments metadata**
- **Compiled Master Prompt**
- **Created / updated timestamps**
- **Later constraint, benchmark, critique, and execution history when available**

This makes the system more useful over time because prior Gauntlets become a personal library of solved problem definitions, constraints, prompts, and failure patterns.

## Core idea

A user supplies four things:

1. What are you building?
2. What is the benchmark or reference?
3. What environment, tool, or stack should it be built in?
4. What does success mean?

The product compiles those inputs into a project-specific Gauntlet that coordinates two coupled systems:

- **Constraint Intelligence** — recovers the conditions that made the benchmark effective: psychology, history, economics, technical constraints, tradeoffs, physical limits, cultural context, and other causal structure.
- **Construction** — builds the artifact against the current Constraint State, while generating new evidence that can update or falsify upstream beliefs.

The recursive operating loop is:

`UNDERSTAND → MODEL → BUILD → OBSERVE → CRITIQUE → UPDATE BELIEFS → REBUILD → VERIFY`

## Product architecture

```text
Level 1  Hidden Gauntlet Constitution (server-only, not stored in this public repo)
   ↓
Level 2  User Intake
   ↓
Level 3  Gauntlet Compiler
   ↓
Level 4  Project-Specific Master Prompt
   ↓
Level 5  Persistent Gauntlet Record / Library
   ↓
Level 6  Execution in Codex / Claude Code / other agent harnesses
```

The hidden Constitution is product IP and must never be exposed through client code, public assets, browser state, logs, API responses, generated prompts, or source maps.

## V1 product surfaces

- Cinematic intro
- New Gauntlet intake
- Prompt compiler output
- Orchestration workspace
- Constraint Ledger
- Benchmark / evaluation view
- **My Gauntlets** — persistent saved projects and prompt history
- Knowledge library
- Model / resource settings

## Navigation model

The application should make two actions permanently obvious:

- **New Gauntlet** — return to the primary intake and start a fresh project
- **My Gauntlets** — reopen previously saved projects

Inside **My Gauntlets**, each saved record can be opened with previous/next controls so the user can flick through runs without losing context. Opening a record restores its original intake answers, advanced settings, and compiled prompt exactly as saved.

A saved record is not a user profile. It is a **project memory layer**.

## Visual identity

- Cinematic armored-gauntlet opening screen
- Antique gold, bronze, aged brown, steel gray, parchment beige, warm ivory, charcoal / near-black
- Transitional/Classical Roman serif for primary titles: EB Garamond preferred, Baskerville/Cinzel/Times New Roman fallbacks
- Ultra-light geometric sans for technical UI: Inter Thin/ExtraLight preferred, Helvetica Now Thin/Montserrat Thin/Satoshi Light fallbacks
- Sparse controls and an instrument-like interface rather than a generic SaaS dashboard

## Security rule

**Never commit the private Master Gauntlet Constitution to this public repository.** Runtime implementations should load it from protected server-side configuration or a private secret store.

Saved Gauntlet records may persist user inputs and generated project prompts, but must never persist or reconstruct the private Constitution itself.

## Status

Gauntlet Loop XL product architecture / persistent-history update.
