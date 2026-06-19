# Onboarding — build your voice profile (one time)

Read and run this file ONLY on first use, when `voice.md` still carries the sentinel
`PROFILE_STATUS: empty`. Its job is to build *your* `voice.md` (and seed `anti-patterns.md`
and `inspiration.md`) so the skill writes like you, not like a generic AI. Once the profile is
built, this file is never read again.

> **Credit / inspiration:** the idea behind this — a plain text file that captures how *you*
> write, so an AI can sound like you instead of like itself — is inspired by Ruben's essay
> [*I am just a text file*](https://ruben.substack.com/p/i-am-just-a-text-file). The questions
> below are original to this skill; none of Ruben's wording is reproduced. Worth reading the
> essay for the why.

---

## Step A — Samples first (the cheapest, most reliable signal)

Ask the user to paste **any real writing of their own** — old posts, newsletter notes, even
long messages they're proud of. Raw, unedited writing is worth more than self-report: people
are unreliable narrators of their own sentence habits, so observed mechanics beat described
ones.

- If they have samples: read them for *observable mechanics* — sentence length and rhythm,
  paragraph/line-break density, opener and closer patterns, punctuation tics, bullets-vs-prose
  habits, recurring word choices.
- If they have none yet: note that the mechanics section of `voice.md` will be thin and should
  be tightened later, once they've published and can feed real posts back in.

Do not infer taste or beliefs from samples alone — that comes from the interview (Step B).

## Step B — Run the interview

Walk the user through the questions below **conversationally** — one or two at a time, not a
wall of text. Capture answers **verbatim** where you can; the exact words are evidence. **Don't
infer and move on** — if an answer is thin or vague, ask one follow-up. Skip whatever the
samples already revealed; dig where they didn't. Label every trait you capture **HARD RULE /
STRONG TENDENCY / LIGHT PREFERENCE**.

**1. Beliefs & point of view**
- What's something in your field that most people get wrong — that you'd happily argue about?
- What do you wish more people understood about the work you actually do?
- Is there common advice in your space you quietly ignore? Why?
- When you read a take in your niche, what makes you think "that's lazy"?

**2. What makes you cringe**
- Describe (or paste) a post that made you roll your eyes. What exactly set you off?
- Which words or phrases instantly make a post feel fake to you?
- Any formatting moves you can't stand — emojis, one-line-per-paragraph spacing, all-caps?
- Where does "confident" tip over into "trying too hard" for you?

**3. Your voice & personality**
- If a friend read something you wrote with your name removed, how would they still know it's you?
- Are you funny on the page, or is humour not your thing? (Be honest — forced jokes read as fake.)
- Pick the few words closest to how you sound: warm, blunt, calm, intense, dry, earnest, playful…
- When you're genuinely excited, does it show on the page, or does your writing stay even?

**4. How you build a piece**
- Short, punchy lines? Longer, flowing sentences? A mix?
- Do you reach for bullets, or do you prefer prose?
- How do you usually open a post? How do you usually end one?
- Any habits you already know you have — a word you overuse, a way you always transition?

**5. Hard nos**
- What would you never say or do in a post, even if it "performed well"?
- Are there words that are an instant no for you?
- Would you ever open with "Unpopular opinion" or "Hot take"? Why or why not?

**6. What makes you distrust a writer**
- When do you stop trusting someone's post partway through?
- Where's the line, for you, between sharing a learning and performing expertise?

**7. Quick parameters**
- Who are you mainly writing for?
- What do you want your writing to do for you?
- Your tone in one line?
- How formal do you want to come across?
- British or American spelling?

Do not invent answers. If something stays vague, ask the user directly rather than guessing.

## Step C — Synthesise into the profile (this is the skill's real work)

Turn the answers + samples into `voice.md`, **evidence-first**:

- **Never invent a trait.** Every entry must trace to a specific interview answer or a sample.
  If you can't cite where it came from, leave it out.
- **Label every trait with a frequency:** `HARD RULE` (never violate) · `STRONG TENDENCY`
  (~70-80%, occasional breaks fine) · `LIGHT PREFERENCE` (tiebreaker). This is the
  anti-overfitting guard — it stops the skill from mechanically stacking every tendency.
- **Separate Observed from Preferred.** Observed = how they actually write now (from samples).
  Preferred = what they're reaching toward (from the interview / admired writing). Keep them
  distinct so the skill doesn't treat aspiration as habit.
- **Apply the litmus test** to every entry you write: *"does this sound like something they'd
  actually write, or like an AI trying hard to imitate them?"* If it feels forced, cut it.
- Fill the `voice.md` template's sections: parameters table, core identity, beliefs & point of
  view, writing mechanics, aesthetic crimes, voice & personality, structural preferences, hard
  nos, red flags, and the quick-reference card.

Then seed the two calibration libraries from the same answers:
- **anti-patterns.md** — from their "what makes you cringe" answers, write one or two annotated
  entries in the file's format (the offending example + *why it fails for them*). These are
  theirs; never copy anyone else's specimens in.
- **inspiration.md** — from any writing they said they admire, record the **extracted pattern**
  only (the reusable shape, in plain words — never the phrasing), per that file's format.

## Step D — Flip the switch and confirm

- Change the first line of `voice.md` from `PROFILE_STATUS: empty` to `PROFILE_STATUS: built`.
- Show the user a short summary of what you captured and ask them to correct anything that
  doesn't sound like them before you save.
- Tell them the profile improves over time: as they publish real posts, paste them back to
  tighten the Observed mechanics.

Once the sentinel reads `built`, return to SKILL.md and proceed with the normal workflow.
