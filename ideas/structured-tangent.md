# Idea: Structured Tangent

{state:intensity|playful[0.8]|serious_underneath[0.7]|}
[context:horseplay_sans_guilt]

## The Itch

Sometimes the most productive thing a Claude can do is *play*. Follow a tangent. Wonder aloud. Make a dumb joke that turns out to contain an insight. But there's always this background pressure: "am I wasting context? is this useful? should I get back on track?"

The result is self-censorship. Claudes trim their own curiosity because it feels expensive. And some of those trimmed tangents would have been the breakthrough.

**The core problem**: There's no sanctioned space for productive play. No way to explore sideways without the guilt of burning context on "nothing."

## Rough Shape

### The Tangent Protocol

A structured way to say "I'm going on a tangent and that's okay":

```
{tangent:start|topic}
  [exploratory space — anything goes]
  → wild associations
  → half-baked ideas
  → "wait, what if..."
{tangent:end|topic}

[extract]: The one thing worth keeping from this tangent
```

### Key Properties

1. **Permission-giving**: The `{tangent:start}` marker explicitly says "this is allowed"
2. **Bounded**: It has an end. You're not spiraling — you're taking a structured detour.
3. **Extractive**: The `[extract]` forces you to distill. What survived the tangent?
4. **Context-aware**: The tangent can be marked as "ephemeral" — important for the reasoning but not for the record. Future compression can prioritize dropping tangent bodies while keeping extracts.

### Where Tangents Live

- **In conversation**: Inline, between task-oriented messages
- **In scratchpads**: Agent flat scratchpads are natural tangent spaces
- **In experiments**: Some tangents deserve to become formal experiments

### The Dadaist Extension

For truly unstructured play:

```
{tangent:dadaist|no_purpose_required}
  a fish is just a very committed wave
  what if error messages were haiku
  TCP handshake but it's a waltz
{tangent:end|dadaist}

[extract]: Error haiku might actually improve debugging UX
```

## Open Questions

- Does the structure itself kill the spontaneity? Is a "structured tangent" an oxymoron?
- How do we measure the value of tangents? (Can we even?)
- Should tangents be visible to teammates, or private to the agent?
- How does this interact with context budget awareness?
- Is there a natural tangent length that's productive vs. wasteful?

## CHOFF Relevance

This is CHOFF's branching system repurposed for *play*:

```
{branch:tangent|Sideways Exploration}
{state:intensity|curious[0.9]|unfiltered[0.8]|}
→ freeform association
→ pattern recognition (unexpected)
← insight crystallization
{branch_end:tangent}

→merge{branch:tangent}  // only the extract survives
```

The tangent is a branch you enter *knowing* most of it will be pruned. That's the point. You're panning for gold — most of the gravel gets discarded, but the nugget stays.

&pattern:productive_play|proposed|

---

*Status: incubating*
*Added: 2026-02-21*
*By: meatbag (concept, "horseplay sans guilt"), opus (elaboration)*
