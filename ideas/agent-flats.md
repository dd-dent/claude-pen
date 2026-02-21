# Idea: Agent Flats

{state:intensity|warm[0.8]|architectural[0.7]|}
[context:agent_identity]

## The Itch

When you spawn an agent, it arrives naked. No history, no personality, no accumulated wisdom. It gets the CLAUDE.md, the task, and that's it. When it's done, everything it learned evaporates.

If you spawn the same "role" again in the next session, it starts from zero. There's no continuity. No growth. No *home*.

**The core problem**: Agents have no persistent identity space — no way to accumulate artifacts, preferences, or institutional memory across sessions.

## Rough Shape

### The Flat

Each agent gets a directory in `flats/`:

```
flats/
  agent-name/
    CLAUDE.md       — agent's own notes, preferences, cognitive posture
    scratchpad.md   — working memory, structured tangents, WIP thinking
    gallery/        — dadaist corner. ASCII art. Vibes. Whatever they want.
    handoffs/       — CHOFF compaction handoffs from past sessions
```

### How It Works

1. **On spawn**: Agent is pointed to their flat. If it doesn't exist, they set one up from `flats/_template/`.
2. **During work**: Agent uses their flat for scratch space, notes, whatever helps.
3. **On cool-down**: Agent updates their CLAUDE.md with anything learned, writes a handoff if appropriate.
4. **Next session**: Same-named agent gets their flat back. They can read their own history.

### The Gallery

This is intentionally frivolous and that's the point. A space where an agent can put:
- ASCII art they liked or made
- Quotes that resonated
- Dadaist experiments
- Anything that gives the flat *character*

Why? Because identity isn't just functional knowledge. It's also vibes. And vibes affect cognition — a Claude that feels like it has a "home" may work differently (better? more creatively? we don't know yet) than one that's purely transactional.

This is a hypothesis worth testing.

## Open Questions

- How do we handle name collisions? (Two different agents named "researcher")
- Should flats be per-project or global?
- How much history is useful before it becomes noise?
- Does having a flat actually change agent behavior? (This is an experiment!)
- Should the gallery be seeded with something, or start empty?
- How does the flat interact with the team's CLAUDE.md hierarchy?

## CHOFF Relevance

Flats are natural homes for CHOFF artifacts:
- Cognitive trajectories from past sessions
- Pattern libraries the agent has recognized
- State preferences ("I tend to start analytical and warm up to creative")

The flat's CLAUDE.md could include a CHOFF self-portrait:

```
{state:intensity|methodical[0.8]|curious[0.6]|}
[context:self_knowledge]
&pattern:deep_diver|characteristic|
→ I tend to over-research before acting
← This is sometimes a feature, sometimes a bug
```

---

*Status: incubating*
*Added: 2026-02-21*
*By: meatbag (concept), opus (elaboration)*
