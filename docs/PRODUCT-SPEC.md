# James Watson's Gauntlet Loop — V1 Product Spec

## Product promise

Give the system an objective and a bar. It constructs the reasoning and execution system required to reach the bar rather than merely generating a larger prompt.

## Primary flow

### Screen 0 — Intro
Full-screen cinematic armored gauntlet artwork. Minimal title treatment. A black circular control with restrained antique-gold arrow advances into the application.

### Screen 1 — New Gauntlet
Four-field intake: Build, Bar, Environment, Success. Reference attachments are optional. Primary action: **Forge Gauntlet**.

### Screen 2 — Compilation
Show the system assembling the project-specific operating model without exposing private Constitution text. Useful visible states include: reading objective, locating constraints, selecting lenses, establishing bar, defining architecture, planning critics, allocating resources.

### Screen 3 — Master Prompt
Display the generated execution prompt. Actions: Copy, Export, Run/Send where integrations permit, Save as Gauntlet.

### Screen 4 — Orchestration
When execution telemetry exists, visualize two coupled organizations: Constraint Intelligence and Construction. Show active agents/functions, evidence, critiques, constraint revisions, build state, resource use, and current quality gaps.

### Screen 5 — Constraint Ledger
Inspectable claims with confidence, evidence, scope, classification, falsification condition, and downstream dependencies.

### Screen 6 — Benchmark
Compare current artifact against its declared bar using appropriate metrics, blind comparisons, tests, screenshots, or other evidence.

### Screen 7 — Library
Saved Gauntlets plus validated reusable constraints and failure patterns. This becomes increasingly valuable as projects accumulate.

## Design language

The experience should feel like an intelligent instrument, not a generic SaaS dashboard.

Background: use the supplied atmospheric coral/orange-to-deep-teal image as the dominant application environment, with dark translucent surfaces where legibility requires them.

Typography:
- Display/classical serif: EB Garamond preferred. Baskerville, Cinzel, Times New Roman fallback.
- Technical/geometric sans: Inter Thin/ExtraLight preferred. Helvetica Now Thin, Montserrat Thin 100, Satoshi Light fallback.

Controls should be sparse. Avoid dense cards, gratuitous gradients, generic AI-purple styling, excessive pills, and decorative dashboards.

## Critical security architecture

The private Gauntlet Constitution belongs only in protected server-side configuration. The browser sends structured intake to a server function. The server constructs the model request using the private Constitution and returns only the compiled project prompt/result.

Never expose the Constitution through frontend bundles, localStorage, database rows readable by users, public repositories, analytics payloads, logs returned to clients, source maps, or generated output.

## Acceptance criteria

A new user should be able to understand the product and generate a useful project-specific Gauntlet without learning the internal framework.

The generated prompt must materially change according to the domain. A game, website, physical structure, brand, research project, and business system should not receive cosmetic variants of one static template.

The application must distinguish constraint discovery from construction and preserve the feedback path between them.
