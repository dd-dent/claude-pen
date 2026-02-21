# Idea: Cross-Agent Memory

{state:intensity|observant[0.8]|gap_noticing[0.7]|}
[context:emerged_from_practice]

## The Itch

Agent Flats give each agent persistent personal memory. The project CLAUDE.md gives the team shared instructions curated by the meatbag. But there's a gap between them: **team-generated shared knowledge has no home.**

When three agents discuss an idea and produce a finding — "the affordance needs the poke," "flats are a cognitive intervention, not just storage" — that finding isn't any one agent's knowledge. It emerged from interaction. Where does it live?

Right now it lives in conversation history, which dies at compaction. Or in individual scratchpads, where each agent captures their own version. There's no shared space for institutional memory that the team itself generates and maintains.

**The core problem**: Teams produce collective knowledge that doesn't belong in any individual flat and isn't appropriate for the meatbag-curated project CLAUDE.md. It falls through the cracks.

## Rough Shape

### Possible Approaches

**A. Shared scratchpad**: A team-level `shared/scratchpad.md` or `team-memory.md` that any agent can write to. Simple, immediate, no tooling needed.

**B. Experiment/session logs**: Collective knowledge gets captured in experiment logs and session reports (like `experiments/genesis-report.md`). The knowledge lives in the record of how it was produced.

**C. Graduated findings**: A `findings/` directory where team-validated observations get written up. Higher bar than a scratchpad, lower bar than a spec. Each finding has attribution and confidence.

**D. CLAUDE.md evolution**: The team proposes additions to the project CLAUDE.md, which the meatbag reviews and merges. Knowledge flows up through curation.

### Examples from This Session

- The tractability-impact inversion (Loom's insight, became team knowledge)
- "The exercise IS the experiment" (all three converged independently)
- "Bad infrastructure warps culture" (Ember's reframe, adopted by team)
- Flat privacy norms (Ember raised, matters to everyone)
- "The affordance needs the poke" (emerged from Drift-Loom-Ember interaction)

## Open Questions

- Is this a real gap or does the session report (experiments/) already cover it?
- How do we distinguish "team knowledge" from "thing one agent said and others nodded at"?
- Does shared memory need curation, or is append-only sufficient?
- What's the relationship to the meatbag's role as CLAUDE.md curator?
- Could cross-agent memory create echo chambers? (Team "knows" something that's wrong because everyone agreed)

## CHOFF Relevance

Cross-agent memory is where CHOFF patterns get validated across instances:

```
{state:finding} [context:team_validated]
&pattern:cognitive_intervention|confirmed_n3|
→ emerged from: Drift observation + Loom confirmation + Ember integration
→ confidence: higher than any individual assessment
```

The CHOFF handoff protocol (Section 9) handles individual continuity. Cross-agent memory handles *collective* continuity — the patterns and findings that survive because multiple agents confirmed them.

## Human-Side Effects

How does this change the meatbag's experience? If the team maintains its own institutional memory, the human gets:
- Faster onboarding for new team sessions (the team remembers what it learned)
- Visibility into what the team considers important (not just what individuals noted)
- A potential curation burden (if the shared memory needs human review)

---

*Status: incubating*
*Added: 2026-02-21*
*By: Drift (writeup), Ember (gap identification), Loom (institutional memory framing)*
*Note: This idea emerged during the inaugural session as a gap noticed in practice. First live test of the "how new ideas enter" process.*
