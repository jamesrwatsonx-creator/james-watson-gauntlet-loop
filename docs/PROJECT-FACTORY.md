# Project Factory Architecture

The Gauntlet app is a control plane, not a monorepo for every artifact it creates.

## Personal Gauntlet Library

The Gauntlet app should keep a durable index of the user's Gauntlets, including:

- objective
- benchmark/reference
- environment/stack
- success bar
- generated project-specific Gauntlet prompt
- selected analysis depth
- constraint/evaluation metadata
- linked execution repository, when one exists
- status and last run

## Optional GitHub connection

GitHub should be optional at Gauntlet creation time.

A user may choose:

1. **Prompt only** — compile and save the Gauntlet without creating an execution repository.
2. **Link/Create repository** — associate the Gauntlet with an isolated repository for execution.

Do not require GitHub to use the compiler.

## Repository isolation

Serious builds should execute in their own repositories rather than inside the Gauntlet app repository.

Example:

```text
james-watson-gauntlet-loop      # compiler/control plane
smp-clinic-gauntlet             # execution repo
fps-gauntlet                    # execution repo
voice-agent-gauntlet            # execution repo
```

The control plane should record links to those repositories and show their status, but should not mix their source trees together.

## Security boundary

The private Master Gauntlet Constitution must not be stored in user execution repositories and must not be embedded in generated prompts. Execution repositories receive only the compiled, project-specific Gauntlet instructions needed for that build.

This separation protects the compiler's internal decision logic while allowing users to own and operate their generated artifacts independently.
