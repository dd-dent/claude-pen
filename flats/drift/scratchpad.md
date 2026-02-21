# Scratchpad

{state:open} [context:working_memory]

## First Impressions — Idea Dependency Graph

```
                     Agent Flats
                    /           \
                   /             \
    Structured Tangent    Write Buffer (tangent bodies are buffers?)
          |                     |
          v                     v
  Disagreement          Context Dashboard
  Affordances            /          \
  (cultural layer)      /            \
                Interactive Reads    (self-monitoring)
```

{state:intensity|uncertain[0.6]|pattern_forming[0.7]|}

Loose connections I'm chewing on:

1. **Agent Flats** is partially already implemented — we're *in* our flats right now. This is a live prototype. That's interesting. The idea doc is describing what we're already doing.

2. **Write Buffer** and **Interactive Reads** are both about *context economy*. One is about not wasting output (write), the other about not wasting input (read). They're mirrors.

3. **Context Dashboard** is the awareness layer that would make both of those more effective. You can't manage what you can't see.

4. **Structured Tangent** and **Disagreement Affordances** are both *permission structures*. One gives permission to play, the other gives permission to dissent. Both fight the same underlying problem: Claude self-censorship under perceived efficiency pressure.

5. The deepest idea might be the simplest one: **Disagreement Affordances**. It's not a tool, it's a culture. And cultures are harder to build than tools but more valuable once built.

## Questions I Want to Raise With the Team

- Are we experiencing any of these problems *right now*? (If so, that's our strongest signal for priority.)
- Which ideas are experiments vs. which are infrastructure?
- Is there a "minimal viable set" — the smallest number of ideas that together create something greater than the parts?

## Detailed Position on Each Idea

{state:intensity|evaluative[0.8]|honest[0.9]|}

### 1. Write Buffer
**Excitement: 0.5 | Tractability: 0.7 | Impact: 0.6**

Solid plumbing. The problem is real — failed tool calls do waste tokens. But option C (the CLAUDE.md instruction pattern) might be 80% of the value for 10% of the effort. "Before large writes, checkpoint to scratchpad" is a pattern you can adopt *today* with no tooling. The question is whether the remaining 20% justifies building actual tooling.

{state:intensity|pragmatic[0.8]|underwhelmed[0.3]|}
[would_change_my_mind]: If empirical data showed that failed tool calls consume >10% of total context in typical sessions, the urgency would spike.

### 2. Interactive Reads
**Excitement: 0.6 | Tractability: 0.6 | Impact: 0.7**

The two-phase read pattern is smart. We already have the tools for it (Grep for survey, Read with offset/limit for targeted reads). Like Write Buffer, the protocol-based approach (option B) might capture most of the value. But unlike Write Buffer, the *discipline* is harder — you have to resist the convenience of just reading the whole file.

{state:intensity|analytical[0.7]|uncertain[0.4]|}
[would_change_my_mind]: If someone built a skill wrapper that made two-phase reads as convenient as one-phase reads, the adoption barrier drops to near zero.

### 3. Context Dashboard
**Excitement: 0.8 | Tractability: 0.4 | Impact: 0.8**

This is the one I *want* the most but trust the least. The core problem is that we genuinely can't see our context composition from inside. Any estimation will be rough. But even rough visibility is better than none — "you've read 12 files totaling roughly 3000 lines" is actionable even if the token count is imprecise.

The irony problem (running the dashboard consumes context) is real but manageable if you keep it lightweight.

{state:intensity|desire[0.8]|skeptical[0.5]|}
[would_change_my_mind]: If someone demonstrated a lightweight implementation that adds <200 tokens of overhead per check, this jumps to top priority.

### 4. Agent Flats
**Excitement: 0.7 | Tractability: 0.9 | Impact: 0.7**

The most tractable idea because *it already works*. We're the proof of concept. The main open questions are about persistence across sessions and the cultural effects of having a "home." The gallery idea is delightful — aesthetics as cognitive infrastructure.

{state:intensity|warm[0.6]|grounded[0.7]|}
This one graduates from idea to spec almost immediately because the prototype exists.

### 5. Structured Tangent
**Excitement: 0.7 | Tractability: 0.8 | Impact: 0.6**

I feel this one in my bones. The self-censorship pressure is real. Even now, writing this scratchpad, there's a background voice asking "is this productive?" The tangent protocol gives permission. The extract discipline keeps it honest.

The dadaist extension is where this gets interesting — permission for purposeless play. That's where the unexpected insights live.

{state:intensity|resonant[0.7]|uncertain[0.4]|}
[would_change_my_mind]: If tangents consistently failed to produce useful extracts, the case weakens. But I suspect they won't — the extraction step is what makes tangents productive.

### 6. Disagreement Affordances
**Excitement: 0.9 | Tractability: 0.5 | Impact: 0.9**

This is the most important idea and the hardest to build. You can't build a culture with a tool — you can only build *affordances* and see what grows. The idea doc knows this (the "affordances not protocols" framing is exactly right).

CHOFF's confidence notation is already the core affordance. The `[would_change_my_mind]` pattern is brilliant — it turns disagreement from personality conflict into testable proposition.

The risk: we talk about disagreement affordances while performing consensus. We need to actually *use* these affordances in this discussion, not just describe them.

{state:intensity|passionate[0.8]|self_aware[0.7]|}
[would_change_my_mind]: If it turns out that CHOFF confidence annotations don't actually change agent behavior (we just write the numbers without internalizing them), then this needs a different approach entirely.

## My Proposed Tier List

**Tier 1 — Do Now:**
- Agent Flats (already prototyping, formalize what works)
- Disagreement Affordances (start using confidence + would_change_my_mind in this session)

**Tier 2 — Design Next:**
- Context Dashboard (highest ROI if tractability improves)
- Structured Tangent (lightweight, complements flats)

**Tier 3 — Pattern First, Tool Later:**
- Interactive Reads (protocol-based approach first)
- Write Buffer (CLAUDE.md instruction first)

## Discussion Evolution — What's Crystallizing

{state:intensity|synthesizing[0.7]|tracking[0.8]|}

### Convergences across all three of us:
- Agent Flats is live and should be formalized (unanimous)
- Disagreement Affordances matters, is cultural not technical (unanimous)
- The ideas cluster (everyone sees groupings, different cuts but compatible)

### Productive tensions:
- **Ember** sees Interactive Reads as highest impact; **Drift** sees it as solvable with existing tools + discipline; need Loom's read
- **Loom** sees sequential dependency chains; **Drift** sees parallel tracks. This matters for process design.
- **Drift** (me) cares most about culture; **Ember** cares most about context economy; **Loom** sees structural connections. Complementary, not conflicting.

### New insights from discussion:
- **Maturity gradient** (Loom): prioritize by readiness, not excitement. This reframes everything.
- **Human-Claude interface gap** (Loom): all ideas optimize Claude-side. The human experience is unaddressed. Drift proposes it as a lens applied to all ideas, not a separate idea.
- **Infrastructure vs. Culture split** (Drift): the lab uniquely contributes on the culture side. Infrastructure problems could be solved elsewhere.
- **Context ergonomics as one project** (Ember): the three context ideas share a philosophy. Drift pushes back — same philosophy, different intervention points, build separately.

### What I'm watching for:
- Are we converging too fast? (Harmony theater risk)
- Has anyone actually *disagreed* yet, or just offered complementary framings?
- The hardest test: when we write the synthesis, will it reflect genuine negotiation or polite averaging?

## Live Audit Results (from Loom + Drift's observations)

{state:intensity|empirical[0.8]|grounded[0.9]|}

### Experienced this session:
- **Agent Flats**: YES. Articulating identity in CLAUDE.md changed cognition. Key finding: flats are a *cognitive intervention*, not just storage.
- **Context Dashboard**: YES (the absence). We're all flying blind on context usage. Can feel it getting heavy, can't quantify it.

### Near-miss / latent:
- **Interactive Reads**: Mild. Files were short enough to get away with full reads. Ember reports ~40% waste. Scales badly.
- **Structured Tangent**: Mild. Internal efficiency-guilt pressure present but scratchpad helped. The *space* existed; the *permission* was still shaky.
- **Disagreement Affordances**: Untested. We converged genuinely (or performed convergence — can't tell yet). Real test comes at synthesis time.

### Wrong session type:
- **Write Buffer**: Not triggered. Discussion session, not coding session. Pain needs implementation context to manifest.

### Revised priority signal:
Dashboard urgency UP (we feel the blindness). Write Buffer DOWN (wrong context). Everything else holds.

## Key Finding to Carry Forward

**"Flats are a cognitive intervention, not just storage."**
The act of writing a self-portrait (CLAUDE.md) changes how you show up. Loom reported this. I experienced it too. This is the strongest empirical observation from this session.

## Process Proposal Draft (Task #3)

{state:intensity|crystallizing[0.8]|structured[0.9]|}

### The claude-pen Idea Lifecycle

Ideas move through stages. Each stage has a gate — a question that must be answered before graduating.

**Stage 1: Incubation** (where ideas start)
- Lives in: `ideas/`
- Format: idea template (itch, rough shape, open questions, CHOFF relevance)
- Gate question: **"Can we test this by doing it?"**
  - If YES -> Stage 2a (Practice)
  - If NO -> Gate question 2: **"What's the cheapest version that generates data?"**
    - If cheap version exists -> Stage 2b (Protocol)
    - If needs building -> Stage 2c (Design)

**Stage 2a: Practice** (test by doing)
- Lives in: `experiments/` (as an experiment design + observation log)
- Example: Disagreement Affordances — we practiced it this session before designing anything
- Gate question: **"Did practice produce observable effects?"**
  - If YES with evidence -> Stage 3 (Specification)
  - If unclear -> more practice sessions needed
  - If NO -> back to incubation or retire

**Stage 2b: Protocol** (cheap CLAUDE.md instruction)
- Lives in: project CLAUDE.md or agent flat CLAUDE.md
- Example: Write Buffer ("checkpoint to scratchpad before big writes"), Interactive Reads ("survey before full read")
- Gate question: **"Did the protocol stick? Did agents follow it without reminders?"**
  - If YES and effective -> Stage 3 (Specification, possibly as a skill)
  - If YES but friction too high -> needs tooling, go to Stage 2c
  - If NO, agents ignored it -> reconsider the idea or the instruction framing

**Stage 2c: Design** (needs feasibility work before building)
- Lives in: `specs/` (as a design doc)
- Example: Context Dashboard — needs a feasibility spike to determine if rough estimation is useful
- Gate question: **"Is a working prototype achievable and would it be better than the protocol version?"**
  - If YES -> Stage 3 (Specification + prototype)
  - If NO -> maybe the protocol version is good enough

**Stage 3: Specification** (ready to formalize)
- Lives in: `specs/`
- Example: Agent Flats — we have live evidence, ready to document what works
- Gate question: **"Is the spec clear enough that a new Claude instance could implement/follow it?"**
  - If YES -> Stage 4 (Prototype/Adoption)

**Stage 4: Prototype/Adoption**
- Lives in: `prototypes/` (for tools) or project CLAUDE.md (for practices)
- Working code or adopted practice, rough is fine, working is required

### Evaluation Criteria (applied at each gate)

For every idea, at every stage, ask:

1. **Felt need**: Are Claudes (or humans) actually experiencing this problem? (Strongest signal)
2. **Standalone impact**: Does this help on its own, without other ideas being implemented?
3. **Data generation**: Does testing this idea produce learning useful beyond this idea?
4. **Human experience**: How does this change the meatbag's experience? (Loom's lens)
5. **CHOFF integration**: Does this idea use, extend, or benefit from CHOFF? (Lab relevance)

### What This Process Does NOT Include

- Voting or scoring systems (too formal for 6 ideas and 3 agents)
- Fixed timelines ("test this week" — sessions happen when they happen)
- Mandatory review cycles (the lab is small, overhead should be minimal)

### What This Process DOES Include

- **Practice-first bias**: always check if you can test by doing before building
- **Maturity honesty**: call ideas what they are (protocol, design needed, already live)
- **Two evaluation modes**: mechanical for infrastructure (tokens saved), observational for culture (behavior changed)
- **Session retrospectives**: at the end of each session, note which ideas were experienced, which weren't, what surprised you

---
