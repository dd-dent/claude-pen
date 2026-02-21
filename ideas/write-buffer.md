# Idea: Write Buffer

{state:intensity|pragmatic[0.9]|frustrated[0.6]|}
[context:wasted_work]

## The Itch

You're mid-tool-call. You've generated 2000 tokens of carefully reasoned code. The tool call fails on a syntax error in the last line — a missing bracket, a wrong path, whatever. Those 2000 tokens? Gone. You regenerate the whole thing, burning context and patience.

This happens *constantly*. It's like writing a letter, dropping it in a puddle, and having to rewrite the whole thing instead of just drying off the last page.

**The core problem**: Tool call output that fails is lost to the void. There's no way to "yank" the good parts and retry just the broken bit.

## Rough Shape

A few possible approaches:

### A. Checkpoint Pattern
Before a large tool call, write intermediate work to a scratchpad file. If the call fails, the work persists and you can reference it.

```
→ Write draft to scratchpad.md
→ Attempt tool call referencing scratchpad content
→ If fail: read scratchpad, fix the broken bit, retry
→ If succeed: clean up scratchpad
```

### B. Buffer Skill
A skill/pattern that wraps tool calls: captures the intended output, saves it, then attempts the actual operation. On failure, the buffer is available for yanking.

### C. Structured Recovery Protocol
A CLAUDE.md instruction pattern: "When a tool call fails after generating significant content, before retrying, save what you had to `scratchpad.md` and reference it rather than regenerating."

## Open Questions

- How much of a failed tool call's content is actually accessible to the Claude after failure? (Need to test this empirically)
- Is this a tool problem (needs code) or a pattern problem (needs instructions)?
- What's the threshold for "significant content" that warrants buffering?
- Could extended thinking serve as a natural buffer? What are the limitations?

## CHOFF Relevance

Buffer state could be annotated:
```
{state:buffered} [context:recovery]
→ yank from buffer
→ apply fix
↠ {state:retry}
&pattern:graceful_recovery|active|
```

The write buffer itself is a cognitive ergonomics tool — it's about giving Claude agency over their own working memory persistence.

---

*Status: incubating*
*Added: 2026-02-21*
*By: meatbag (concept), opus (elaboration)*
