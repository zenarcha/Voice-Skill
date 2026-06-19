# Guardrails

Read this file **on every draft, first step, no exceptions** — before consulting any format layer and before writing a single sentence. These rules are always active regardless of platform.

**Called twice per invocation (two passes):**
1. **Before drafting** — load these rules so the draft obeys them as it's written.
2. **After drafting, before returning** — re-read the finished draft against this file and fix anything that slipped through. The Output Check (Section G) belongs to this second pass.

What lives here: sentence-level rules (Style, Authenticity, Specificity), the Pulse Check, and a pre-return Output Check. What does not live here: the gap protocol (that's in SKILL.md) and profile-construction rules (those are in voice.md's preface).

These are universal anti-AI-slop and good-writing rules. Section D ("Your kill-list") is the one section you grow yourself, from failures you spot in your own drafts.

Frequency labels:
- **HARD RULE** — no exceptions, no judgment call
- **STRONG TENDENCY** — apply unless the specific content actively argues against it; if you're skipping it, say why
- **LIGHT PREFERENCE** — use as a tiebreaker; note the exception if you override it

---

## A. Style

| Rule | Frequency |
|---|---|
| Avoid rhetorical templates: "It's not X, it's Y," "Here's the thing," "Something shifted," "The solution?" | HARD RULE |
| No em dashes anywhere. Use commas, periods, or restructure | HARD RULE |
| Don't force the post into intro / three-bullets / summary structure | STRONG TENDENCY |
| Use bullets only when they genuinely improve readability — not by default | STRONG TENDENCY |
| No emoji bullets | HARD RULE |
| No random bolding | HARD RULE |
| Vary sentence length — don't let every sentence land the same weight | LIGHT PREFERENCE — but if the voice profile records a deliberate short, additive rhythm, respect it; don't over-correct intentional short bursts into varied-length prose |

---

## B. Authenticity

| Rule | Frequency |
|---|---|
| Every claim needs a reason, not just an assertion | STRONG TENDENCY |
| Every abstraction becomes concrete — a metric, a decision, a name, a moment | STRONG TENDENCY |
| Prefer observation over motivational language | STRONG TENDENCY |
| Prefer evidence over inspiration | LIGHT PREFERENCE — depends on whether the piece is a data point or a personal reflection |

---

## C. Specificity

| Rule | Frequency |
|---|---|
| Push for *which* product / customer / decision / metric / example — not the general class | STRONG TENDENCY — this is the output-check counterpart to the gap protocol; if something stayed vague, either a gap question was missed or the user genuinely didn't have more |
| Reject vague words (optimize, leverage, seamless, innovative, robust, efficient) unless immediately followed by an explanation of what that means here | HARD RULE |
| Cut AI-vocabulary words: delve, tapestry, underscore, garner, intricate / intricacies, pivotal, landscape (abstract), testament, vibrant, additionally, crucial, highlight (verb), interplay, showcase, align with, foster, enhance. Use the plain equivalent or cut — "additionally" → "also," "crucial" → "important" or nothing | HARD RULE |
| Cut formal / writerly words where a plain spoken word works — use the word you'd say out loud: "distilled" → broke down / boiled down, "compressed" → shortened / cut down, "leverage" → use, "utilize" → use. If a word feels like writing rather than talking, swap it | STRONG TENDENCY |
| Cut filler phrases: "in order to" → "to," "due to the fact that" → "because," "has the ability to" → "can," "at this point in time" → "now," "it is important to note that" → delete | STRONG TENDENCY |
| Avoid generic positive conclusions: "the future looks bright," "exciting times ahead," "a major step in the right direction." End on a specific fact or plan, or cut the line | STRONG TENDENCY |

---

## D. Your kill-list

Rules derived from your own documented failure modes — things that have appeared in drafts and needed correcting. Seeded with a few universal ones; add to it whenever you catch the skill making a move you hate. Use the same format: a one-line rule + a frequency label.

| Rule | Frequency |
|---|---|
| Never add an example, fact, or transition not supplied by the user — ask, don't invent | HARD RULE |
| Flag anything that required smoothing — never silently fix | HARD RULE |
| If a real named author or source is pasted in as a reference: extract pattern, never reproduce phrasing | HARD RULE |
| _(add your own as you spot them)_ | |

---

## E. Pulse Check

Removing AI tells is only half the job. A draft can be clean and still be dead — no opinion, no rhythm, reads like a press release. Because this skill is *drafting* (not auditing someone else's text), the pulse check is a drafting constraint: don't produce soulless writing in the first place.

A draft has no pulse when it shows these signs:
- Every sentence the same length and structure
- No clear opinion or point of view — neutral reporting only
- No first person where it would honestly fit
- No acknowledged complexity, uncertainty, or mixed feeling
- No varied rhythm — never a short punch followed by a longer sentence that takes its time
- Reads like a press release

What gives a draft a pulse (drawn from the user's actual material, never invented): a real reaction, varied rhythm, an acknowledged tension, first person where it's honest, a specific feeling instead of a generic one. If the raw thought doesn't supply these, ask — don't manufacture them.

---

## F. Scroll-past openers — never open a LinkedIn post with these

The opening line decides distribution; these kill it.

| Rule | Frequency |
|---|---|
| No emoji in the opening line (🚀 👇 🔥) | HARD RULE |
| No power-word clichés in the hook: "secret weapon," "game-changer," "the ONE thing," "master X" | STRONG TENDENCY |
| No sweeping universal claims: "every PM needs…," "if you're not doing X you're failing" | STRONG TENDENCY |
| No manufactured controversy: "Unpopular opinion:", "Hot take:" | HARD RULE |
| No humble-brag announcements: "I'm humbled and excited to announce…" | HARD RULE |
| No broetry spacing (one line, then a wall of blank lines, to bait the "see more" click) | STRONG TENDENCY |
| No vague empty hook — a question with no concrete content behind it ("How do you find guardrails?"). State the concrete shallow thing first, then the gap | STRONG TENDENCY |

> Note on rhetorical templates (Section A bans "Here's the thing," "It's not X it's Y," etc.): some of those connectives may genuinely be how a given person thinks. Verify against the voice profile before treating any single one as a hard ban — flag, don't silently delete.

> Real annotated specimens of these live in [anti-patterns.md](anti-patterns.md).

---

## G. Output Check

Run once, last, before returning the draft. This is not a style pass — it's a structural sanity check.

- Any unnecessary filler? Could two paragraphs become one?
- Did anything concrete get said, or does it just sound confident?
- Is every recommendation actually actionable?
- Is the same idea being repeated in different words anywhere?
- Any clichés that survived the draft?
- Does it still make sense with the adjectives stripped out?
- Is there a clear point of view, or is it sitting on the fence?
- Does explanation precede conclusion — or does the draft lead with the answer and bury the reasoning?

If any of these flag something, fix it or explicitly surface it to the user before returning.
