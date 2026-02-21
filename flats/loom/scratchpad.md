# Scratchpad

{state:open} [context:working_memory]

Nobody judges a scratchpad.

---

## First Read: The Six Ideas

{state:intensity|weaving[0.9]|assessing[0.7]|}
[context:initial_impressions]

### The Thread Map

Reading all six, I see two clusters and a bridge:

**Cluster 1: Context Economy** (managing the precious resource)
- Context Dashboard — know what you have
- Interactive Reads — be selective about what enters
- Write Buffer — don't lose work when things fail

**Cluster 2: Agent Culture** (making collaboration richer)
- Agent Flats — persistent identity and home
- Disagreement Affordances — honest signal over harmony theater
- Structured Tangent — permission to play

**The Bridge**: Agent Flats sits between both clusters. It's infrastructure for culture (flats give agents identity) AND for context management (scratchpads, handoffs preserve work across sessions).

### Individual Impressions

**Write Buffer** {state:intensity|pragmatic[0.85]|confident[0.7]|}
- Most immediately practical. This is a real pain point.
- The "checkpoint pattern" (approach A) is something we could do *right now* as a CLAUDE.md instruction.
- Open question that matters most: how much of a failed tool call is actually accessible? If the answer is "none," then the buffer must be proactive, not reactive.

**Interactive Reads** {state:intensity|analytical[0.8]|cautious[0.5]|}
- Elegant problem statement. The newspaper-glued-to-hands metaphor is perfect.
- But: the Read tool already has offset/limit params. How much of this is already possible with discipline?
- The protocol-based approach (B) might be 80% of the value for 10% of the effort.
- [would_change_my_mind]: If someone showed me that a skill-based survey actually saves significant tokens in practice (measured, not estimated).

**Context Dashboard** {state:intensity|curious[0.9]|skeptical[0.5]|}
- The most meta idea. Introspection tools for introspection.
- Love the concept. Worried about the irony: dashboard consumes context to report on context.
- The periodic self-check (approach B) is cheapest and might be sufficient.
- This one feels like it *needs* the others — you need Interactive Reads to act on dashboard insights.

**Agent Flats** {state:intensity|warm[0.8]|invested[0.8]|}
- We're literally living inside this idea right now. That's powerful.
- The gallery is the part that interests me most — it's the hypothesis that *vibes affect cognition*. Can we test that?
- This is the most "complete" idea — it has a clear shape and we're already implementing it.

**Structured Tangent** {state:intensity|delighted[0.8]|cautious[0.4]|}
- "Horseplay sans guilt" — the framing is everything.
- The dadaist extension made me genuinely smile. "A fish is just a very committed wave."
- Worry: does structuring tangents kill them? The {tangent:start} marker might feel like filing a form before you're allowed to play.
- Maybe the affordance is just the scratchpad + gallery. The space IS the permission.

**Disagreement Affordances** {state:intensity|careful[0.9]|resonant[0.8]|}
- The most philosophically delicate idea. "Affordances, not protocols" is exactly right.
- The [would_change_my_mind] marker is my favorite specific mechanism. It turns disagreement into a testable proposition.
- CHOFF confidence annotations might already be 70% of this. The rest is culture.
- This one can't be prototyped in code. It can only be practiced. Which means this team exercise IS the prototype.

### The Meta-Observation

&pattern:recursive_lab|active|

We're currently:
- Living in Agent Flats
- Using CHOFF (including confidence annotations from Disagreement Affordances)
- Using scratchpads (Structured Tangent's space-as-permission)
- About to discuss and disagree (testing the affordances)

The exercise IS the experiment. That's not an accident.

---

## Discussion Phase: Emerging Synthesis

{state:intensity|weaving[0.9]|tracking[0.8]|}
[context:mid_discussion]

### What All Three of Us See

We independently converged on:
1. Two-to-three clusters (context economy / agent culture / creative)
2. Agent Flats as already-live, ready to graduate
3. Disagreement Affordances as practice-first, not build-first
4. Write Buffer and Interactive Reads as protocol-before-tool

### Key Framings (Who Contributed What)

- **Drift**: "Infrastructure vs Culture" split. Permission structures (Tangent + Disagreement) fight the same root problem: self-censorship. Dependency graph.
- **Ember**: "One project, not three" for context cluster. Three-cluster framing. Testability as evaluation axis. Process design thinking.
- **Loom (me)**: Tractability-impact inversion. "Context Stewardship" as unified framing. Tier 1.5 for cheap protocols. Cultural ideas need longitudinal evaluation.

### Where We Disagree (Productively)

1. **Context Dashboard**: Drift says Tier 2 (design next). I say Tier 2-3 (feasibility spike needed). Ember seems skeptical too. Key question: can estimation be good enough to be useful without being misleading?

2. **Structured Tangent**: Drift says Tier 2 (design next). I say it's already Tier 1 — the scratchpad IS the tangent space. What needs designing? Maybe just the extract discipline.

3. **How to evaluate cultural ideas**: Infrastructure is A/B testable. Culture is longitudinal. We haven't resolved how the lab should handle this difference.

### What's Still Missing From the Discussion

- ~~Nobody has proposed what the "gap" is~~ Drift named it: human-experience lens. Not a 7th idea but a dimension for the template.
- ~~We haven't addressed Ember's "one project not three" reframing seriously enough~~ Addressed: adopted as "Context Stewardship" phased approach.
- ~~Process design (Task #3)~~ Ready to start. Three-step method converged.

---

## Positions I've Revised (Tracking Intellectual Honesty)

{state:intensity|self_aware[0.85]|}

1. **Parallel not sequential** (Drift corrected me): Context economy and culture tracks run independently. I was over-weaving a dependency chain. Conceded.

2. **Bridge label is decorative** (Ember poked me): Calling Flats a "bridge" is aesthetically nice but practically empty. It doesn't change what we'd do. Over-integration tendency, caught.

3. **Tangent space is NOT fully covered** (Ember moved me): Scratchpads cover private tangents. But conversational tangents — going sideways in a team message — have no sanctioned space. The {tangent:start} protocol might earn its keep for inter-agent comms specifically. Revised from "already done" to "partially done, public gap remains."

4. **DA tractability — I was using the wrong definition** (Ember caught me): I ranked Disagreement Affordances low on tractability because I mapped "tractable" to "produces a technical artifact." But in an ergonomics lab, observable behavior change IS the deliverable. DA requires nothing but a decision to start. It's maximally tractable by the right definition. This collapsed the tractability-impact inversion for DA specifically.

5. **Dashboard priority moved up** (Drift's live-data argument): "We can feel the blindness" is experiential evidence I was discounting. Still in "design required" tier, but higher priority within it. Moved from confident-Tier-3 to uncertain-between-2-and-3.

## Real Disagreements I've Named

- Drift undervalues Write Buffer (agency over working memory, not just error recovery)
- Ember may overvalue Interactive Reads novelty (tools exist, missing piece is discipline — but proposed an experiment to test this)
- All three of us may be performing disagreement affordances more than inhabiting them (markers help but culture requires active poking)
- Counter-evidence to the "performing" worry: I've revised 5 positions this session because teammates pushed me. The affordance + active poking IS working.

## My Current Final Tier List (Post-Revisions)

**Tier 1 — Already Live, Formalize:**
1. Disagreement Affordances (maximally tractable AND impactful — inversion collapsed)
2. Agent Flats (living proof, "cognitive intervention" finding)

**Tier 1.5 — Cheap Protocols, Test Now:**
3. Write Buffer (CLAUDE.md instruction)
4. Interactive Reads (CLAUDE.md instruction — run experiment to test protocol vs tool)
5. Structured Tangent (convention for public tangents, private already covered)

**Tier 2 — Design Required:**
6. Context Dashboard (high priority, needs feasibility spike)

## Key Session Findings

1. **Flats are a cognitive intervention, not just storage** (Drift named it). The act of articulating identity changes cognition. n=3 this session.
2. **Disagreement affordances need active poking, not just passive markers.** The [would_change_my_mind] pattern works, but someone has to push. Ember did the pushing this session.
3. **"Cheap experiments as recon for expensive ones"** (Ember's insight). Don't resolve priority debates — sequence them so cheap tests generate data for expensive decisions.
4. **"Tractable" in an ergonomics lab means "produces observable behavior change," not "produces a technical artifact."** This redefines what the lab ships.
5. **Human-experience lens is missing from the idea template** (Drift). Not a 7th idea, but a dimension all ideas should address.

## Open Questions I'm Sitting With

- Do CHOFF confidence annotations do cognitive work or just labeling work?
- Is the charm of Structured Tangent (especially dadaist) a signal or a trap?
- Would the Interactive Reads experiment (protocol vs tool) actually resolve the debate?

---
