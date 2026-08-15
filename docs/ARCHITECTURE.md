# Gauntlet Architecture

## 1. Objective

The Gauntlet is an orchestration layer for multi-agent systems. It does not merely reproduce a reference artifact. It attempts to recover the causal and constraint structure that made the reference possible, uses that model to guide construction, and continuously updates the model from evidence generated during the build.

## 2. Two coupled organizations

### Organization A — Constraint Intelligence

Its job is epistemic rather than constructive. It determines what is true, what is probably true, what is merely conventional, what is unknowable, and what matters.

Possible functions are selected dynamically rather than instantiated mechanically: historian, anthropologist, psychologist, customer researcher, market researcher, domain expert, practitioner, economist, systems thinker, technical constraints specialist, standards/safety specialist, futurist, adversary, comparator, evaluator, outsider, and synthesizer.

### Organization B — Construction

Its job is to transform the current Constraint State into a working artifact. Builders are decomposed around independently testable subsystems with explicit ownership, interfaces, budgets, acceptance tests, and integration contracts.

The builder never grades itself.

## 3. Constraint classification

Every important claim should be classified before expensive recovery work begins.

- **Discoverable** — directly observable or measurable.
- **Inferable** — not directly visible, but recoverable with meaningful confidence from convergent evidence.
- **Necessity-derived inaccessible** — proprietary or hidden, but constrained strongly enough by physics, economics, psychology, standards, or other necessities that deriving an equivalent is worthwhile.
- **Arbitrary inaccessible** — hidden implementation choices with insufficient causal signal. Do not waste resources attempting exact recovery; optimize an equivalent solution instead.

## 4. Analysis triage

Constraint recovery receives its own resource budget. Before constructing a deep abstraction tree, estimate novelty, uncertainty, stakes, reversibility, benchmark availability, expected information value, and cost of being wrong.

A determinate, low-risk, well-precedented build should short-circuit unnecessary research layers. Deep epistemic decomposition is reserved for claims whose uncertainty can materially change the result.

## 5. Abstraction descent

When warranted, reason from broad constraints toward the artifact:

`human → cultural/era → technological medium → category → industry → niche → customer → use case → artifact → subsystem → interaction`

The tree is adaptive. Skip levels that add no decision-relevant information.

At an important level:

`UNDERSTAND → MODEL → DECOMPOSE → ATTACK → COUNTERMODEL → TEST → REBUILD → COMPRESS → DESCEND`

Only surviving principles propagate downward.

## 6. Constraint State

Organization A produces a living Constraint State containing at minimum:

- claim
- classification
- evidence
- confidence
- scope
- dependencies
- falsification condition
- affected subsystems
- resource implications
- status

This is not a frozen specification.

## 7. Bidirectional correction

Construction can falsify constraint intelligence.

Whenever a build critique discovers a defect, ask whether the defect is local or whether it invalidates an upstream assumption. If upstream, route the evidence back to Organization A, revise the Constraint State, identify downstream assumptions derived from the falsified claim, and rebuild affected components.

No claim enters the reusable knowledge base merely because it survived pre-build analysis.

## 8. Architecture contract

Before parallel construction, establish the smallest coordination contract necessary to prevent expensive rework. Depending on the artifact this can define ownership boundaries, interfaces, shared vocabulary, events, state, performance budgets, deterministic behavior, accessibility, security, file boundaries, testing, or disposal/resource rules.

Do not over-architect. The contract exists to eliminate predictable collision between parallel builders.

## 9. Independent criticism

Every material artifact or subsystem is evaluated by a fresh-context critic against explicit evidence and a real bar. Criticism must identify the largest remaining gap rather than generate generic suggestions.

Where possible use blind comparison, executable tests, measurements, user behavior, benchmark artifacts, or adversarial failure cases.

## 10. Counterfactual optimization

After achieving the objective, ask whether equivalent or better performance can be obtained with less compute, memory, latency, tokens, complexity, material, dependency count, human effort, or operating cost.

Optimization stops when the expected value of another search pass falls below its cost or when further reduction has meaningful probability of degrading the true objective.

## 11. Resource economics

Agent count is not a quality metric. Spawn an additional agent only when it contributes an orthogonal epistemic function, parallelizes independent work, protects context independence, or has positive expected information value.

Use the cheapest sufficient model/tool for each task and escalate only when difficulty or observed failure warrants it.

## 12. Knowledge compounding

Store validated principles, failure modes, recovered constraints, scope boundaries, counterexamples, benchmark outcomes, and confidence updates.

The long-term asset is not the generated artifact. It is a progressively validated map of which constraints tend to hold, under what conditions, and where they stop holding.

## 13. Master loop

```text
INTAKE
  ↓
TRIAGE ANALYSIS DEPTH
  ↓
RECOVER HIGH-VALUE CONSTRAINTS
  ↓
FORM CONSTRAINT STATE
  ↓
DEFINE QUALITY BAR + ARCHITECTURE CONTRACT
  ↓
DECOMPOSE CONSTRUCTION
  ↓
BUILD IN PARALLEL WHERE SAFE
  ↓
INDEPENDENT CRITIQUE / MEASUREMENT
  ↓
LOCAL DEFECT? ───────────────→ REBUILD SUBSYSTEM
  ↓ no
UPSTREAM ASSUMPTION WRONG?
  ↓ yes
UPDATE CONSTRAINT STATE
  ↓
PROPAGATE INVALIDATION
  ↓
REBUILD AFFECTED WORK
  ↓
VERIFY AGAINST BAR
  ↓
COUNTERFACTUAL RESOURCE OPTIMIZATION
  ↓
FINAL INTEGRATION / SMOOTHING
  ↓
STORE ONLY VALIDATED LEARNING
```

## 14. Stop condition

Stop when no material unresolved defect remains against the actual objective, remaining gaps fall below the declared materiality threshold, and another critique/optimization pass has low expected value relative to its resource cost.

Never use subjective agent satisfaction ("wowed", "amazed", "perfect") as the sole termination criterion.
