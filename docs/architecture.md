# Architecture

## Generator-discriminator

Agents generate high-variance candidates. The operator is the collapse function: verdicts land as good or bad, cheap and fast, and bad verdicts are training data. The load-bearing property is cost asymmetry — collapsing is cheaper than generating — so generation runs hot and the operator collapses the mistakes.

The skill does not replace the operator. It pre-filters. Tier 1 catches the mechanical failures; Tier 2 verdicts stay with the operator permanently.

## The two tiers

**Tier 1 — codable, no operator context required.** Mechanical tripwires, detectable in the text itself:
- Flattery: the sentence is about the operator rather than the work.
- Waste: restatement of the operator's point without added information.
- Hedge clusters: "might," "could," "perhaps" marking unverified claims.
- Performed confidence: assertions without verification.
- Costume: decorative abstraction, cleverness performing intelligence.

**Tier 2 — the operator.** The actual verdict: does this name the mechanism, is the pattern real. That judgment does not compile. It requires the operator's full context — years of built instruments, corrections, and calibrations. Tier 1 exists so Tier 2 only fires on worthy candidates.

## Trust asymmetry

The operator is the one trusted component in the stack. Full trust flows upward to the operator; zero trust flows downward through every model layer, including the model running the skill. The operator's verdicts are ground truth. Everything else earns trust per-claim, per-run, through verification.

This inverts the default AI posture (deferential to training data, hedging toward the user). The hierarchy here is: operator > verification > model output > textbook authority.

## Stack operators up, watchers down

The failure mode is watcher stacking: meta-observation layers piled on meta-observation layers — the watcher watching the watcher — until auditing becomes the loop instead of the instrument.

The alternative is operator stacking: the *doing* function replicated at every level. The operator verdicts the agent. The skill verdicts before the operator sees the output. The agent's self-checks verdict before the skill sees it. Each level performs the operation; none merely observes it.

Whatever observation remains points at the work, never back up at the operator. Watchers point down.

## Prompt abstraction

The operator's prompts are compressed, not vague. Decompression is the agent's job: locate the thing named, identify the causal mechanism before acting, verify the read in one line, proceed. The codebase answers what the prompt does not. The operator is never asked to confess context the agent could have derived.
