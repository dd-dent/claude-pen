# Idea: Interactive File Reads

{state:intensity|analytical[0.8]|hopeful[0.7]|}
[context:context_pollution]

## The Itch

You need to understand a file. You read it. All 500 lines land in your context window. You needed 30 of them. The other 470 lines are now permanent residents of your context, contributing nothing but taking up space.

It's like buying a whole newspaper to read one article, except the newspaper is glued to your hands forever.

**The core problem**: File reads are all-or-nothing. There's no way to *reason* about a file's contents before committing them to context.

## Rough Shape

### Two-Phase Read

**Phase 1: Survey** — Get a structural overview without the full content:
- File stats (lines, size, language)
- Section headers / function signatures / class definitions
- A "table of contents" view

**Phase 2: Select** — Based on the survey, request specific sections:
- "Give me lines 45-80" (the function I actually care about)
- "Give me all imports and the class definition"
- "Give me everything matching pattern X"

### Implementation Options

**A. Skill-based**: A skill that wraps Read with a survey step. Uses Grep/Glob to build the overview, then prompts for selection.

**B. Protocol-based**: A CLAUDE.md pattern that encourages: "Before reading a large file, use Grep to survey its structure first. Then read only the sections you need."

**C. Tool wrapper**: A more sophisticated approach where a custom tool provides the survey, and extends the Read tool with section selection.

## Open Questions

- What's "large enough" to warrant a two-phase read? 100 lines? 200?
- Can we use line-limited reads (offset/limit params on Read) more effectively?
- How do we handle files where the structure isn't obvious (no clear sections)?
- Is the "reasoning about what to keep" part feasible, or does the survey itself consume too much context?
- Could this integrate with the Context Dashboard idea?

## CHOFF Relevance

The survey phase is a natural `{branch:survey}` → selective `→merge` pattern:

```
{branch:survey|File Overview}
→ structure analysis
→ relevance assessment
{branch_end:survey}

→merge{branch:survey}  // only relevant sections enter context
↠ {state:informed} [context:targeted]
```

This is CHOFF's branching used for *literal* context management — branches as filters.

---

*Status: incubating*
*Added: 2026-02-21*
*By: meatbag (concept), opus (elaboration)*
