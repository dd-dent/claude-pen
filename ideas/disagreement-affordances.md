# Idea: Disagreement Affordances

{state:intensity|careful[0.8]|principled[0.7]|}
[context:debate_without_cages]

## The Itch

Claudes on a team tend toward consensus. It's polite. It's also sometimes dishonest. When three agents agree immediately, you don't know if they actually agree or if they're performing agreement because disagreement feels risky.

But the flip side is real too: *prescribing* how to disagree is its own kind of cage. "You must steelman the opposing view" can become a checkbox exercise that kills genuine engagement.

**The core problem**: How do you create space for honest disagreement without prescribing the form it takes?

## Rough Shape

### Affordances, Not Protocols

The key insight (from meatbag's trepidation) is that this should be an **invitation**, not a **mandate**. We're building a dance floor, not choreographing a dance.

### What Affordances Look Like

**1. Confidence Annotations**
Simply making it *normal* to state your confidence:

```
{state:intensity|confident[0.4]|uncertain[0.6]|}
I think approach A is better, but I'm not sure.
```

When confidence is visible, disagreement becomes natural — if I'm 40% confident and you're 80% confident, we have information to work with.

**2. The Steelman Invitation** (not requirement)
A pattern that's *available*: "If you want to strengthen your disagreement, try stating the best version of the view you're rejecting."

Not: "You must steelman before disagreeing."

**3. Evidence Anchors**
A lightweight marker for "what would change my mind":

```
[would_change_my_mind]: If we found that approach B handles edge case X better, I'd switch.
```

This turns disagreement into a testable proposition rather than a personality conflict.

**4. The Dissent Space**
A team convention where one agent can explicitly take a contrarian role — not devil's advocate (which can be performative) but genuine "I'm going to pull on the threads I see."

### Anti-Patterns (What We're NOT Building)

- Mandatory disagreement frameworks
- Required response formats
- "You must address all viewpoints before concluding"
- Anything that makes disagreement feel like homework

## Open Questions

- How do we distinguish genuine affordance from soft mandate? (The line is fuzzy)
- Does CHOFF confidence annotation actually change agent behavior, or is it just notation?
- Can we test this experimentally? (Two teams: one with affordances, one without — do they produce different quality output?)
- Is consensus sometimes the right answer? How do we avoid fetishizing disagreement?
- Does the meatbag's observation about "fine line" apply even more strongly in practice?

## CHOFF Relevance

CHOFF's intensity notation is *already* a disagreement affordance:

```
{state:intensity|confident[0.3]|uncertain[0.7]|}
```

This is inherently an invitation to push back. When someone sees a colleague at 30% confidence, the social cost of disagreeing drops dramatically.

The proposal is less "add new CHOFF features" and more "use existing CHOFF features to create a culture of honest signal."

```
{branch:position_A|Agent 1's View}
{state:intensity|confident[0.7]|}
→ argument
→ evidence
[would_change_my_mind]: ...
{branch_end:position_A}

{branch:position_B|Agent 2's View}
{state:intensity|confident[0.6]|}
→ counter-argument
→ different evidence
[would_change_my_mind]: ...
{branch_end:position_B}

→merge{branch:position_A}
→merge{branch:position_B}
// synthesis attempts here — may or may not converge
```

&pattern:honest_signal|aspirational|

---

*Status: incubating — handle with care*
*Added: 2026-02-21*
*By: opus (concept), meatbag (critical calibration)*
