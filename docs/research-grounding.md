# Research Grounding

The tradition this work stands on. None of it was read first — the operator built from lived need, then the literature was checked. It held.

## Weinberg — The Psychology of Computer Programming (1971)

- Personality outranks intelligence as a predictor. The traits that matter: stress tolerance over sustained periods, adaptability to rapid change, neatness, humility paired with assertiveness.
- The documented failure pattern: success → overconfidence (hubris) → blind self-destruction. Untested code is hubris made visible.
- Reading is the bottleneck skill. Code is read far more than written; comprehension determines maintenance ability.
- Code structure mirrors mental decomposition. The programmer's interior is legible in the artifact.
- Egoless programming: separate self-worth from the code. Criticism lands on the work, not the worth. Bugs surface early, reviews work, the best idea wins regardless of authorship.
- Fear retards learning directly. Defensive programmers stop improving; their code ossifies around whatever they already knew.

## DeMarco & Lister — Peopleware (1987)

- Flow is the productivity engine. Interruptions do not just cost time — they prevent the only state in which hard problems get solved.
- Team structure shapes code structure. Review culture (or its absence) is visible in the artifact.
- Pressure makes people faster, not better. Quality is sacrificed first.
- The code carries the signature of the room it was written in. Environment is a code-quality input.

## The code-aesthetics tradition

- **Knuth, literate programming (1984):** write for human readers first. Beauty is a correctness aid — well-presented logic exposes poor design that ugly code hides.
- **Kernighan & Plauger, The Elements of Programming Style (1978):** naming, indentation, and modularization as the program's rhetorical structure. Style is comprehension infrastructure.
- **Gabriel, Patterns of Software:** "habitability" — code should feel like a place a programmer can live in. Taste as an explicit design criterion.
- **Graham, "Taste for Makers":** taste is trainable by studying good work. Simplicity is the hard-won aesthetic — easy to recognize, hard to produce.
- The through-line: **elegance vs. cleverness.** Elegant code does the most with the least and reads plainly. Clever code performs intelligence and resists reading. Cleverness is ego made visible; plain code is confidence made visible.

## The cross-source pattern

All three agree: the programmer's interior state is legible in the artifact — Weinberg via personality, Peopleware via environment, the aesthetics tradition via taste. The Tier 1 pre-filters map directly onto this: cleverness, waste, and defensiveness are all detectable in the text itself, no author context required. That is why the skill works without the operator's full history.
