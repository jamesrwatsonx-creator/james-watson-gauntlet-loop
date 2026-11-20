<img width="1079" height="544" alt="25710" src="https://github.com/user-attachments/assets/014c21b5-dc2f-41c3-839a-944bff04714a" />
# James Watson's Gauntlet Loop

A recursive multi-agent orchestration system for building from recovered constraints rather than surface imitation.

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
Level 5  Execution in Codex / Claude Code / other agent harnesses
```

The hidden Constitution is product IP and must never be exposed through client code, public assets, browser state, logs, API responses, generated prompts, or source maps.

## V1 product surfaces

- Cinematic intro
- New Gauntlet intake
- Prompt compiler output
- Orchestration workspace
- Constraint Ledger
- Benchmark / evaluation view
- Knowledge library
- Model / resource settings

## Visual identity

- Cinematic armored-gauntlet opening screen
- Atmospheric coral-to-deep-teal background language
- Transitional/Classical Roman serif for primary titles: EB Garamond preferred, Baskerville/Cinzel/Times New Roman fallbacks
- Ultra-light geometric sans for technical UI: Inter Thin/ExtraLight preferred, Helvetica Now Thin/Montserrat Thin/Satoshi Light fallbacks
- Near-black, charcoal, warm ivory, and restrained antique-gold accents

## Security rule

**Never commit the private Master Gauntlet Constitution to this public repository.** Runtime implementations should load it from protected server-side configuration or a private secret store.

## Status

Early product architecture / V1 build.

## Role in an agent engineering stack

Gauntlet is designed as a constraint-discovery and construction/evaluation method, not a model, universal memory store or complete agent runtime. Prompting specifies an objective; context supplies relevant knowledge; a harness provides tools and permissions; loops correct a bounded result; graphs coordinate real dependencies. Gauntlet can operate within those layers to recover why a benchmark works and revise both the construction and the underlying assumptions when evidence contradicts them.

A prospective integration should accept a scoped goal, reference, environment, constraints and acceptance criteria, and return an artifact, actual evaluation evidence, unresolved issues and candidate transferable lessons. Bound retries, cost and time; keep independent evaluation distinct from builder advocacy; use deterministic checks where possible. New hypotheses are not validated competence. Never allow a comparative win to override mandatory security, accessibility or functional requirements.

The system is an early specification, not a demonstrated autonomous runtime. This public README deliberately describes only the general method; private constitutions, owner-specific context, credentials and commercial integration plans remain outside this repository.

