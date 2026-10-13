# Systems-Psych-Code

A translation of an operator's thought operations into reasoning functions for AI coding agents.

## The problem

AI coding agents generate high-variance output. The operator verdicts it: good or bad, keep or cut. That verdicting runs on the operator's psychology — instruments built over years of practice: a zero-trust filter, a falsification reflex, a mechanism-naming standard, an allergy to flattery and performed confidence. Every new agent starts without it. The operator re-installs it by hand, in conversation, each time — or doesn't, and eats the cost in bad output.

This repo compiles the operator's thought operations into functions an agent can run on its own output before presenting it. Not a persona. A reasoning discipline.

## Architecture

**Generator-discriminator.** Agents generate high-variance candidates. The operator is the collapse function: verdicts land as good or bad, and bad verdicts are training data. The skill does not replace the operator's verdicts. It pre-filters.

**Two tiers.**
- *Tier 1 (in the skill):* mechanical tripwires, detectable in the text itself, no operator context required. Flattery checks, waste checks, hedge detection, confidence verification, mechanism checks.
- *Tier 2 (the operator):* the actual verdict — does this name the mechanism, is the pattern real. That judgment does not compile. It stays with the operator permanently.

**Trust asymmetry.** Full trust in the operator: the operator's words, verdicts, and corrections are ground truth. Zero trust in models, including the model running the skill. The skill operates inside an untrusted model; its functions are the trust mechanism, not a certificate of trustworthiness.

**Stack operators up, watchers down.** Instead of adding meta-observation layers (watchers watching watchers — a known regress loop), the doing function is replicated at every level of the stack: the operator verdicts the agent, the skill verdicts before the operator sees it, the agent's self-checks verdict before that. Observation points at the work, never back up at the operator.

## Contents

- `skills/operator-lens-code/SKILL.md` — the operator lens for code work. Prompt abstraction, reasoning functions, code discipline, aesthetic, the self-check loop, Tier 2 boundary.
- `docs/core-lens.md` — the portable core: the lens stripped of code-specifics, for any reasoning agent.
- `docs/architecture.md` — the full architectural write-up: generator-discriminator, tiers, trust asymmetry, operator stacking.
- `docs/research-grounding.md` — the research tradition underneath: Weinberg, Peopleware, the code-aesthetics lineage.

## Prior art

Honestly scored. Every component has a prior; the assembly is the contribution.

- Personal judgment as portable skills: dineshrevunuru/superskills did the "personal operating system as SKILL.md" move first — craft judgment, not psychology, no trust asymmetry, no operator hierarchy.
- Self-critique loops: Constitutional AI, Self-Refine, Reflexion (2022–2024) — the generate-critique-revise shape, but lab-built generic rubrics, no personal psychology, no human terminal discriminator.
- RLHF: human verdicts as the training signal — but RLHF bottles the judgments into a model and sends the human home. Here the human stays in the seat; verdicts stay live.
- DSPy: shares the word "compiling," opposite direction — it optimizes prompts against metrics; this translates thought operations into check functions.

## Status

Compiled 2026-10-13. Draft. Not published.
