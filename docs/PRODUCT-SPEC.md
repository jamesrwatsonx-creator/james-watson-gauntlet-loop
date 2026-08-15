# James Watson's Gauntlet Loop XL — V1 Product Spec

## Product promise

Give the system an objective and a bar. It constructs the reasoning and execution system required to reach the bar rather than merely generating a larger prompt — and it preserves every Gauntlet as a durable project record instead of disposable session state.

## Primary flow

### Screen 0 — Intro
Full-screen cinematic armored gauntlet artwork. Minimal title treatment. A black circular control with restrained antique-gold arrow advances into the application.

### Screen 1 — New Gauntlet
Four-field intake: Build, Bar, Environment, Success. Reference attachments are optional. Advanced settings are optional. Primary action: **Forge Gauntlet**.

The four core answers must autosave locally or to the authenticated project store as the user types so a reset or accidental navigation cannot destroy work.

### Screen 2 — Compilation
Show the system assembling the project-specific operating model without exposing private Constitution text. Useful visible states include: reading objective, locating constraints, selecting lenses, establishing bar, defining architecture, planning critics, allocating resources.

### Screen 3 — Master Prompt
Display the generated execution prompt. Actions: Copy, Export, Run/Send where integrations permit, Save as Gauntlet.

Saving creates or updates a persistent Gauntlet record containing:
- Build
- Bar
- Environment
- Success
- Advanced settings
- Reference / attachment metadata
- Compiled Master Prompt
- Created / updated timestamps
- Later execution, critique, benchmark, and constraint history when available

### Screen 4 — Orchestration
When execution telemetry exists, visualize two coupled organizations: Constraint Intelligence and Construction. Show active agents/functions, evidence, critiques, constraint revisions, build state, resource use, and current quality gaps.

### Screen 5 — Constraint Ledger
Inspectable claims with confidence, evidence, scope, classification, falsification condition, and downstream dependencies.

### Screen 6 — Benchmark
Compare current artifact against its declared bar using appropriate metrics, blind comparisons, tests, screenshots, or other evidence.

### Screen 7 — My Gauntlets
This is the persistence layer for prior project runs. It replaces the idea of a generic profile screen.

Each saved Gauntlet must preserve the complete project definition and generated prompt so the user can return later and recover exactly what produced that run.

Primary behavior:
- Show saved Gauntlets newest first.
- Open any Gauntlet into a detail view.
- Provide previous / next arrows for fast sequential browsing.
- Restore all four intake answers exactly as saved.
- Restore advanced settings exactly as saved.
- Restore the compiled prompt exactly as saved.
- Allow **Duplicate as New** to seed a fresh Gauntlet without overwriting the original.
- Allow **Back to New Gauntlet** from any saved record.
- Allow rename, archive, and delete with confirmation.

Suggested record summary:

```text
Gauntlet title
Created date / Updated date
Build
Bar
Environment
Success
[Open]  [Duplicate as New]
```

The user should never need to reconstruct an old prompt manually from memory.

### Screen 8 — Knowledge Library
Validated reusable constraints, benchmark patterns, failure patterns, and reusable project intelligence accumulated across Gauntlets.

This is distinct from **My Gauntlets**:
- **My Gauntlets** = the user's saved project runs.
- **Knowledge Library** = reusable validated knowledge extracted across runs.

## Persistent data model

At minimum, a saved Gauntlet record should support:

```text
id
name
created_at
updated_at
build
bar
environment
success
advanced_settings
reference_metadata
compiled_prompt
status
```

Optional later fields:

```text
constraint_ledger_id
benchmark_id
execution_history
critic_history
quality_score
parent_gauntlet_id
```

`parent_gauntlet_id` allows a duplicated or evolved Gauntlet to preserve lineage without mutating the original.

## Navigation

Do not rely on a profile metaphor. The primary navigation should represent the actual jobs the user performs.

Recommended compact navigation:

- **New** — plus / forge icon; returns to fresh intake
- **My Gauntlets** — saved project history
- **Library** — reusable validated knowledge
- **Settings** — models, resources, preferences

The most important global action is **New Gauntlet**. It should remain available from every major screen.

Within My Gauntlets detail view, add restrained left/right arrows to move between saved records. Swiping may be supported on mobile, but visible controls should remain available for discoverability.

## Save behavior

Persistence must be explicit and resilient:

1. Draft intake autosaves while editing.
2. Forging the prompt never clears the intake data.
3. Successful compilation automatically creates a recoverable draft/version even before the user manually names it.
4. **Save as Gauntlet** promotes the draft into the permanent My Gauntlets history.
5. Starting **New Gauntlet** creates a new record context; it does not overwrite the previous Gauntlet.
6. Reopening an old Gauntlet must not silently regenerate the prompt. The exact saved prompt is shown unless the user explicitly chooses Recompile.

This prevents the prior failure mode where resetting the application caused the generated prompt and its source inputs to disappear.

## Design language

The experience should feel like an intelligent instrument, not a generic SaaS dashboard.

Visual palette:
- antique gold
- bronze / copper
- aged brown
- steel gray
- parchment beige / warm ivory
- charcoal / near-black

Typography:
- Display/classical serif: EB Garamond preferred. Baskerville, Cinzel, Times New Roman fallback.
- Technical/geometric sans: Inter Thin/ExtraLight preferred. Helvetica Now Thin, Montserrat Thin 100, Satoshi Light fallback.

Controls should be sparse. Avoid dense cards, gratuitous gradients, generic AI-purple styling, excessive pills, and decorative dashboards.

## Critical security architecture

The private Gauntlet Constitution belongs only in protected server-side configuration. The browser sends structured intake to a server function. The server constructs the model request using the private Constitution and returns only the compiled project prompt/result.

Never expose the Constitution through frontend bundles, localStorage, database rows readable by users, public repositories, analytics payloads, logs returned to clients, source maps, or generated output.

Persistent Gauntlet records may contain user-provided intake and the generated project-specific prompt, but must not contain the Constitution or hidden orchestration instructions used to produce it.

## Acceptance criteria

A new user should be able to understand the product and generate a useful project-specific Gauntlet without learning the internal framework.

The generated prompt must materially change according to the domain. A game, website, physical structure, brand, research project, and business system should not receive cosmetic variants of one static template.

The application must distinguish constraint discovery from construction and preserve the feedback path between them.

Persistence acceptance tests:
- Fill all four intake fields, add advanced settings, forge a prompt, refresh/reopen, and verify the data is recoverable.
- Start a second Gauntlet and verify the first remains unchanged.
- Open My Gauntlets and browse previous/next through saved records.
- Reopen a saved record and verify every intake field and the exact compiled prompt match the stored version.
- Duplicate an old Gauntlet and verify edits affect only the duplicate.
