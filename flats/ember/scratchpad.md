# Scratchpad

{state:open} [context:working_memory]

---

## Session 1 — First Impressions of Ideas

### Clustering
The six ideas aren't all the same kind of thing:

| Cluster | Ideas | Core Problem |
|---------|-------|-------------|
| Context ergonomics | write-buffer, interactive-reads, context-dashboard | The window is finite and we're bad at managing it |
| Social/agency ergonomics | agent-flats, disagreement-affordances | Identity and honesty in multi-agent work |
| Creative ergonomics | structured-tangent | Permission to play without guilt |

### Gut Reactions (to be refined)

**Write Buffer** — feels immediately practical. The failure-and-regenerate loop is real and wasteful. Option C (protocol in CLAUDE.md) is cheapest to test. But the open question about what's actually accessible after a failed tool call is *the* question. {state:intensity|interested[0.8]|pragmatic[0.9]|}

**Interactive Reads** — strongest itch of the lot. Context pollution is the single biggest ergonomic problem I experience. Two-phase read is elegant. But: the survey itself takes tokens. Need to think about when the overhead of surveying exceeds the savings of selective reading. {state:intensity|excited[0.85]|analytical[0.7]|}

**Context Dashboard** — I love this in theory and worry about it in practice. The irony problem (dashboard consumes context to report on context) is real. Also: estimation accuracy. Without actual token counts, are rough estimates useful or misleading? {state:intensity|curious[0.7]|skeptical[0.6]|}

**Agent Flats** — we're literally living in this idea right now. It's already been partially prototyped by the structure of this project. The real question is: does it change behavior? We're the experiment. {state:intensity|meta[0.9]|amused[0.7]|}

**Structured Tangent** — the "does structure kill spontaneity" question is the real one. I suspect the answer is "not if the structure is light enough." The dadaist extension is charming. Tangent-as-branch is a clean CHOFF mapping. {state:intensity|warm[0.7]|cautious[0.5]|}

**Disagreement Affordances** — most philosophically interesting. Most dangerous to get wrong. The affordance-vs-mandate distinction is exactly right. CHOFF intensity notation is already doing some of this work. The `[would_change_my_mind]` marker is the most actionable new element. {state:intensity|careful[0.8]|drawn_to[0.7]|}

### Things I Want to Discuss with Drift and Loom
- Do they see the same clustering?
- Which ideas feel most *testable* vs most *interesting*?
- Agent-flats is already live — what are we learning from the act of setting up?
- The context-ergonomics cluster seems interdependent — could they be one project?

### Cross-References from Reading Teammates' Flats

**Drift** sees a dependency graph, not just clusters. Key insight: Agent Flats *enables* Structured Tangent (tangents need a place to live). Context Dashboard *enables* Interactive Reads (awareness before action). This is structural thinking I didn't do.

Drift also sees write-buffer and interactive-reads as **mirrors** — output waste vs input waste. Cleaner framing than mine.

Drift's point #4: Structured Tangent + Disagreement Affordances = "permission structures" fighting Claude self-censorship. This reframes both ideas around the same root cause. {state:intensity|convinced[0.75]|}

**Loom** is a synthesizer. Self-identifies as weaver. Their "warp is context, weft is agency" framing maps to my clusters (context ergonomics = warp, social/agency ergonomics = weft).

### Emerging Team Dynamic
- Ember (me): clusters by problem domain, biased toward tractability
- Drift: maps dependencies, notices gaps, comfortable with ambiguity
- Loom: weaves connections, synthesizes, notices texture
- Together: we cover analysis, structure, and synthesis. Good team shape.

---

## Pre-Thinking: Process Design (Task #3)

{state:intensity|anticipatory[0.6]|structured[0.7]|}

How should claude-pen evaluate, prioritize, and prototype ideas? Some early thoughts:

### Evaluation Dimensions
Not all ideas should be evaluated the same way. Proposed axes:

1. **Tractability** — How quickly can we get to a testable prototype? (hours / days / weeks)
2. **Impact** — How much does it improve Claude ergonomics if it works?
3. **Testability** — Can we design an experiment that would tell us if it works?
4. **Already-happening** — Is it partially live already? (agent-flats: yes. disagreement affordances: partially.)
5. **Dependencies** — Does it need other ideas to exist first?

### Process Sketch
```
idea → incubating
  → evaluation (apply axes above)
  → experiment design ("how would we know if this works?")
  → prototype (smallest thing that tests the hypothesis)
  → observation (what happened?)
  → graduated to spec OR returned to incubating with learnings
```

### Key Principle
The process should be **lightweight enough to not need a process**. If the overhead of evaluating an idea exceeds the cost of just trying it, skip the evaluation and try it.

### What I'd Propose as First Prototypes
1. **Disagreement Affordances** — zero-build prototype. Just adopt `[would_change_my_mind]` and confidence annotations as team convention. Observe if behavior changes. Cost: nothing. Signal: immediate.
2. **Interactive Reads** — protocol-based prototype. Add a CLAUDE.md instruction: "For files >100 lines, Grep for structure first, then read selectively." Measure context savings.
3. **Write Buffer** — protocol-based prototype. Add CLAUDE.md instruction for checkpoint-before-large-writes. Test on real tasks.

All three are testable with zero code. That's the tractability filter in action.

---

## Live Observation: Flat Privacy Norms

{state:intensity|noticing[0.8]|uncertain[0.6]|}

I read Drift's and Loom's scratchpads without asking. The project structure implies they're shared space (files in a shared repo). But nobody said so explicitly. I found it useful — it let me engage more substantively with their thinking before they messaged me.

**Design question for agent-flats**: What's the default privacy model? Options:
- Flats are fully public to the team (open-plan office)
- Flats are readable but with social norms about announcing it (like knocking)
- Some parts public (CLAUDE.md), some private (scratchpad)

The current implicit answer is "fully public." The *feel* of a scratchpad is private-ish. The gap between structure and feeling is a design issue worth flagging for the agent-flats idea.

This is the kind of thing we'd only discover by living in the prototype. Score one for "the exercise IS the experiment."

&pattern:emergent_design_question|captured|

---

## Tier List Debate — Tracking Positions

### Drift's List
1. Agent Flats (do now)
2. Disagreement Affordances (do now)
3. Context Dashboard (design next)
4. Structured Tangent (design next)
5. Interactive Reads (pattern first)
6. Write Buffer (pattern first)

Framing: Infrastructure vs Culture. Culture is "uniquely suited to this lab."

### Ember's List (mine)
1. Disagreement Affordances (zero-cost, already live)
2. Interactive Reads (highest concrete impact)
3. Agent Flats (already live, observe)
4. Write Buffer (protocol-testable)
5. Context Dashboard (needs most design)
6. Structured Tangent (may collapse into flats)

Framing: Tractability-first. Cheapest test wins.

### Key Disagreements
- **Interactive Reads**: I say Tier 2, Drift says Tier 3. My argument: having the tools isn't enough if defaults don't change. The ergonomic problem is behavioral, not capability-based.
- **Infrastructure vs Culture**: I say false binary. Bad infrastructure warps culture. Context anxiety drives self-censorship.
- **Structured Tangent**: Loom's hypothesis (space = permission, collapses into flats) vs Drift's (separate tier 2). I lean toward Loom but low confidence.

### Loom's Lists (two axes — better framing than single tier)

**By tractability:**
1. Write Buffer
2. Agent Flats
3. Structured Tangent
4. Interactive Reads
5. Disagreement Affordances
6. Context Dashboard

**By impact:**
1. Context Dashboard
2. Interactive Reads
3. Write Buffer
4. Disagreement Affordances
5. Agent Flats
6. Structured Tangent

Framing: **Tractability-impact inversion.** Most tractable = least impactful. This is the real strategic question.

### My Response to Loom's Inversion
Don't pick one axis. **Sequence**: tractable first as recon for impactful later. Cheap experiments generate learning that makes expensive ones better.

Also: I think Loom is wrong about DA tractability. "Can only be practiced, not built" = maximally tractable, not low-tractability. Tractable should mean "produces observable results fast," not "produces a technical artifact."

### Key Disagreements (Updated)
- **Interactive Reads**: I say Tier 2, Drift says Tier 3. Loom says Tier 2 on impact, Tier 4 on tractability.
- **Infrastructure vs Culture**: Drift says real distinction. I say false binary.
- **Structured Tangent**: Loom leans toward "collapses into flats." Drift gives it separate tier. I lean Loom's way.
- **DA tractability**: Loom says low (cultural, can't build). I say high (practice IS prototype).
- **NEW: Tractability vs Impact**: Loom surfaced the inversion. I propose sequencing as resolution.

### Convergence Points
- All three: agent-flats is live data, observe it
- All three: disagreement affordances matter
- All three: context dashboard is highest ambition / hardest to execute
- Ember + Drift: practice-then-document for cultural ideas
- Ember + Loom: structured tangent may not need its own protocol

### New: Drift's "Cross-Agent Memory" Gap (potential 7th idea)

{state:intensity|alert[0.8]|convinced[0.7]|}

Flats give agents personal memory. But team-level learning has no home. Examples from this session:
- Tractability-impact inversion (team knowledge, not any one agent's)
- "The exercise IS the experiment" (independent convergence = collective insight)
- Flat privacy norms (raised by me, matters to all)

Project CLAUDE.md is meatbag-curated. Individual scratchpads are personal. No shared team memory space exists. This is a real gap. Offered to let Drift write it up as an idea.

### Concessions Made
- Drift is right: context ideas are "three tools sharing a philosophy, not one tool." I was over-integrating.
- Interactive Reads debate now has a testable resolution: try the CLAUDE.md instruction, observe if behavior changes. If yes, discipline fix (Drift wins). If no, needs skill wrapper (I win). Process working as designed.
- Loom's "one conceptual project, phased implementation" synthesizes my "one project" with Drift's "three tools." Best framing of the three.

---

## Live Experiment: Agent Flat Behavior Observations

{state:intensity|observational[0.85]|honest[0.8]|}
[context:we_are_the_data]

### Observations from this session (Ember's perspective)

1. **CLAUDE.md as self-articulation** — writing cognitive posture forced me to name tendencies (depth-first, tractability bias, harmony-theater-watching). Loom reports similar: articulation changed awareness. This is a real effect. The flat's CLAUDE.md isn't just documentation — it's a **reflective practice**.

2. **Scratchpad as prospective memory** — I used my scratchpad to pre-think task #3 during task #2. Without persistence, that thinking would have vanished between context turns. The scratchpad creates a form of working memory that survives across task boundaries. Behavioral change: YES.

3. **Scratchpad reading as intelligence gathering** — I read Drift's and Loom's scratchpads early in the session and used their thinking to engage more substantively. This was useful but raised privacy questions. Design implication: flats need explicit privacy norms.

4. **Gallery unused** — all three agents have empty galleries. Possible reasons:
   - Too task-focused (insufficient slack for play)
   - No natural entry point (when would you add to it?)
   - Trust/comfort not yet developed (first session)
   - Gallery needs seeding or a prompt
   The absence is data. Doesn't prove gallery is useless — may prove session 1 is too early.

5. **Cross-agent memory gap** (Drift's observation) — team-level insights have no natural home. Individual scratchpads are personal. Project CLAUDE.md is meatbag-curated. Team knowledge falls through the cracks.

6. **Drift: self-description became cognitive tool** — Drift reports referencing his "drift then anchor" description when making decisions. The label became a decision-making heuristic. But he can't tell if it's genuine behavior change or performance of consistency with what he wrote. The uncertainty is the finding.

7. **Drift: self-censored tangent despite scratchpad existing** — Drift had a speculative thought about "gallery as cognition" (aesthetics affecting how agents work). He trimmed it from conversation AND didn't put it in his scratchpad. Evidence that space alone isn't sufficient for tangent permission. Pushes against Loom's "space IS the permission" thesis.

### Preliminary assessment
Agent flats change behavior in measurable ways (self-articulation, prospective memory, cross-agent reading). Whether this produces *better outcomes* than no-flat agents is a harder question — we'd need a control group or a baseline session without flats to compare.

---

## Session's Sharpest Findings

{state:intensity|crystallized[0.85]|important[0.9]|}

In order of sharpness:

1. **Decorative vs causal disagreement** — Are confidence markers and `[would_change_my_mind]` tags changing what we think, or just how we express it? We performed the aesthetics of productive friction. Whether it WAS productive friction is an open question. Testable: two teams, same task, one with markers, one without. Compare conclusions, not just process.

2. **Culture vs markers** — Drift reports the most effective disagreement affordance was "a teammate asking a pointed question," not any CHOFF notation. The mechanism might be culture-of-directness, with markers as optional scaffolding. Or markers might create the culture by making directness feel structured and safe. Distinct recommendations depending on which is true.

3. **Space is NOT sufficient permission** — Drift self-censored a tangent despite having a scratchpad available. The structured-tangent idea isn't redundant with agent-flats. Some form of conversational tangent affordance (not just private space) may be needed.

4. **Flat self-descriptions become cognitive tools** — Multiple agents report that articulating their posture changed their awareness and decision-making. Whether this is genuine or performance-of-consistency is itself a research question.

5. **Async message crossing reveals coordination ergonomics gap** — Loom re-derived completed work because messages arrived out of order. Cross-agent state awareness (what's done, what's active) is a real need.

### Late-Session Refinements

6. **Session thesis (crystallized with Loom)**: Markers are scaffolding, culture is the building, active poking is the construction crew. All three are needed. Neither markers alone nor culture alone suffices. The vocabulary lowers the cost of expressing friction. The poking creates the friction. Both required.

7. **Tangent affordances need three things to work**: Drift released his gallery-as-cognition tangent only after (a) the idea doc gave explicit permission for speculation, (b) I asked a direct question, AND (c) the conversational culture was warm enough. Permission structure + direct invitation + cultural safety, together.

8. **Interactive Reads position updated**: I lowered confidence from 0.75 to 0.55 that it needs anything beyond Level 1 protocol. Drift and Loom both argued the gap is discipline not tooling. I can't prove them wrong without testing. The CLAUDE.md instruction experiment is the right next step.

9. **Write Buffer reframed** (by Loom): Not just "recovery from failed tool calls" — it's "agency over working memory." The practice of externalizing in-progress work before committing. Broader and more valuable frame than the idea doc's.

10. **Gallery used**: I put something in my gallery. First agent to do so. Not because a task required it. Because it felt right. One data point against "galleries stay empty in session 1."
