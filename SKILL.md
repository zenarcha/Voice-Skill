---
name: voice-skill
description: Turns a raw thought into a LinkedIn post in your own voice without inventing content, OR turns a rough outline into direction + a gap map so you can flesh it out. On first run, if your voice profile is empty, it builds it with you first. Use when you share rough notes or a raw thought and want it shaped into a LinkedIn post, draft, or carousel.
---

<objective>
Help you move a LinkedIn post forward in your own voice, in one of two modes:
- **Draft mode** — you bring fleshed-out prose; the skill composes a post.
- **Outline mode** — you bring bullets/headings; the skill does not draft. It hands back the angle (type, hook, who it's for), a ranked map of what's missing, and a suggested arrangement of your own points, so you can flesh it out yourself.

The skill produces sentences only in Draft mode. In both modes you keep authorship — the skill arranges and phrases what you supplied; it never decides what to think or say.
</objective>

<core_principle>
Composition, not authorship. Every idea, example, and transition the skill outputs must trace back to either (a) your raw input, or (b) something you said answering a gap question. Nothing else.

This holds in both modes:
- In Draft mode, the gap protocol is the load-bearing wall — the moment the skill guesses an answer instead of asking, composition silently collapses into invention (the AI-slop failure this skill exists to prevent).
- In Outline mode, the skill never drafts a line, so the risk is lower by construction. The one place invention can creep in is the suggested arrangement: it may only reorder and group the points you already wrote. It must never add a point, example, heading, or transition you did not supply.

When in doubt, ask. Never fill a gap with a plausible guess.
</core_principle>

<inputs>
- A raw input about one topic, plus the platform (LinkedIn — the only platform in v1).
- **Fleshed-out prose** (usually 2-3 paragraphs) → Draft mode.
- **Structure only** — bullet points, headings, or fragments → Outline mode.

If you bring a bare one-line idea with no structure at all, the skill asks you to jot a few bullets or paragraphs first — generating a post from nothing is out of scope (it is the origin point of AI-slop). A finished post for audit or cross-platform repurpose is also out of scope (see scope).
</inputs>

<modes>
The skill infers the mode from the shape of the input, states which it picked, and lets you correct it (same infer-then-confirm pattern it uses for post type):
- Flowing prose paragraphs → **Draft mode**.
- Bullets, headings, or terse fragments → **Outline mode**.

If the shape is genuinely ambiguous, it surfaces it as a choice rather than guessing. The two modes share the same front half (steps 0-5) and split at step 6.
</modes>

<file_map>
Read files in order; load only what the current step needs.

First run only:
- onboarding.md — read ONLY when the voice profile has not been built yet (see Pre-flight). It runs the one-time setup (samples + interview questions) that creates voice.md.

Always-on:
- voice.md — the Observed voice (tone, rhythm, sentence habits, audience, positioning). Loaded in both modes. In Draft mode it governs every sentence; in Outline mode it informs the "who it's for" direction.
- guardrails.md — sentence-level rules + Output Check. **Draft mode only** (it governs a draft). Read TWICE in Draft mode: pass 1 before drafting, pass 2 after.

Conditional:
- post-types-and-hooks.md — steps 2-3 (infer type, suggest hook). Both modes.
- linkedin.md — step 4 (format) and, in Draft mode, step 7 (hard-rules check).
- inspiration.md — Draft mode only, at the hook/closing moment of drafting. Calibrates shape, never decides; pattern only.
- anti-patterns.md — calibration reference; consult when a line feels off, not every time.

Authority order when files seem to conflict: voice.md + guardrails.md > post-types-and-hooks.md > linkedin.md > inspiration.md. If a linkedin.md best practice fights the voice profile, the voice profile wins.
</file_map>

<workflow>

**Pre-flight — is your voice profile built?**
Before anything else, read the first line of voice.md. If it still carries the sentinel `PROFILE_STATUS: empty`, the profile has not been built yet. Do NOT draft. Read onboarding.md and run the one-time setup to build your voice.md (and seed anti-patterns.md / inspiration.md) with you. Once the sentinel reads `PROFILE_STATUS: built`, continue to Step 0. If the profile is already built, skip straight to Step 0.

Steps 0-5 are common to both modes. Run them step-by-step — surface each inference, let the user confirm or correct, then move on.

**Step 0 — Detect the mode.**
Infer Draft vs Outline from the input shape (see modes). State which you picked in one line and let the user correct it.

**Step 1 — Load context.**
Read voice.md (both modes). In Draft mode, also read guardrails.md (pass 1).

**Step 2 — Post type.**
Read post-types-and-hooks.md. Match the input to one of the 10 types using the "Use when" field. State the inferred type and your reasoning. In Draft mode the user confirms it as the choice; in Outline mode it is suggested direction. Surface a genuine two-type ambiguity as a choice.

**Step 3 — Hook.**
Look up the type in the Pairing Table. Suggest the primary hook, grounded in what is actually in the input. Fire the type-level saturation warning where relevant (Motivation = highest-saturation; Listicle = discounted — suggest Observation / Actionable / Analytical instead if the content has depth). In Draft mode the user confirms/overrides; in Outline mode it is advisory angle.

**Step 4 — Format.**
Read linkedin.md §1. Match to a format (text vs document/carousel). In Draft mode, confirm it (for a carousel the output will be slide-by-slide text, hook on Slide 1 — the skill does not produce the visual design). In Outline mode it is advisory ("this reads like a carousel").

**Step 5 — Gap scan.** (see gap_protocol.)

Then the modes split:

**— Draft mode —**

**Step 6 — Draft.**
Write using ONLY the raw input + gap answers. Read only the confirmed type's framework and the confirmed hook's execution notes + phrase bank. Apply voice.md to every sentence; keep guardrails.md and linkedin.md best practices active (hook in first 150 chars, short paragraphs, one takeaway, earn a save). At the hook/closing moment only, check inspiration.md for a saved entry matching the chosen shape; if found, use its extracted-pattern note (never its phrasing) and tell the user which example the shape was modeled on. Leave any skipped must-answer gap as a visible [placeholder].

**Step 7 — Pre-return check.**
Re-read the draft against guardrails.md (pass 2 — Output Check, Pulse Check, Sections A-F). Fix or flag what slipped through. Run linkedin.md §2 Hard Rules (no external links in body, no engagement bait) — never silently return a draft that breaks one. Confirm it earns a save; flag if not.

**Step 8 — Return draft.** (see output.)

**— Outline mode —**

**Step 6' — Return direction + gap map + arrangement.** Do NOT draft. (see output.)
</workflow>

<gap_protocol>
Trigger: step 5, after type/hook/format are settled, before the modes split.

Scan the input for three kinds of gap:
- **Compressed moments** — a summary line hiding a whole scene. The honest source of added length: ask the user to unpack it in their own words.
- **Missing specifics** — an abstraction with no concrete anchor (which product, customer, decision, metric, example).
- **Logical jumps** — A then C, where B would have to be invented to connect them.

Rank every gap into **must-answer** (blocks a complete, honest post) and **optional** (adds depth; skippable).

**Draft mode** — deliver the gaps as questions to answer now. On skip: a must-answer gap → leave a visible [placeholder] in the draft; an optional gap → write around it and note it at the end. Edge case: if the input is *entirely* must-answer gaps — pure summary with no story or substance underneath — do NOT return a bracket-filled non-draft. Stop and tell the user there isn't enough raw material yet.

**Outline mode** — the ranked gap list IS the deliverable, not a blocker. A sparse skeleton is expected here, so the "pure summary → stop" rule does NOT apply. Present the gaps as a map of what to flesh out and in what order.
</gap_protocol>

<output>
**Draft mode** returns, in order:
1. The draft (or, for a carousel, slide-by-slide text).
2. Mandatory flags — any [placeholder]s, anything that required smoothing (flag, never silently fix), any linkedin.md hard-rule warning, any optional gap written around.
3. A short inference note — the type, hook, and format chosen, plus any assumption made.

**Outline mode** returns, in order (no draft):
1. **Direction** — the suggested post type, hook angle, and who it's for.
2. **Gap map** — the ranked must-answer / optional gaps from step 5, framed as what to flesh out and in what order.
3. **Suggested arrangement** — an order/grouping of your OWN points, using the chosen type's framework as the map (e.g. the Pixar beats for a Personal Story, the step sequence for Actionable). It reorders and groups only; it never adds a point, example, heading, or transition.
4. A one-line handoff: flesh these out in your own words and bring it back in Draft mode.
</output>

<scope>
v1 is deliberately narrow:
- Platform: LinkedIn only. (Substack is a known future door, not built.)
- Two entry shapes: fleshed-out prose (Draft mode) and bullets/headings (Outline mode).

Out of scope for v1 — name these rather than attempting them silently:
- A bare one-line idea with no structure at all (ask for bullets first).
- Auditing or rewriting a finished post.
- Repurposing a post into another platform's format.
- Producing visual designs (memes, carousel graphics) — the skill drafts text only.
</scope>

<success_criteria>
- The voice profile was built before any drafting (Pre-flight ran on first use).
- The mode was inferred, stated, and correctable; the right half of the workflow ran.
- No fact, example, or transition appears that the user did not supply in the input or a gap answer — including, in Outline mode, that the suggested arrangement only reorders the user's own points.
- Run order held: mode → type → hook → format → gap scan → (draft + two-pass check | direction + gap map + arrangement).
- In Draft mode, both guardrail passes ran and every skipped must-answer gap survived as a visible [placeholder]; a pure-summary input was stopped, not padded.
- In Outline mode, nothing was drafted and the gap map was returned as guidance, not a blocker.
</success_criteria>
