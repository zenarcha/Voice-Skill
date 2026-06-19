# Post Types & Hooks

Operational reference for choosing what kind of LinkedIn post to write and how to open it.

**How the skill uses this file:**
1. **Infer post type** — read the user's raw input, match it to one of the 10 post types using the "Use when" field, state the inferred type + reasoning, let the user confirm or reframe.
2. **Suggest hook** — look up the inferred type in the Pairing Table, suggest the primary hook (grounded in what's actually in the input), let the user confirm or override.
3. **Use it** — in Draft mode, read only the chosen post type's framework + the chosen hook's execution notes + phrase bank to draft; in Outline mode, use the type's framework as the map for the suggested arrangement and the hook as advisory angle. Ignore the rest either way.

Nothing here overrides the gap protocol (never invent content) or `guardrails.md`. This file decides *structure and opening*, not voice.

---

## Pairing Table

Drives the hook suggestion. Primary is suggested first; secondary is the fallback or stack option.

| Post type | Primary hook | Secondary hook |
|---|---|---|
| Actionable | Value | Credibility |
| Observation | Eloquence | Counter-Narrative |
| X vs Y | Surprise | Counter-Narrative |
| Motivation | Fear / FOBO | Identity |
| Analytical | Credibility (Labor Illusion) | Value |
| Listicle | Value | Curiosity |
| Contrarian | Counter-Narrative | Fear |
| Testimonial | Credibility | Celebration |
| Personal Story | Curiosity | Credibility |
| Meme | Surprise | Identity |

**Stacking rule:** most high-performing posts combine 2+ hooks. If the user picks one, the skill may suggest the secondary as a complement — but never force it.

---

# Part 1 — Post Types

## Actionable
- **Use when:** the draft teaches a repeatable process — "how to X" or "how I X," with steps the reader could execute.
- **Format:** thread, carousel, or long-form; can be short.
- **Core mechanism:** demonstrate expertise by giving away a complete, executable method — no gaps, no withholding the useful part.
- **Best hooks:** Value (primary), Credibility (secondary).
- **Drafting note:** every step must be concrete enough to act on. If a step is vague, that's a gap question, not a thing to smooth over.

## Observation
- **Use when:** the draft names something the user has noticed in their industry that others aren't naming.
- **Format:** short text, or text + image. Rarely a carousel.
- **Core mechanism:** signal thought leadership by articulating a pattern before it's common knowledge.
- **Best hooks:** Eloquence (primary), Counter-Narrative (secondary).
- **Drafting note:** the value is precision. Resist padding — the observation should land in as few words as possible.

## X vs Y
- **Use when:** the draft frames a choice between two approaches, tools, or mindsets — one favored, one not.
- **Format:** short bullets or a visual comparison.
- **Core mechanism:** the writer controls the framing of both sides (exploits "what you see is all there is").
- **Best hooks:** Surprise (primary), Counter-Narrative (secondary).
- **Drafting note:** converting the comparison into a clean graphic boosts performance. Keep each side parallel in structure.

## Motivation
- **Use when:** the draft pushes the reader to act on something they already know but haven't done.
- **Format:** short-form (or video for longer speeches).
- **Core mechanism:** triggers Fear of Being Outdone + makes the desired outcome feel achievable.
- **Best hooks:** Fear / FOBO (primary), Identity (secondary).
- **Framework — Selfish Desire Targeting:**
  1. Identify the audience's unspoken desire (usually status, wealth, or power).
  2. Make it feel achievable — simplify it, "I did it, you can too," or share a concrete win.
- **Drafting note:** highest-saturation post type on LinkedIn. Only worth it if the angle is specific — otherwise suggest Observation.

## Analytical
- **Use when:** the draft breaks down how a person, company, trend, or framework works.
- **Format:** carousel, thread, long-form, or newsletter.
- **Core mechanism:** teach by teardown — show the mechanics rather than prescribe actions.
- **Best hooks:** Credibility via Labor Illusion (primary), Value (secondary).
- **Drafting note:** the depth is the point. This is the opposite of a Listicle — don't let it flatten into a list.

## Listicle
- **Use when:** the draft aggregates multiple tips/items into one bookmarkable list.
- **Format:** thread, text, or carousel.
- **Core mechanism:** easy to save, low effort to consume.
- **Best hooks:** Value (primary), Curiosity (secondary).
- **Drafting note:** algorithms now discount pure listicles. Use sparingly. If the content has real depth, suggest Actionable or Analytical instead.

## Contrarian
- **Use when:** the draft takes a spiky position that contradicts conventional wisdom in the user's niche.
- **Format:** short, sharp statement.
- **Core mechanism:** disagreement attracts an aligned audience and sparks debate.
- **Best hooks:** Counter-Narrative (primary), Fear (secondary).
- **Framework — Spiky Point of View:** the take should draw from
  - what the user believes differently than peers in their niche, and
  - how their specific experience shaped that belief.
  Build from 4–6 personal facts/biases — the "well" the contrarian take is drawn from. Never manufacture a spiky take the user doesn't actually hold.
- **Drafting note:** the position must be the user's real one. If the draft hedges, ask which way they actually lean — don't pick a side for them.

## Testimonial
- **Use when:** the draft centers a client win, customer result, or piece of social proof.
- **Format:** quote image, video, DM screenshot, or case study.
- **Core mechanism:** social proof — a happy customer sells better than self-description.
- **Best hooks:** Credibility (primary), Celebration (secondary).
- **Drafting note:** drives conversions, not engagement. Lead with the result, not the setup.

## Personal Story
- **Use when:** the draft contains a lived experience with a turning point and a lesson.
- **Format:** long-form narrative.
- **Core mechanism:** narrative identification — the reader sees themselves in the story.
- **Best hooks:** Curiosity (primary), Credibility (secondary).
- **Framework — Pixar structure:**
  - Once upon a time, ___
  - Every day, ___
  - Until one day, ___
  - Because of that, ___
  - Because of that, ___
  - Until finally, ___
- **Drafting note:** length comes from unpacking compressed moments the user already lived — never from invention. If the story has no real turning point underneath it, say so rather than padding.

## Meme
- **Use when:** the draft is a quick, shareable joke that encodes the user's specific point of view.
- **Format:** image / meme.
- **Core mechanism:** fast dopamine hit + viral share trigger.
- **Best hooks:** Surprise (primary), Identity (secondary).
- **Drafting note:** must carry the user's actual POV, not be generically funny. Out of scope for text-drafting — flag if the user wants a visual.

---

# Part 2 — Hooks

A hook is the opening 1–3 lines — everything before the "see more" fold. It changes what makes someone stop scrolling, not what the post says.

## Credibility
- **What it does:** establishes why the user should be trusted on this topic.
- **Lever:** authority. Three variants — (a) accomplishments/experience, (b) visible effort (Labor Illusion — people value things more when they see the work behind them), (c) borrowed credibility from a known person/brand.
- **Execution:** lead with the proof, not the claim it supports.
- **Phrase bank:**
  - "Last year my business did $X in revenue…"
  - "I analyzed 1,000s of posts and noticed…"
  - "I lost over $100,000 on these failures:"
  - "I reviewed 50 [X] so you don't have to."

## Fear
- **What it does:** makes the reader feel a risk of loss or falling behind.
- **Lever:** loss aversion + negativity bias.
- **Execution:** FOMO ("don't miss this"), FOBO / Fear of Being Outdone ("everyone else is ahead"), "I hope I'm not doing this wrong," "I hope that doesn't happen to me."
- **Phrase bank:**
  - "Everyone is scared of X happening…"
  - "You're going to regret not doing this."
  - "I hope I'm not doing this wrong."
  - "The [people] getting ahead right now aren't who you'd expect."

## Curiosity
- **What it does:** opens a loop the reader needs closed.
- **Lever:** dopamine-seeking via open loops.
- **Execution:** tease without resolving — "then what happened?", trailing "…", an image or claim with no explanation yet.
- **Phrase bank:**
  - "I almost quit my [job] six months in."
  - "I don't know who needs to hear this…"
  - "Look closely at most successful [X], and you'll notice something:"
  - "This is a story about how I lost $X…"

## Counter-Narrative
- **What it does:** contradicts a widely-held belief.
- **Lever:** provokes thought/debate — same engine as the Spiky Point of View.
- **Execution:** state the opposite of conventional wisdom in the user's niche, plainly, in the first line.
- **Phrase bank:**
  - "Everyone says X. I think that's mostly wrong."
  - "[Common advice] won't fix [problem]."
  - "The conventional wisdom on X is backwards."

## Eloquence
- **What it does:** articulates an unvoiced feeling precisely.
- **Lever:** recognition — "finally, someone said it."
- **Execution:** find a shared frustration nobody has named well, and name it sharply.
- **Phrase bank:**
  - "Most [people] are busy. Almost none of them are clear."
  - "There's a difference between X and Y that nobody talks about."

## Faces
- **What it does:** uses a human face to stop the scroll (image/video only).
- **Lever:** biological — humans notice faces and mirror emotion.
- **Execution:** shocked expression, contextually relevant selfie, a credible figure's face, or averted gaze drawing the eye toward the subject.
- **Phrase bank:** n/a — this is a visual hook. Flag when the user is producing an image/video, not text.

## Value
- **What it does:** sets a clear expectation of a useful takeaway.
- **Lever:** explicit promise.
- **Execution:** state plainly what the reader gets; optionally preempt an objection ("you might think X, but…") before delivering. Must actually deliver or it reads as clickbait.
- **Phrase bank:**
  - "Here's exactly how to [X]."
  - "[N] [things] I [do] before every [Y]. Steal them."
  - "Here's how I went from X to Y."

## Surprise
- **What it does:** leads with a startling fact or statistic.
- **Lever:** social currency — sharing novel facts raises the sharer's status.
- **Execution:** one startling sentence. Quick-hit, not a story.
- **Phrase bank:**
  - "Did you know [surprising stat]?"
  - "[Counterintuitive fact stated flatly]."

## Celebration
- **What it does:** lowers the barrier to engagement (easy to comment "congrats!").
- **Lever:** social ease — celebration invites low-effort response.
- **Execution:** new jobs, milestones (followers/revenue/funding/awards), birthdays. Often stacks with Credibility + FOBO automatically.
- **Phrase bank:**
  - "[Milestone] just happened and I still can't believe it."
  - "Six months ago [starting point]. Today [result]."

## Identity
- **What it does:** signals "this is for you" to a specific reader segment.
- **Lever:** self-recognition — "hey, that's me."
- **Execution:** (a) Barnum-style statement/question — specific-sounding but broadly applicable, or (b) direct labeling of the group using their own in-group terminology, including the user in that group.
- **Phrase bank:**
  - "If you're a [role] who [specific situation], this is for you."
  - "Every [group] knows this feeling:"

---

## Tactical Notes

- **DM vs comment CTA:** comments publicly signal demand (good for free/high-demand offers); DMs keep interest private (better for paid/limited offers). Only add a CTA if the voice profile confirms a CTA habit — see `voice.md`; do not add one by default.
- **Visual upgrade:** converting plain-text comparisons (X vs Y) or lists into a clean graphic boosts performance.
